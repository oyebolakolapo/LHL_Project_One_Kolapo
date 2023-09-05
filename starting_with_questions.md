Answer the following questions and provide the SQL queries used to find the answer.

    
**Question 1: Which cities and countries have the highest level of transaction revenues on the site?**


SQL Queries:
SELECT city, country, totaltransactionrevenue 
FROM all_sessions
WHERE totaltransactionrevenue IS NOT NULL
ORDER BY totaltransactionrevenue DESC
LIMIT 10);
Answer:
city	country	totaltransactionrevenue
not available in demo dataset	United States	1015480000
not available in demo dataset	United States	1005500000
Atlanta	United States	742480000
Sunnyvale	United States	649240000
not available in demo dataset	United States	391000000
Sydney	Australia	358000000
Chicago	United States	306000000
San Francisco	United States	202000000
Sunnyvale	United States	200000000
not available in demo dataset	United States	169970000![image](https://github.com/oyebolakolapo/LHL_Project_One_Kolapo/assets/40770957/7e9c364f-6ff4-41d3-a015-858e6a604102)

**Question 2: What is the average number of products ordered from visitors in each city and country?**


SQL Queries:
--We need information "orderedquantity" from products table & "fullvisitorid", "city" and "country" from all_sessions table
--To JOIN table "products" and table "all_sessions" at sku column which was named productsku in all_sessions,
--we will rename productsku to sku for consistency.

ALTER TABLE products 
RENAME COLUMN sku TO productsku;

--Then we will INNER JOIN all_sessions table with products table

SELECT all_sessions.fullvisitorid, all_sessions.city, all_sessions.country, avg (products.orderedquantity) AS avgnumberofproducts
FROM all_sessions
INNER JOIN products
ON all_sessions.productsku = products.productsku
GROUP BY fullvisitorid, city, country
ORDER By country

Answer:
fullvisitorid	city	country	avgnumberofproducts
6.33E+18	Sydney	Australia	2139
8.99E+17	not available in demo dataset	Canada	887
8.91E+18	not available in demo dataset	Canada	121
7.36E+18	not available in demo dataset	France	168
2.58E+16	San Francisco	United States	2719
8.61E+16	Mountain View	United States	193
2.24E+17	Austin	United States	90
3.68E+17	Sunnyvale	United States	3682
4.01E+17	San Francisco	United States	2719
4.57E+17	not available in demo dataset	United States	17
5.38E+17	Chicago	United States	1046
1.25E+18	Columbus	United States	5
1.7E+18	Mountain View	United States	1886
2.31E+18	Mountain View	United States	1886
2.4E+18	not available in demo dataset	United States	1033
2.81E+18	not available in demo dataset	United States	1886
3.22E+18	not available in demo dataset	United States	63
3.44E+18	not available in demo dataset	United States	85
3.76E+18	not available in demo dataset	United States	2139
4.13E+18	not available in demo dataset	United States	2002
4.4E+18	Sunnyvale	United States	2139
4.41E+18	Irvine	United States	1033
4.85E+18	Nashville	United States	1886
4.95E+18	Chicago	United States	23
5.04E+18	Palo Alto	United States	849
5.1E+18	Salem	United States	316
5.96E+18	Mountain View	United States	41
6.34E+18	Detroit	United States	10075
6.57E+18	Chicago	United States	1886
6.84E+18	not available in demo dataset	United States	1573
7.37E+18	New York	United States	90
7.68E+18	not available in demo dataset	United States	3
8.65E+18	Mountain View	United States	68
8.8E+18	San Jose	United States	90![image](https://github.com/oyebolakolapo/LHL_Project_One_Kolapo/assets/40770957/127166d6-66be-40d5-b39e-5f7130d18251)

**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:
SELECT all_sessions.fullvisitorid, all_sessions.type_s, all_sessions.city, all_sessions.country, products.orderedquantity
FROM all_sessions
FULL JOIN products
ON all_sessions.productsku = products.productsku
GROUP BY all_sessions.fullvisitorid, all_sessions.type_s, all_sessions.city, all_sessions.country, products.orderedquantity
ORDER BY all_sessions.type_s

Answer:

No striking pattern identified



**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:

SELECT all_sessions.city, all_sessions.country, products.orderedquantity, all_sessions.productvariant
FROM all_sessions
FULL JOIN products
ON all_sessions.productsku = products.productsku
WHERE products.orderedquantity =  (SELECT MAX (products.orderedquantity)
   FROM products)
GROUP BY all_sessions.productvariant, all_sessions.city, all_sessions.country, products.orderedquantity
ORDER BY all_sessions.country
Answer:





**Question 5: Can we summarize the impact of revenue generated from each city/country?**

SQL Queries:



Answer:







