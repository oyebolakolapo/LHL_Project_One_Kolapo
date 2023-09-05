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
SELECT v2productcategory, fullvisitorid, city, country, sales_report.total_ordered 
FROM all_sessions
LEFT JOIN sales_report ON all_sessions.productssku = sales_report.productssku
GROUP BY v2productcategory, sales_report.total_ordered, fullvisitorid, city, country
ORDER BY v2productcategory, country

Answer:
Nest-USA was the most ordered item especially from visitors in US cities.
v2productcategory	fullvisitorid	city	country	total_ordered
(not set)	8.99E+17	not available in demo dataset	Canada	14
(not set)	7.37E+18	New York	United States	4
(not set)	2.4E+18	not available in demo dataset	United States	13
(not set)	4.41E+18	Irvine	United States	13
(not set)	1.25E+18	Columbus	United States	NULL
(not set)	5.1E+18	Salem	United States	NULL
Apparel	3.29E+18	Toronto	Canada	NULL
Apparel	8.91E+18	not available in demo dataset	Canada	NULL
Apparel	7.27E+17	Bengaluru	India	NULL
Apparel	8.8E+18	San Jose	United States	4
Apparel	4.57E+17	not available in demo dataset	United States	5
Apparel	8.61E+16	Mountain View	United States	NULL
Apparel	2.24E+17	Austin	United States	NULL
Apparel	7.43E+17	New York	United States	NULL
Apparel	4.95E+18	Chicago	United States	NULL
Apparel	5.96E+18	Mountain View	United States	NULL
Apparel	7.68E+18	not available in demo dataset	United States	NULL
Bags	1.48E+18	not available in demo dataset	United States	NULL
Bags	8.44E+18	Atlanta	United States	NULL
Drinkware	6.34E+18	Detroit	United States	23
Electronics	3.44E+18	not available in demo dataset	United States	NULL
Electronics	7.3E+18	not available in demo dataset	United States	NULL
Headgear	7.36E+18	not available in demo dataset	France	0
Housewares	3.68E+17	Sunnyvale	United States	60
Lifestyle	6.84E+18	not available in demo dataset	United States	14
Lifestyle	5.38E+17	Chicago	United States	26
Nest-USA	6.33E+18	Sydney	Australia	102
Nest-USA	5.04E+18	Palo Alto	United States	7
Nest-USA	1.7E+18	Mountain View	United States	94
Nest-USA	2.31E+18	Mountain View	United States	94
Nest-USA	2.81E+18	not available in demo dataset	United States	94
Nest-USA	4.85E+18	Nashville	United States	94
Nest-USA	6.57E+18	Chicago	United States	94
Nest-USA	3.76E+18	not available in demo dataset	United States	102
Nest-USA	4.4E+18	Sunnyvale	United States	102
Nest-USA	2.58E+16	San Francisco	United States	112
Nest-USA	4.01E+17	San Francisco	United States	112
Office	4.13E+18	not available in demo dataset	United States	22
Waze	8.65E+18	Mountain View	United States	4
Waze	3.22E+18	not available in demo dataset	United States	5![image](https://github.com/oyebolakolapo/LHL_Project_One_Kolapo/assets/40770957/708c2850-1eaa-4828-9581-ba189529238e)

**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:

SSELECT products.name, city, country, products.orderedquantity 
FROM all_sessions
INNER JOIN products ON all_sessions.productssku = products.productssku
GROUP BY products.name, city, country, products.orderedquantity 
ORDER BY country, products.orderedquantity DESC
Answer:

name	city	country	orderedquantity
 Cam Indoor Security Camera - USA	Sydney	Australia	2139
 Sunglasses	not available in demo dataset	Canada	887
 Men's Vintage Badge Tee White	not available in demo dataset	Canada	121
Android Wool Heather Cap Heather/Black	not available in demo dataset	France	168
 22 oz Water Bottle	Detroit	United States	10075
SPF-15 Slim & Slender Lip Balm	Sunnyvale	United States	3682
 Cam Outdoor Security Camera - USA	San Francisco	United States	2719
 Cam Indoor Security Camera - USA	Sunnyvale	United States	2139
 Cam Indoor Security Camera - USA	not available in demo dataset	United States	2139
Four Color Retractable Pen	not available in demo dataset	United States	2002
 Learning Thermostat 3rd Gen-USA - Stainless Steel	Chicago	United States	1886
 Learning Thermostat 3rd Gen-USA - Stainless Steel	Mountain View	United States	1886
 Learning Thermostat 3rd Gen-USA - Stainless Steel	Nashville	United States	1886
 Learning Thermostat 3rd Gen-USA - Stainless Steel	not available in demo dataset	United States	1886
 Sunglasses	not available in demo dataset	United States	1573
 Sunglasses	Chicago	United States	1046
 Laptop and Cell Phone Stickers	Irvine	United States	1033
 Laptop and Cell Phone Stickers	not available in demo dataset	United States	1033
 Learning Thermostat 3rd Gen-USA - White	Palo Alto	United States	849
Red Spiral  Notebook	Salem	United States	316
 Men's Vintage Badge Tee Sage	Mountain View	United States	193
 Men's  Zip Hoodie	New York	United States	90
 Men's  Zip Hoodie	San Jose	United States	90
 Men's 100% Cotton Short Sleeve Hero Tee Black	Austin	United States	90
 Bongo Cupholder Bluetooth Speaker	not available in demo dataset	United States	85
 Mobile Phone Vent Mount	Mountain View	United States	68
 Mood Original Window Decal	not available in demo dataset	United States	63
 Men's Bike Short Sleeve Tee Charcoal	Mountain View	United States	41
 Womens 3/4 Sleeve Baseball Raglan Heather/Black	Chicago	United States	23
 Men's Short Sleeve Hero Tee Charcoal	not available in demo dataset	United States	17
 Men's Short Sleeve Badge Tee Charcoal	Columbus	United States	5
 Men's Airflow 1/4 Zip Pullover Lapis	not available in demo dataset	United States	3![image](https://github.com/oyebolakolapo/LHL_Project_One_Kolapo/assets/40770957/31607560-7137-4411-91ce-78d11a7198a2)



**Question 5: Can we summarize the impact of revenue generated from each city/country?**

SQL Queries:
SELECT city, country, totaltransactionrevenue, products.stocklevel
FROM all_sessions
INNER JOIN products ON all_sessions.productssku = products.productssku
WHERE totaltransactionrevenue IS NOT NULL
GROUP BY city, country, totaltransactionrevenue, products.stocklevel
ORDER BY products.stocklevel DESC


Answer:
No specific patterns were observed between totaltransactionrevue and stocklevel
city	country	totaltransactionrevenue	stocklevel
San Francisco	United States	202000000	4683
Sunnyvale	United States	649240000	4069
Sunnyvale	United States	200000000	2615
Sydney	Australia	358000000	2615
not available in demo dataset	United States	124000000	2615
Chicago	United States	306000000	2525
Mountain View	United States	154000000	2525
Nashville	United States	157000000	2525
not available in demo dataset	United States	391000000	2525
not available in demo dataset	United States	60000000	2086
Chicago	United States	123940000	1195
Palo Alto	United States	151000000	1142
Mountain View	United States	26820000	277
San Jose	United States	108380000	156
Austin	United States	35780000	148
Mountain View	United States	8980000	129
not available in demo dataset	United States	1005500000	115
Mountain View	United States	16990000	70
not available in demo dataset	United States	9960000	66
not available in demo dataset	United States	29970000	33
Columbus	United States	21990000	9![image](https://github.com/oyebolakolapo/LHL_Project_One_Kolapo/assets/40770957/d139bcc9-9e5c-49df-8276-f060759ca46d)






