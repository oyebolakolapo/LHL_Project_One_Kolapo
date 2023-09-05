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

SELECT all_sessions.fullvisitorid, all_sessions.city, all_sessions.country, products.name, avg (products.orderedquantity) AS avgnumberofproducts
FROM all_sessions
INNER JOIN products
ON all_sessions.productsku = products.productsku
GROUP BY fullvisitorid, city, country, products.name
ORDER By country

Answer:
fullvisitorid	city	country	name	avgnumberofproducts
6.33E+18	Sydney	Australia	 Cam Indoor Security Camera - USA	2139
8.99E+17	not available in demo dataset	Canada	 Sunglasses	887
8.91E+18	not available in demo dataset	Canada	 Men's Vintage Badge Tee White	121
7.36E+18	not available in demo dataset	France	Android Wool Heather Cap Heather/Black	168
2.58E+16	San Francisco	United States	 Cam Outdoor Security Camera - USA	2719
8.61E+16	Mountain View	United States	 Men's Vintage Badge Tee Sage	193
2.24E+17	Austin	United States	 Men's 100% Cotton Short Sleeve Hero Tee Black	90
3.68E+17	Sunnyvale	United States	SPF-15 Slim & Slender Lip Balm	3682
4.01E+17	San Francisco	United States	 Cam Outdoor Security Camera - USA	2719
4.57E+17	not available in demo dataset	United States	 Men's Short Sleeve Hero Tee Charcoal	17
5.38E+17	Chicago	United States	 Sunglasses	1046
1.25E+18	Columbus	United States	 Men's Short Sleeve Badge Tee Charcoal	5
1.7E+18	Mountain View	United States	 Learning Thermostat 3rd Gen-USA - Stainless Steel	1886
2.31E+18	Mountain View	United States	 Learning Thermostat 3rd Gen-USA - Stainless Steel	1886
2.4E+18	not available in demo dataset	United States	 Laptop and Cell Phone Stickers	1033
2.81E+18	not available in demo dataset	United States	 Learning Thermostat 3rd Gen-USA - Stainless Steel	1886
3.22E+18	not available in demo dataset	United States	 Mood Original Window Decal	63
3.44E+18	not available in demo dataset	United States	 Bongo Cupholder Bluetooth Speaker	85
3.76E+18	not available in demo dataset	United States	 Cam Indoor Security Camera - USA	2139
4.13E+18	not available in demo dataset	United States	Four Color Retractable Pen	2002
4.4E+18	Sunnyvale	United States	 Cam Indoor Security Camera - USA	2139
4.41E+18	Irvine	United States	 Laptop and Cell Phone Stickers	1033
4.85E+18	Nashville	United States	 Learning Thermostat 3rd Gen-USA - Stainless Steel	1886
4.95E+18	Chicago	United States	 Womens 3/4 Sleeve Baseball Raglan Heather/Black	23
5.04E+18	Palo Alto	United States	 Learning Thermostat 3rd Gen-USA - White	849
5.1E+18	Salem	United States	Red Spiral  Notebook	316
5.96E+18	Mountain View	United States	 Men's Bike Short Sleeve Tee Charcoal	41
6.34E+18	Detroit	United States	 22 oz Water Bottle	10075
6.57E+18	Chicago	United States	 Learning Thermostat 3rd Gen-USA - Stainless Steel	1886
6.84E+18	not available in demo dataset	United States	 Sunglasses	1573
7.37E+18	New York	United States	 Men's  Zip Hoodie	90
7.68E+18	not available in demo dataset	United States	 Men's Airflow 1/4 Zip Pullover Lapis	3
8.65E+18	Mountain View	United States	 Mobile Phone Vent Mount	68
8.8E+18	San Jose	United States	 Men's  Zip Hoodie	90![image](https://github.com/oyebolakolapo/LHL_Project_One_Kolapo/assets/40770957/0ec3074c-8580-4fbb-a4c4-797cdd90a0ee)

**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:
SELECT v2productcategory, fullvisitorid, city, country 
FROM all_sessions
GROUP BY v2productcategory, fullvisitorid, city, country 
ORDER BY v2productcategory

Answer:
v2productcategory	fullvisitorid	city	country
(not set)	8.99E+17	not available in demo dataset	Canada
(not set)	1.25E+18	Columbus	United States
(not set)	2.4E+18	not available in demo dataset	United States
(not set)	4.41E+18	Irvine	United States
(not set)	5.1E+18	Salem	United States
(not set)	7.37E+18	New York	United States
Apparel	8.61E+16	Mountain View	United States
Apparel	2.24E+17	Austin	United States
Apparel	4.57E+17	not available in demo dataset	United States
Apparel	7.27E+17	Bengaluru	India
Apparel	7.43E+17	New York	United States
Apparel	3.29E+18	Toronto	Canada
Apparel	4.95E+18	Chicago	United States
Apparel	5.96E+18	Mountain View	United States
Apparel	7.68E+18	not available in demo dataset	United States
Apparel	8.8E+18	San Jose	United States
Apparel	8.91E+18	not available in demo dataset	Canada
Bags	1.48E+18	not available in demo dataset	United States
Bags	8.44E+18	Atlanta	United States
Drinkware	6.34E+18	Detroit	United States
Electronics	3.44E+18	not available in demo dataset	United States
Electronics	7.3E+18	not available in demo dataset	United States
Headgear	7.36E+18	not available in demo dataset	France
Housewares	3.68E+17	Sunnyvale	United States
Lifestyle	5.38E+17	Chicago	United States
Lifestyle	6.84E+18	not available in demo dataset	United States
Nest-USA	2.58E+16	San Francisco	United States
Nest-USA	4.01E+17	San Francisco	United States
Nest-USA	1.7E+18	Mountain View	United States
Nest-USA	2.31E+18	Mountain View	United States
Nest-USA	2.81E+18	not available in demo dataset	United States
Nest-USA	3.76E+18	not available in demo dataset	United States
Nest-USA	4.4E+18	Sunnyvale	United States
Nest-USA	4.85E+18	Nashville	United States
Nest-USA	5.04E+18	Palo Alto	United States
Nest-USA	6.33E+18	Sydney	Australia
Nest-USA	6.57E+18	Chicago	United States
Office	4.13E+18	not available in demo dataset	United States
Waze	3.22E+18	not available in demo dataset	United States
Waze	8.65E+18	Mountain View	United States![image](https://github.com/oyebolakolapo/LHL_Project_One_Kolapo/assets/40770957/fc335c7c-f2cd-4c17-b8a5-4ae38cb1b4ef)


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







