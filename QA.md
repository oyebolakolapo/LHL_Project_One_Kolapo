What are your risk areas? Identify and describe them.

I focused on resolving the following issues:


##Remove irrelevant data

##Remove duplicate data

##Fix structural errors

##Do type conversion

##Handle missing data

##Deal with outliers

##Standardize/Normalize data

##Validate data

QA Process:
#Describe your QA process and include the SQL queries used to execute it.
##1. I carried out data profiling to identify the schema of the ecommerce database: That is, 
   SELECT *
   FROM information_schema.tables
   WHERE table_schema = 'public';
##2. I went ahead to determine the data types, null values, and unique values:
   SELECT column_name, data_type, is_nullable
   FROM information_schema.columns
   WHERE table_name = 'all_sessions';

   SELECT COUNT(DISTINCT fullvisitorid)
   FROM all_sessions;

##3. I also checked for duplicate data e.g:
   SELECT country, COUNT(*)
   FROM all_sessions
   GROUP BY country
   HAVING COUNT(*) > 1;
##4. Removed structural errors in the dataset: Structural errors include strange naming conventions, typos, or incorrect capitalization. For instance, in the vproductcategory of the all_sessions table, I saw reported as '(not set)' which we standardized by replacing them with "null". That is,
SELECT *,
IF (v2productcategory IN ('(not set)'), NULL, v2productcategory)  AS v2productcategory_clean 
FROM all_sessions;

##5. Checked for outliers
Suspected outliers are values at least 1.5 * IQR below the first-quartile or above the third-quartile. 
WITH 
quantiles AS (
  SELECT *,
    (APPROX_QUANTILES(unit_price_actual, 4) [OFFSET] (1)) AS percentile_25,
    (APPROX_QUANTILES(unit_price_actual, 4) [OFFSET] (3)) AS percentile_75,
  FROM analytics_renamed
),

iqr AS (
  SELECT *,
    1.5 * (percentile_75 - percentile_25) AS iqr_value
  FROM quantiles
),

outliers AS (
  SELECT fullvisitorid, 
    IF(unit_price_actual < (percentile_25 - iqr_value) 
       OR unit_price_actual > (percentile_75 + iqr_value), NULL, unit_price_actual) 
       AS unit_price_actual_null
  FROM iqr, analytics_renamed
)

SELECT name,
  IFNULL(unit_price_actual_null, AVG(unit_price_actual_null) OVER()) AS clean_unit_price
FROM outliers;   


