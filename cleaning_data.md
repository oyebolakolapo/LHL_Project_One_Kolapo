What issues will you address by cleaning the data?





Queries:
Below, provide the SQL queries you used to clean your data.
--Data cleaning
SELECT *
FROM all_sessions
ORDER BY country
DESC
LIMIT 10

--Drop columns "itemquantity", "productrefundamount", "searchkeyword" which appear to be empty in the "all_sessions" table
--First let's reconfirm
SELECT COUNT(*)
FROM all_sessions
WHERE itemquantity IS NOT NULL

SELECT COUNT(*)
FROM all_sessions
WHERE prodcutrefundamount IS NOT NULL

SELECT COUNT(*)
FROM all_sessions
WHERE searchkeyword IS NOT NULL

--Drop "itemquantity", "productrefundamount", "searchkeyword"
ALTER TABLE all_sessions 
DROP COLUMN itemquantity,
DROP COLUMN productrefundamount,
DROP COLUMN searchkeyword;

--Drop column "userid" which appears to be empty in the "analytics_renamed" table
--First let's reconfirm
SELECT COUNT(*)
FROM analytics_renamed
WHERE userid IS NOT NULL

ALTER TABLE analytics_renamed 
DROP COLUMN userid;
