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
--We need information "orderedquantity" from products table & "fullvisitorid", "city" and "country" from all_sessions table
--To JOIN table "products" and table "all_sessions" at sku column which was named productsku in all_sessions,
--we will rename productsku to sku for consistency.

ALTER TABLE products 
RENAME COLUMN sku TO productsku;

--Then we will FULL JOIN all_sessions table with products table

SELECT all_sessions.city, all_sessions.country, avg (products.orderedquantity) AS avgnumberofproducts
FROM all_sessions
FULL JOIN products
ON all_sessions.productsku = products.productsku
GROUP BY city, country
ORDER By city, country

Answer:
city	country	avgnumberofproducts
(not set)	(not set)	551.2352941
(not set)	Bahamas	917
(not set)	Bangladesh	272.9285714
(not set)	Belize	NULL
(not set)	Bosnia & Herzegovina	1148
(not set)	Brazil	433
(not set)	Canada	183
(not set)	C√¥te d‚ÄôIvoire	3786
(not set)	Dominican Republic	3
(not set)	Greece	114.1428571
(not set)	Hong Kong	482.4375
(not set)	Iceland	0
(not set)	India	691.2058824
(not set)	Indonesia	1360
(not set)	Japan	93.25
(not set)	Kosovo	433
(not set)	Latvia	935
(not set)	Nepal	212
(not set)	Netherlands	NULL
(not set)	Palestine	155
(not set)	Panama	2
(not set)	Peru	347.1428571
(not set)	Philippines	1351
(not set)	Puerto Rico	3
(not set)	R√©union	2538
(not set)	San Marino	757
(not set)	Serbia	513.5
(not set)	Singapore	395.1153846
(not set)	Sint Maarten	1100
(not set)	Sri Lanka	3
(not set)	Sudan	NULL
(not set)	Switzerland	1100
(not set)	Taiwan	842.6055046
(not set)	Thailand	73
(not set)	Trinidad & Tobago	1379.5
(not set)	United Kingdom	87.66666667
(not set)	United States	363.9
Adelaide	Australia	54
Ahmedabad	India	364.6363636
Akron	United States	15
Alexandria	Egypt	NULL
Amsterdam	Netherlands	390.4
Amsterdam	United States	8
Am√£	Jordan	NULL
Ann Arbor	United States	290.5609756
Antalya	Turkey	0
Antwerp	Belgium	134.5
Appleton	United States	66
Ashburn	United States	187.5
Asuncion	Paraguay	15
Athens	Greece	1088.4
Atlanta	United States	483.0877193
Auckland	New Zealand	52
Austin	United States	570.6914894
Avon	United States	330.5
Bandung	Indonesia	53
Bangkok	Thailand	610.3461538
Bangkok	United States	7
Barcelona	Spain	241.5294118
Beijing	China	16
Belgrade	Serbia	NULL
Bellflower	United States	3786
Bellingham	United States	2836
Belo Horizonte	Brazil	1184
Bengaluru	India	463.4307692
Berkeley	United States	25
Berlin	Germany	708.7692308
Bhubaneswar	India	499
Bilbao	Spain	13.5
Bogota	Colombia	488
Bordeaux	France	0
Boston	United States	313.3157895
Boulder	United States	361
Bratislava	Slovakia	0
Brisbane	Australia	274.5
Brno	Czechia	1548
Brussels	Belgium	62
Bucharest	Romania	697.4444444
Budapest	Hungary	184.1666667
Buenos Aires	Argentina	434.5
Burnaby	Canada	200.6666667
Calgary	Canada	472.2
Cambridge	United States	627.125
Cape Town	South Africa	25
Chandigarh	India	15
Charlotte	United States	749.1333333
Charlottetown	Canada	NULL
Chennai	India	497.1969697
Chicago	United States	647.2916667
Chico	United States	22
Chiyoda	Japan	0
Chuo	Japan	65
Cluj-Napoca	Romania	62
Colombo	Sri Lanka	138.6666667
Columbia	United States	154
Columbus	United States	8.5
Copenhagen	Denmark	61.5
Cork	Ireland	3786
Council Bluffs	United States	7589
Courbevoie	France	348
Coventry	United Kingdom	22
Culiacan	Mexico	220
Cupertino	United States	466.7
Dallas	United States	503.2758621
Denver	United States	355.8333333
Detroit	United States	2748
Doha	Qatar	62
Druid Hills	United States	269
Dubai	United Arab Emirates	798.1428571
Dublin	Ireland	657.4
Dublin	Netherlands	844
East Lansing	United States	66
Eau Claire	United States	59.63636364
Edmonton	Canada	569.5
Egham	United Kingdom	50
El Paso	United States	2
Esbjerg	Denmark	NULL
Forest Park	United States	5
Fort Worth	United States	0
Fortaleza	Brazil	22
Frankfurt	Germany	65
Fremont	United States	401.5
Ghent	Belgium	1351
Glasgow	United Kingdom	183
Goose Creek	United States	168
Gothenburg	Sweden	NULL
Greer	United States	26
Gurgaon	India	1335.857143
Hamburg	Germany	437.0909091
Hanoi	Vietnam	347
Hayward	United States	137
Helsinki	Finland	31
Ho Chi Minh City	Vietnam	378.3333333
Hong Kong	Hong Kong	568.875
Hong Kong	United States	363
Houston	United States	380.25
Hyderabad	India	602.3269231
Iasi	Romania	79
Indianapolis	United States	769
Indore	India	689
Ipoh	Malaysia	362
Irvine	United States	379.8888889
Istanbul	Hungary	363
Istanbul	Turkey	420.6818182
Izmir	Turkey	58
Jacksonville	United States	326.5
Jaipur	India	339.5
Jakarta	Indonesia	347.7826087
Jersey City	United States	18.33333333
Johnson City	United States	NULL
Kalamazoo	United States	403
Kansas City	United States	4
Karachi	Pakistan	428
Kharagpur	India	46
Kharkiv	Ukraine	51
Kiev	Ukraine	400.5625
Kirkland	United States	847.7179487
Kitchener	Canada	321.4
Kolkata	India	593.2222222
Kovrov	Russia	58
Krakow	Poland	NULL
Kuala Lumpur	Malaysia	384.5
La Victoria	Peru	465.25
LaFayette	United States	15
Lahore	Pakistan	218
Lake Oswego	United States	215
Las Vegas	United States	26.66666667
Lisbon	Portugal	299
London	United Kingdom	501.2093023
London	United States	10.66666667
Longtan District	Taiwan	845
Los Angeles	Australia	917
Los Angeles	United States	401.2222222
Lucknow	India	33
Madison	United States	92
Madrid	Spain	1286.466667
Makati	Philippines	51.5
Manchester	United Kingdom	50.5
Manila	Philippines	128.75
Maracaibo	Venezuela	119.5
Marlboro	United States	0
Marseille	France	31
Medellin	Colombia	208
Melbourne	Australia	659.375
Menlo Park	United States	791
Mexico City	Mexico	723.375
Mexico City	United States	160
Milan	Italy	1091.545455
Milpitas	United States	66.375
Minato	Japan	1033.69697
Minneapolis	United States	70
Mississauga	Canada	1305.25
Monterrey	Mexico	393
Montevideo	Uruguay	292.5
Montreal	Canada	313.8947368
Montreuil	France	726.5
Moscow	Russia	1291.8
Mountain View	Australia	33
Mountain View	Japan	151
Mountain View	United States	576.6178536
Mumbai	India	470.3061224
Munich	Germany	865.2857143
Nagoya	Japan	22
Nairobi	Kenya	6
Nanded	India	53
Nashville	United States	1886
Neipu Township	Taiwan	58
New Delhi	India	487.6944444
New York	Canada	178
New York	United States	431.9614679
Nice	France	NULL
Norfolk	United States	102
Oakland	United States	445.4285714
Odessa	Ukraine	NULL
Orlando	United States	100.1666667
Osaka	Japan	434.3333333
Oslo	Norway	40
Ottawa	Canada	25.5
Oviedo	United States	260
Oxford	United Kingdom	183
Palo Alto	United States	703.4367816
Panama City	United States	0
Paris	France	352.8837209
Paris	United States	6
Parsippany-Troy Hills	United States	18
Patna	India	327
Perth	Australia	1035.8
Petaling Jaya	Malaysia	53.5
Philadelphia	United States	315
Phoenix	United States	694.8333333
Piscataway Township	United States	40
Pittsburgh	United States	533.7272727
Pleasanton	United States	330
Portland	United States	15
Poznan	Poland	73.5
Pozuelo de Alarcon	Spain	541.3333333
Prague	Czechia	1216.5
Pune	India	386.5555556
Quebec City	Canada	578.1428571
Quezon City	Philippines	66.83333333
Quimper	France	NULL
Raleigh	United States	NULL
Redmond	United States	661.125
Redwood City	United States	435.1666667
Rexburg	United States	308.6666667
Richardson	United States	185
Rio de Janeiro	Brazil	179.6666667
Riyadh	Saudi Arabia	1138
Rome	Italy	1310.4
Rosario	Argentina	433
Rotterdam	Netherlands	0
Sacramento	United States	299
Saint Petersburg	Russia	1106.75
Sakai	Japan	1148
Salem	United States	446.275
Salford	United Kingdom	171
San Antonio	United States	368.8571429
San Bruno	United States	1106.428571
San Diego	United States	1093.52381
San Francisco	France	499
San Francisco	Japan	65
San Francisco	United States	505.0257069
San Jose	United States	468.2216981
San Mateo	United States	36
San Salvador	El Salvador	49
Sandton	South Africa	183
Santa Clara	United States	826.8275862
Santa Fe	Argentina	1932.5
Santa Monica	United States	276
Santiago	Chile	3607
Sao Paulo	Brazil	826.6785714
Sapporo	Japan	12
Seattle	United States	478.0280374
Seoul	South Korea	670.5454545
Sherbrooke	Canada	812.6666667
Shibuya	Japan	152
Shinjuku	Japan	565.2857143
Singapore	France	433
Singapore	Singapore	667.1891892
Skopje	Macedonia (FYROM)	NULL
South El Monte	United States	137
South San Francisco	United States	159.5
St. John's	Canada	34
St. Louis	United States	13.5
Stanford	United States	178
Stockholm	Sweden	163.4666667
Stuttgart	Germany	214
Sunnyvale	United States	491.9389068
Sydney	Australia	396.0909091
Taguig	Philippines	355.4285714
Tampa	United States	168
Tel Aviv-Yafo	Israel	547.7567568
Tempe	United States	447.25
The Dalles	United States	516.5
Thessaloniki	Greece	171.5
Timisoara	Romania	344
Toronto	Canada	570.4678899
Toronto	United States	168
University Park	United States	215
Vancouver	Canada	395
Vancouver	United States	0
Vienna	Austria	228.5
Villeneuve-d'Ascq	France	230
Vilnius	Lithuania	40
Vladivostok	Russia	551
Warsaw	Poland	463.5217391
Washington	United States	191.1111111
Waterloo	Canada	8
Watford	United Kingdom	0
Wellesley	United States	269
Westlake Village	United States	0
Westville	South Africa	2299
Wrexham	United Kingdom	1033
Wroclaw	Poland	NULL
Yokohama	Japan	91.83333333
Yokohama	United States	25
Zagreb	Croatia	54
Zhongli District	Taiwan	1492
Zurich	Switzerland	399.6666667
not available in demo dataset	(not set)	0
not available in demo dataset	Albania	510.3333333
not available in demo dataset	Algeria	720.5
not available in demo dataset	Argentina	344.8333333
not available in demo dataset	Armenia	1351
not available in demo dataset	Australia	550.4927536
not available in demo dataset	Austria	331.5862069
not available in demo dataset	Bahamas	79
not available in demo dataset	Bahrain	226.3333333
not available in demo dataset	Bangladesh	217.8823529
not available in demo dataset	Barbados	25
not available in demo dataset	Belarus	231
not available in demo dataset	Belgium	237.0178571
not available in demo dataset	Bolivia	90
not available in demo dataset	Bosnia & Herzegovina	6
not available in demo dataset	Botswana	215
not available in demo dataset	Brazil	538.1702128
not available in demo dataset	Brunei	45.5
not available in demo dataset	Bulgaria	1231.727273
not available in demo dataset	Cambodia	362.2
not available in demo dataset	Canada	491.0811518
not available in demo dataset	Chile	261.8
not available in demo dataset	China	229
not available in demo dataset	Colombia	411.7931034
not available in demo dataset	Costa Rica	573.4
not available in demo dataset	Croatia	516.5384615
not available in demo dataset	Cyprus	78.25
not available in demo dataset	Czechia	605.4428571
not available in demo dataset	C√¥te d‚ÄôIvoire	1309.333333
not available in demo dataset	Denmark	598.7037037
not available in demo dataset	Dominican Republic	912.2
not available in demo dataset	Ecuador	136.7272727
not available in demo dataset	Egypt	322.4545455
not available in demo dataset	El Salvador	14
not available in demo dataset	Estonia	151.2
not available in demo dataset	Ethiopia	1239
not available in demo dataset	Finland	337.3333333
not available in demo dataset	France	447.2357143
not available in demo dataset	French Polynesia	NULL
not available in demo dataset	Georgia	2506.4
not available in demo dataset	Germany	466.5807692
not available in demo dataset	Ghana	197
not available in demo dataset	Gibraltar	79
not available in demo dataset	Greece	443.4642857
not available in demo dataset	Guatemala	603.2222222
not available in demo dataset	Haiti	1
not available in demo dataset	Honduras	680.5
not available in demo dataset	Hong Kong	1555
not available in demo dataset	Hungary	383.4285714
not available in demo dataset	Iceland	NULL
not available in demo dataset	India	421.5954198
not available in demo dataset	Indonesia	535.0185185
not available in demo dataset	Iraq	150.6666667
not available in demo dataset	Ireland	354.3793103
not available in demo dataset	Israel	783.1666667
not available in demo dataset	Italy	697.8857143
not available in demo dataset	Jamaica	178
not available in demo dataset	Japan	509.262069
not available in demo dataset	Jersey	59
not available in demo dataset	Jordan	295
not available in demo dataset	Kazakhstan	617
not available in demo dataset	Kenya	27
not available in demo dataset	Kuwait	221.1666667
not available in demo dataset	Kyrgyzstan	123
not available in demo dataset	Laos	886.6666667
not available in demo dataset	Latvia	309.4285714
not available in demo dataset	Lebanon	935
not available in demo dataset	Lithuania	511.3571429
not available in demo dataset	Luxembourg	12
not available in demo dataset	Macau	701.6666667
not available in demo dataset	Macedonia (FYROM)	505
not available in demo dataset	Malaysia	416.8709677
not available in demo dataset	Maldives	33
not available in demo dataset	Mali	3786
not available in demo dataset	Malta	469.5
not available in demo dataset	Martinique	138.5
not available in demo dataset	Mauritius	104.5
not available in demo dataset	Mexico	560.1896552
not available in demo dataset	Moldova	1893
not available in demo dataset	Montenegro	3786
not available in demo dataset	Morocco	1203.428571
not available in demo dataset	Myanmar (Burma)	543.6666667
not available in demo dataset	Nepal	746
not available in demo dataset	Netherlands	448.8846154
not available in demo dataset	New Zealand	464.2272727
not available in demo dataset	Nicaragua	268
not available in demo dataset	Nigeria	280.1428571
not available in demo dataset	Norway	397.4827586
not available in demo dataset	Oman	1330
not available in demo dataset	Pakistan	539.7179487
not available in demo dataset	Panama	630.5714286
not available in demo dataset	Papua New Guinea	2558
not available in demo dataset	Peru	743.8181818
not available in demo dataset	Philippines	547.0923077
not available in demo dataset	Poland	368.1162791
not available in demo dataset	Portugal	1265.9
not available in demo dataset	Puerto Rico	1319.2
not available in demo dataset	Qatar	31
not available in demo dataset	Romania	847.15625
not available in demo dataset	Russia	506.9850746
not available in demo dataset	Rwanda	0
not available in demo dataset	Saudi Arabia	277.3333333
not available in demo dataset	Serbia	618.3636364
not available in demo dataset	Singapore	364.8571429
not available in demo dataset	Slovakia	525.1428571
not available in demo dataset	Slovenia	553.875
not available in demo dataset	Somalia	50
not available in demo dataset	South Africa	203.5909091
not available in demo dataset	South Korea	486.7391304
not available in demo dataset	Spain	417.6818182
not available in demo dataset	Sri Lanka	427.5454545
not available in demo dataset	Sudan	935
not available in demo dataset	Sweden	366.7446809
not available in demo dataset	Switzerland	396.6
not available in demo dataset	Taiwan	409.2666667
not available in demo dataset	Tanzania	1429
not available in demo dataset	Thailand	508.6315789
not available in demo dataset	Tunisia	748
not available in demo dataset	Turkey	350.2424242
not available in demo dataset	Uganda	1033
not available in demo dataset	Ukraine	587.5142857
not available in demo dataset	United Arab Emirates	316.2
not available in demo dataset	United Kingdom	610.0225564
not available in demo dataset	United States	506.3745875
not available in demo dataset	Uruguay	384.3333333
not available in demo dataset	Venezuela	359
not available in demo dataset	Vietnam	538
not available in demo dataset	Zimbabwe	844
NULL	NULL	30.6571835![image](https://github.com/oyebolakolapo/LHL_Project_One_Kolapo/assets/40770957/3c5a247a-04fc-4433-8e85-fafe4c712112)




**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:



Answer:





**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:



Answer:





**Question 5: Can we summarize the impact of revenue generated from each city/country?**

SQL Queries:



Answer:







