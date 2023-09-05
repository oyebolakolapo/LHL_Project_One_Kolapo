What issues will you address by cleaning the data?





Queries:
Below, provide the SQL queries you used to clean your data.
--DATA CLEANING
--1. View rows and columns of first table all_sessions to identify inconsistencies
SELECT *
FROM all_sessions

--2. Drop columns "itemquantity", "productrefundamount", "searchkeyword" and "itemrevenue" which appeared to be empty in the "all_sessions" table
--First let's check columns 
SELECT COUNT(*)
FROM all_sessions
WHERE itemquantity IS NOT NULL

SELECT COUNT(*)
FROM all_sessions
WHERE prodcutrefundamount IS NOT NULL

SELECT COUNT(*)
FROM all_sessions
WHERE searchkeyword IS NOT NULL

SELECT COUNT(*)
FROM all_sessions
WHERE itemrevenue IS NOT NULL

--3. Drop "itemquantity", "productrefundamount", "searchkeyword", "itemrevenue"
ALTER TABLE all_sessions 
DROP COLUMN itemquantity,
DROP COLUMN productrefundamount,
DROP COLUMN searchkeyword,
DROP COLUMN itemrevenue

--4. Check null columns in table "analytics_renamed" by viewing first 50 rows
SELECT *
FROM analytics_renamed
LIMIT 50

--Drop column "userid" which appears to be empty in the "analytics_renamed" table
--First let's reconfirm
SELECT COUNT(*)
FROM analytics_renamed
WHERE userid IS NOT NULL
--Then drop the column
ALTER TABLE analytics_renamed 
DROP COLUMN userid;

SELECT COUNT(*)
FROM analytics_renamed
WHERE units_sold IS NOT NULL

--5. Check null columns in table "products" by viewing first 50 rows
SELECT *
FROM products
LIMIT 50
--6. Check null columns in table "sales_by_sku" by viewing first 50 rows
SELECT *
FROM sales_by_sku
LIMIT 50
--7. Check null columns in table "sales_report" by viewing first 50 rows
SELECT *
FROM sales_report
LIMIT 50

--8. Divide column "unit_price" by 1000000 in a new column "unit_price_actual" in table analytics_renamed 
ALTER TABLE analytics_renamed
ADD unit_price_actual decimal;
UPDATE analytics_renamed SET unit_price_actual = (unit_price / 1000000);
