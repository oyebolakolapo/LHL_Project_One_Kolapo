What are your risk areas? Identify and describe them.

The risk areas for the data include:
1. Consistency: This includes order and format of year (YYYY-MM-DD) or time:

2. Accuracy
   
4. Validity:  e.g datatype requirement
   
5. Uniqueness: For each unique record expected in a database there should be one field that uniquely identifies each given record, e.g. a visitor's id number for the ecommerce website. That account number’s uniqueness may be critical to identifying repeated transactions for a single visitor's transaction.
   
6. Completeness: Data is incomplete if there are missing critical fields.

7. Timeliness: What are the expectations on receiving new data into each report? The timeliness of data is defined by the needs of the business. For example, if it’s necessary for a data set to be refreshed daily, the testing metric for timeliness on that data set is also daily.


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


   


