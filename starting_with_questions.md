Answer the following questions and provide the SQL queries used to find the answer.

    
**Question 1: Which cities and countries have the highest level of transaction revenues on the site?**


SQL Queries:
SELECT city, country, totaltransactionrevenue FROM all_sessions
WHERE totaltransactionrevenue = (
   SELECT MAX (totaltransactionrevenue)
   FROM all_sessions
);
Answer:
city	country	totaltransactionrevenue
not available in demo dataset	United States	1015480000![image](https://github.com/oyebolakolapo/LHL_Project_One_Kolapo/assets/40770957/0731b433-91bc-4ad8-81d4-c9471a44d3d3)


**Question 2: What is the average number of products ordered from visitors in each city and country?**


SQL Queries:



Answer:





**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:



Answer:





**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:



Answer:





**Question 5: Can we summarize the impact of revenue generated from each city/country?**

SQL Queries:



Answer:







