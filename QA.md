What are your risk areas? Identify and describe them.

The risk areas for the data include:

##Remove irrelevant data

##Remove duplicate data

##Fix structural errors

##Do type conversion

##Handle missing data

##Deal with outliers

##Standardize/Normalize data

##Validate data

QA Process:
Describe your QA process and include the SQL queries used to execute it.
1. I carried out data profiling to identify the schema of the ecommerce database: That is, 
   SELECT *
   FROM information_schema.tables
   WHERE table_schema = 'public';
2. I went ahead to determine the data types, null values, and unique values:
   SELECT column_name, data_type, is_nullable
   FROM information_schema.columns
   WHERE table_name = 'all_sessions';

   SELECT COUNT(DISTINCT fullvisitorid)
   FROM all_sessions;

3. I also checked for duplicate data e.g:
   SELECT country, COUNT(*)
   FROM all_sessions
   GROUP BY country
   HAVING COUNT(*) > 1;


   


