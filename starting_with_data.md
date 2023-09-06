Question 1: 
--Part 4: Starting with Data
--Consider the data you have available to you. You can use the data to: find all duplicate records, find the total number of unique, visitors (fullVisitorID), find the total number of unique visitors by referring sites, find each unique product viewed by each visitor, compute the percentage of visitors to the site that actually makes a purchase

SQL Queries:
SELECT products.productssku, products.name, COUNT (*)
FROM products
GROUP BY products.productssku, products.name
HAVING COUNT (products.productssku) > 1

Answer: 
productssku	name	count
GGOEGADJ059715	 Men's Quilted Insulated Vest Battleship Grey	2
9181149	Gift Card - $25.00	2
GGOEGATB060613	 Women's Convertible Vest-Jacket Black	2
GGOEGAUC057713	 Women's Performance Golf Polo Blue	2
GGOEGAAJ032713	 Men's Long & Lean Tee Grey	2
GGOEGAXR065130	 Toddler Short Sleeve Tee Red	2
GGOEAAAP081215	Android Men's Take Charge Short Sleeve Tee Purple	2
GGOEGAQB036016	 Women's Fleece Hoodie	2
GGOEGAEA030414	 Womens 3/4 Sleeve Baseball Raglan Heather/Black	2
GGOEGAYC068326	 Youth Short Sleeve T-shirt Royal Blue	2
9182587	Android Women's Fleece Hoodie	2
9180770	Yoga Mat Blue	2
GGOEAAXC066428	Android Toddler Short Sleeve T-shirt Aqua	2
GGOEGAPB058214	 Women's Lightweight Microfleece Jacket	2
GGOEYAQB073216	 Women's Fleece Hoodie Black	2
GGOEGADB059615	 Men's Quilted Insulated Vest Black	2
GGOEGAEA030415	 Womens 3/4 Sleeve Baseball Raglan Heather/Black	2
GGOEGEHQ072499	 2200mAh Micro Charger	2
9182706	Android Stretch Fit Hat	2
GGOEGALL074614	 Women's Short Sleeve Badge Tee Navy	2
GGOEAXXX0812	Android Men's Take Charge Short Sleeve Tee Purple	2
GGOEWAAJ082817	 Men's Short Sleeve Tee	2
9182752	 Men's Short Sleeve Performance Badge Tee Charcoal	2
GGOEGXXX0806	 Men's Bike Short Sleeve Tee Charcoal	2
GGOEYAYR068624	 Youth Short Sleeve Tee Red	2
GGOEAAEJ030915	Android Women's Long Sleeve Blended Cardigan Grey	2
GGOEAAWT061749	Android Onesie Gold	2
GGOEGALJ036414	 Women's Tee Grey	2
9184721	BLM Sweatshirt	2
GGOEGAAR010717	 Men's 100% Cotton Short Sleeve Hero Tee Red	2
GGOEGAPB058213	 Women's Lightweight Microfleece Jacket	2
GGOENEBB081499	 Cam Indoor Security Camera - CA	2
GGOEGAEJ028116	 Women's Short Sleeve Badge Tee Grey	2
GGOEGAQB036013	 Women's Fleece Hoodie	2
GGOEGAAQ010413	 Men's 100% Cotton Short Sleeve Hero Tee White	2
GGOEGAAX0570	 Men's Short Sleeve Performance Badge Tee Charcoal	2
GGOEGAAX0625	Android Infant Short Sleeve Tee Pewter	2
GGOEAAAB034816	Android BTTF Cosmos Graphic Tee	2
GGOEGAAQ057213	 Men's Colorblock Tee White/Heather	2
GGOEGHPB080410	 5-Panel Snapback Cap	2
GGOEGALB036515	 Women's Scoop Neck Tee Black	2
9180862	 Screen Cleaning Cloth	2
GGOEGEVA022399	Micro Wireless Earbud	2
9184707	 Women's Typography Short Sleeve Tee	2
GGOEYOBR078599	 Luggage Tag	2
GGOEGALP036315	 Women's Long Sleeve Tee Lavender	2
GGOEGAAJ073416	 Men's Short Sleeve Hero Tee Heather	2
9184733	 Learning Thermostat 3rd Gen-USA - White	2
GGOEAAAJ080817	Android Men's Engineer Short Sleeve Tee Charcoal	2
GGOEGAPB058613	 Women's Yoga Jacket Black	2
GGOEGDHQ014899	20 oz Stainless Steel Insulated Tumbler	2
GGOEGAAX0590	 Men's Short Sleeve Performance Badge Tee Navy	2
GGOEGALL074616	 Women's Short Sleeve Badge Tee Navy	2
GGOEYAAQ031715	 Men's Short Sleeve Hero Tee White	2
GGOEYAAJ032517	 Men's Short Sleeve Hero Tee Charcoal	2
GGOEGDHC018299	 22 oz Water Bottle	2
9182816	 Infant Zip Hood Royal Blue	2
GGOEGAYQ068925	 Youth Girl Hoodie	2
GGOEGHGR019499	 Sunglasses	2
9180806	Clip-on Compact Charger	2
GGOEGAAX0659	 Toddler Raglan Shirt Blue Heather/Navy	2
GGOEWXXX0834	 Women's Typography Short Sleeve Tee	2
GGOEGALQ036615	 Women's Scoop Neck Tee White	2
GGOEGALJ060113	 Women's Short Sleeve Performance Tee Pewter	2
GGOEWAAJ082815	 Men's Short Sleeve Tee	2
GGOEGAAX0589	 Men's Short Sleeve Performance Badge Tee Black	2
GGOEGALP034317	 Women's Vintage Hero Tee Lavender	2
GGOEGAPJ058012	 Women's 1/4 Zip Jacket Charcoal	2
GGOEGOCT019199	Red Spiral  Notebook	2
GGOEGHPB003410	 Snapback Hat Black	2
9183241	25L Classic Rucksack	2
GGOEAAAL081113	Android Men's Pep Rally Short Sleeve Tee Navy	2
GGOEGGCX056199	Gift Card- $100.00	2
GGOEGAAX0628	 Infant Zip Hood Royal Blue	2
GGOEAAEJ030913	Android Women's Long Sleeve Blended Cardigan Grey	2
GGOEGAEC029113	 Women's Short Sleeve Hero Tee Sky Blue	2
GGOEGALJ057915	 Women's Short Sleeve Performance Tee Charcoal	2
GGOEGADB059613	 Men's Quilted Insulated Vest Black	2
GGOEGAPJ058016	 Women's 1/4 Zip Jacket Charcoal	2
GGOEGAAC032116	 Men's Short Sleeve Hero Tee Light Blue	2
9181148	Gift Card- $100.00	2
GGOEGAAB058913	 Men's Short Sleeve Performance Badge Tee Black	2
GGOEYAEJ029515	 Women's Short Sleeve Tri-blend Badge Tee Charcoal	2
GGOEYAEB028415	Women's  Short Sleeve Hero Tee Black	2
GGOEGESC014699	Aluminum Handy Emergency Flashlight	2
GGOEGCBC074299	 Device Stand	2
GGOEGAAJ059113	 Men's Short Sleeve Performance Badge Tee Pewter	2
GGOEGATC060316	 Women's 1/4 Zip Performance Pullover Two-Tone Blue	2
9182559	Android Men's Vintage Henley	2
GGOEGXXX0845	BLM Sweatshirt	2
GGOEYAEJ029014	 Women's Short Sleeve Hero Tee Charcoal	2
GGOEGAPB057516	Women's Weatherblock Shell Jacket Black	2
GGOEGBMB073799	 Zipper-front Sports Bag	2
GGOEGOAJ021599	Gunmetal Roller Ball Pen	2
GGOEGAAX0313	 Tri-blend Hoodie Grey	2
GGOEGAWQ062948	 Baby Essentials Set	2
9180833	Rubber Grip Ballpoint Pen 4 Pack	2
9181572	Android Wool Heather Cap Heather/Black	2
9182764	 Women's Convertible Vest-Jacket Black	2
GGOEAXXX0811	Android Men's Pep Rally Short Sleeve Tee Navy	2
GGOEGCBB074199	 Car Clip Phone Holder	2
GGOEGALB036517	 Women's Scoop Neck Tee Black	2
GGOEAHPJ004213	Android Stretch Fit Hat S/M	2
GGOEGAWR061154	 Onesie Red	2
GGOEAAEJ028213	Android Women's Short Sleeve Badge Tee Dark Heather	2
GGOEGAEB027813	 Women's Short Sleeve Hero Tee Black	2
GGOEGAAJ032716	 Men's Long & Lean Tee Grey	2
GGOEGAAX0781	 Leather Journal	2
9182828	 Toddler Short Sleeve T-shirt Royal Blue	2
9184683	 Women's Short Sleeve Tee	2
GGOEGAAX0326	 Men's Short Sleeve Badge Tee Charcoal	2
GGOEGBJC019999	Collapsible Shopping Bag	2
GGOEAAEJ033416	Android Men's Long Sleeve Badge Crew Tee Heather	2
9180767	 Slim Utility Travel Bag	2
GGOEAAEH035214	Android Men's Vintage Henley	2
GGOEGFYQ016599	Foam Can and Bottle Cooler	2
GGOEGAEJ029913	 Women's V-Neck Tee Charcoal	2
GGOEGAEB084514	BLM Sweatshirt	2
GGOEGAAX0619	 Infant Short Sleeve Tee Royal Blue	2
GGOEGBRB013899	 Laptop Backpack	2
GGOEGALQ036614	 Women's Scoop Neck Tee White	2
9180782	Seat Pack Organizer	2
GGOEGAEA030413	 Womens 3/4 Sleeve Baseball Raglan Heather/Black	2
GGOEGAYB068026	 Youth Baseball Raglan Heather/Black	2
9184720	 Women's Short Sleeve Hero Tee Sky Blue	2
GGOEGAYH068425	 Youth Short Sleeve T-shirt Green	2
GGOEGAAJ057018	 Men's Short Sleeve Performance Badge Tee Charcoal	2
GGOEGKWR060810	 Bib Red	2
GGOEGADB059616	 Men's Quilted Insulated Vest Black	2
GGOEGAAQ010415	 Men's 100% Cotton Short Sleeve Hero Tee White	2
GGOEGETB023799	 Power Bank	2
GGOEAAWT061748	Android Onesie Gold	2
9180748	Android Lunch Kit	2
GGOEGAAX0341	 Women's Vintage Hero Tee Black	2
9182772	 Women's Performance Full Zip Jacket Black	2
9182999	 Bongo Cupholder Bluetooth Speaker	2
9182785	 Women's Lightweight Microfleece Jacket	2
GGOEAAAC080916	Android Lifted Men's Short Sleeve Tee Blue	2
9182746	 Men's Quilted Insulated Vest Battleship Grey	2
GGOEGAAQ033914	 Men's Vintage Badge Tee White	2
GGOEGAAX0686	 Youth Short Sleeve Tee Red	2
9184698	 Mood Ninja Window Decal	2
GGOEWEBB082699	 Mobile Phone Vent Mount	2
9183203	 Device Holder Sticky Pad	2
9183239	25L Classic Rucksack	2
GGOEGAAX0671	 Toddler Short Sleeve Tee White	2
GGOEGAEJ035316	 Vintage Henley Grey/Black	2
GGOEGAAX0168	 Pet Feeding Mat	2
GGOEGAAC032115	 Men's Short Sleeve Hero Tee Light Blue	2
9182719	 Men's Short Sleeve Hero Tee Charcoal	2
GGOEGATB060416	 Women's Quilted Insulated Vest Black	2
GGOEGALP034314	 Women's Vintage Hero Tee Lavender	2
GGOEGALJ036416	 Women's Tee Grey	2
GGOEGAAX0731	 Men's Fleece Hoodie Black	2
9184695	 Baby on Board Window Decal	2
GGOEGADB057318	 Men's Lightweight Microfleece Jacket Black	2
GGOEYAWJ061453	 Onesie Heather	2
9182781	 Women's Short Sleeve Hero Tee Black	2
GGOEGAEJ028113	 Women's Short Sleeve Badge Tee Grey	2
GGOEGOLC013299	Spiral Notebook and Pen Set	2
GGOEGAAH034013	 Men's Vintage Badge Tee Sage	2
GGOEGAAQ010417	 Men's 100% Cotton Short Sleeve Hero Tee White	2
GGOEGAAX0320	Android Men's Short Sleeve Hero Tee White	2
9182750	 Men's Performance 1/4 Zip Pullover Heather/Black	2
GGOEGAAX0627	 Infant Zip Hood Pink	2
GGOEGAAX0577	 Women's Performance Golf Polo Blue	2
GGOEYFKQ020699	 Custom Decals	2
GGOEAAAC080913	Android Lifted Men's Short Sleeve Tee Blue	2
GGOEGAAX0730	 Men's Performance Hero Tee Gunmetal	2
GGOEAOBH078799	Android Luggage Tag	2
GGOEGAAX0355	 Men's Vintage Tank	2
9182179	Android Women's Short Sleeve Badge Tee Dark Heather	2
GGOEYAWJ061450	 Onesie Heather	2
GGOEGAAX0593	 Men's Airflow 1/4 Zip Pullover Lapis	2
GGOEWFKA082999	 Baby on Board Window Decal	2
GGOEGAWH061348	 Onesie Green	2
GGOEGAAX0573	 Men's Lightweight Microfleece Jacket Black	2
GGOEGALQ034217	 Women's Vintage Hero Tee White	2
9183219	 Leather Journal	2
GGOEGATB060616	 Women's Convertible Vest-Jacket Black	2
GGOEGAEJ028016	 Women's Short Sleeve Hero Tee Grey	2
GGOEGAYQ069056	 Youth Short Sleeve Tee White	2
GGOEGAPB058216	 Women's Lightweight Microfleece Jacket	2
GGOEGADC059316	 Men's Airflow 1/4 Zip Pullover Lapis	2
9180769	 Laptop Backpack	2
GGOEGAAX0283	Android Women's Short Sleeve Hero Tee Black	2
9182383	 Men's Watershed Full Zip Hoodie Grey	2
9180820	 Doodle Decal	2
GGOEGAAX0610	 Onesie Red/Graphite	2
GGOEGAEJ028015	 Women's Short Sleeve Hero Tee Grey	2
GGOEGAAJ080613	 Men's Bike Short Sleeve Tee Charcoal	2
GGOEGAPB057514	Women's Weatherblock Shell Jacket Black	2
9182722	 Men's 100% Cotton Short Sleeve Hero Tee Navy	2
GGOEGADJ057115	 Men's Performance 1/4 Zip Pullover Heather/Black	2
GGOEAAEJ033417	Android Men's Long Sleeve Badge Crew Tee Heather	2
GGOEGAYB068056	 Youth Baseball Raglan Heather/Black	2
GGOEAAWN062649	Android Infant Short Sleeve Tee Pink	2
GGOEGAAC032117	 Men's Short Sleeve Hero Tee Light Blue	2
GGOEGAAL010617	 Men's 100% Cotton Short Sleeve Hero Tee Navy	2
GGOEGAAX0363	 Women's Long Sleeve Tee Lavender	2
GGOEGATH060713	 Women's Convertible Vest-Jacket Sea Foam Green	2
9182714	 Men's Long Sleeve Raglan Ocean Blue	2
GGOEGAAX0661	 Toddler Short Sleeve Tee Red	2
9183240	25L Classic Rucksack	2
GGOEYAEJ029614	 Women's Short Sleeve Tri-blend Badge Tee Grey	2
GGOEGAXQ067130	 Toddler Short Sleeve Tee White	2
GGOEGAAX0578	 Women's Performance Full Zip Jacket Black	2
GGOEGAAJ080617	 Men's Bike Short Sleeve Tee Charcoal	2
9182575	Android Men's  Zip Hoodie	2
GGOEGOAQ012899	Ballpoint LED Light Pen	2
GGOEGAAX0350	 Men's Bayside Graphic Tee	2
GGOEGALJ060116	 Women's Short Sleeve Performance Tee Pewter	2
GGOEGAEJ028916	 Women's Short Sleeve Hero Dark Grey	2
GGOEGAAX0684	 Youth Short Sleeve T-shirt Green	2
GGOEGALJ034413	 Women's Vintage Hero Tee Platinum	2
GGOEGAAJ032815	 Men's Long & Lean Tee Charcoal	2
GGOEGCBC016999	 Pet Feeding Mat	2
9182774	 Women's Yoga Pants	2
GGOEAHPB076115	Android Stretch Fit Hat	2
GGOEGAXJ065755	 Toddler 1/4 Zip Fleece Pewter	2
GGOEGAAX0308	 Women's Long Sleeve Blended Cardigan Charcoal	2
GGOEGADJ059713	 Men's Quilted Insulated Vest Battleship Grey	2
9183000	 Pocket Bluetooth Speaker	2
GGOEGAAB033813	 Men's Vintage Badge Tee Black	2
GGOEGBRC021399	Yoga Mat Blue	2
GGOEGAAX0598	 Men's Convertible Vest-Jacket Pewter	2
GGOEYAFB073114	 Men's Fleece Hoodie Black	2
GGOEYAEJ029513	 Women's Short Sleeve Tri-blend Badge Tee Charcoal	2
GGOEAAEJ030914	Android Women's Long Sleeve Blended Cardigan Grey	2
GGOEGAXJ065555	 Toddler Short Sleeve T-shirt Grey	2
9182705	Android Men's Long & Lean Badge Tee Charcoal	2
9182743	 Men's Microfiber 1/4 Zip Pullover Blue/Indigo	2
GGOEAAWJ062550	Android Infant Short Sleeve Tee Pewter	2
GGOEGATB060614	 Women's Convertible Vest-Jacket Black	2
GGOEGAEJ029916	 Women's V-Neck Tee Charcoal	2
GGOEGAWR061148	 Onesie Red	2
GGOEGAER029717	 Women's Short Sleeve Hero Tee Red Heather	2
GGOEYAAB031815	 Men's Short Sleeve Hero Tee Black	2
GGOEGALP036313	 Women's Long Sleeve Tee Lavender	2
GGOEGAAQ033915	 Men's Vintage Badge Tee White	2
GGOEGBRD079699	25L Classic Rucksack	2
GGOEGAPB058612	 Women's Yoga Jacket Black	2
GGOEGDWR015799	Red Shine 15 oz Mug	2
GGOEGAEJ028014	 Women's Short Sleeve Hero Tee Grey	2
GGOEGAFB035814	 Men's  Zip Hoodie	2
GGOEGAPB057817	Women's Performance Full Zip Jacket Black	2
GGOEGAAX0098	7" Dog Frisbee	2
GGOEGCMB020932	Suitcase Organizer Cubes	2
9182909	 Collapsible Pet Bowl	2
GGOEAAEJ028214	Android Women's Short Sleeve Badge Tee Dark Heather	2
GGOEGAAX0734	 Men's Short Sleeve Hero Tee Heather	2
GGOEGADB059214	 Men's Airflow 1/4 Zip Pullover Black	2
9182773	 Women's Short Sleeve Performance Tee Charcoal	2
9180850	Ballpoint Stylus Pen	2
GGOEGALQ036613	 Women's Scoop Neck Tee White	2
GGOEGAWH061350	 Onesie Green	2
GGOEAAAJ031914	Android Men's Short Sleeve Hero Tee Heather	2
GGOEGBRP037599	Yoga Mat Purple	2
GGOEGAEB084517	BLM Sweatshirt	2
9180868	Crunch Noise Dog Toy	2
GGOENEBJ081899	 Learning Thermostat 3rd Gen - CA - Stainless Steel	2
GGOEGAAB033815	 Men's Vintage Badge Tee Black	2
GGOEGCVB072399	 Executive Umbrella	2
9183106	 Women's Performance Hero Tee Gunmetal	2
9183225	 Luggage Tag	2
GGOENEBQ081799	 Protect Smoke + CO White Wired Alarm - CA	2
GGOEGAAJ032615	 Men's Short Sleeve Badge Tee Charcoal	2
GGOEYAAJ032514	 Men's Short Sleeve Hero Tee Charcoal	2
GGOEGAWR061049	 Onesie Red/Graphite	2
GGOEGAAR010713	 Men's 100% Cotton Short Sleeve Hero Tee Red	2
GGOEYAFB073117	 Men's Fleece Hoodie Black	2
GGOEGAWH061349	 Onesie Green	2
GGOEGAAX0324	Android Men's Short Sleeve Tri-blend Hero Tee Grey	2
9183086	 Youth Girl Tee Green	2
GGOEAAAJ032913	Android Men's Long & Lean Badge Tee Charcoal	2
9184708	 Women's Typography Short Sleeve Tee	2
GGOEAAAB081014	Android Men's Outerstellar Short Sleeve Tee Black	2
GGOEAAFB035917	Android Men's  Zip Hoodie	2
GGOENEBQ081699	 Protect Smoke + CO White Battery Alarm - CA	2
GGOEGBPB021199	 Slim Utility Travel Bag	2
GGOEGATB060413	 Women's Quilted Insulated Vest Black	2
GGOEGAFB035815	 Men's  Zip Hoodie	2
GGOEGAYR068224	 Youth Short Sleeve Tee Red	2
GGOEGALJ072915	 Women's Performance Hero Tee Gunmetal	2
9180808	Basecamp Explorer Powerbank Flashlight	2
9180838	Metal Texture Roller Pen	2
GGOEGAAX0660	 Toddler Sports T-shirt Red	2
9182859	 Toddler Raglan Shirt Blue Heather/Navy	2
9182741	 Men's Airflow 1/4 Zip Pullover Lapis	2
GGOEGAWN062749	 Infant Zip Hood Pink	2
GGOEGHPJ080310	 Blackout Cap	2
GGOEGALB034117	 Women's Vintage Hero Tee Black	2
GGOEYAWJ061454	 Onesie Heather	2
GGOEGATB060213	 Women's 1/4 Zip Performance Pullover Black	2
9181139	Waterproof Backpack	2
GGOEGADB056915	 Men's Performance Full Zip Jacket Black	2
9182569	 Men's  Zip Hoodie	2
GGOEGAAX0361	Android Women's Fleece Hoodie	2
GGOEYOCR077799	 Hard Cover Journal	2
GGOEGADJ056814	 Men's Watershed Full Zip Hoodie Grey	2
GGOEYAWJ061448	 Onesie Heather	2
GGOEGAAB010517	 Men's 100% Cotton Short Sleeve Hero Tee Black	2
GGOEGAAJ073415	 Men's Short Sleeve Hero Tee Heather	2
GGOEGAXL065928	 Toddler Raglan Shirt Blue Heather/Navy	2
GGOEGAAX0340	 Men's Vintage Badge Tee Sage	2
GGOEGAAX0613	 Onesie Green	2
GGOEAAXN066330	Android Toddler Short Sleeve T-shirt Pink	2
GGOEAAEJ035714	Android Men's Vintage Tank	2
GGOEGAWQ062953	 Baby Essentials Set	2
GGOEGAWR061150	 Onesie Red	2
GGOEYAAJ033013	 Men's Long & Lean Tee Charcoal	2
GGOEGAAX0614	 Onesie Heather	2
GGOEYAEA035114	 Men's Vintage Henley	2
9182738	 Women's Long Sleeve Blended Cardigan Charcoal	2
GGOEAAAB081015	Android Men's Outerstellar Short Sleeve Tee Black	2
GGOEGAXC065628	 Toddler Hoodie Royal Blue	2
GGOEGAYL068125	 Youth Sports Tee Navy	2
GGOEAAQB036116	Android Women's Fleece Hoodie	2
GGOEGCBQ016499	SPF-15 Slim & Slender Lip Balm	2
GGOEGAXR066055	 Toddler Sports T-shirt Red	2
9182658	 Women's Short Sleeve Hero Tee Sky Blue	2
GGOEGAAJ032316	 Men's Short Sleeve Hero Tee Charcoal	2
GGOEGAAX0329	Android Men's Long & Lean Badge Tee Charcoal	2
GGOEGAYR068226	 Youth Short Sleeve Tee Red	2
9181573	 Snapback Hat Black	2
GGOEAAXN066355	Android Toddler Short Sleeve T-shirt Pink	2
GGOEGAEQ027915	 Women's Short Sleeve Hero Tee White	2
GGOEGALJ036413	 Women's Tee Grey	2
GGOEGAAJ059114	 Men's Short Sleeve Performance Badge Tee Pewter	2
GGOEGALJ073315	 Women's Short Sleeve Hero Tee Heather	2
GGOEGAXR065128	 Toddler Short Sleeve Tee Red	2
GGOEYAAJ033014	 Men's Long & Lean Tee Charcoal	2
GGOEYAQB073217	 Women's Fleece Hoodie Black	2
GGOEGAAX0278	 Women's Short Sleeve Hero Tee Black	2
GGOEGAEC029115	 Women's Short Sleeve Hero Tee Sky Blue	2
GGOEGAEJ030816	 Women's Long Sleeve Blended Cardigan Charcoal	2
GGOEGOCC077299	 RFID Journal	2
GGOEGAAJ032717	 Men's Long & Lean Tee Grey	2
GGOEGOAA017199	Rubber Grip Ballpoint Pen 4 Pack	2
GGOEGAWC061948	 Infant Short Sleeve Tee Royal Blue	2
GGOEGAEA030416	 Womens 3/4 Sleeve Baseball Raglan Heather/Black	2
9183222	 Leather Perforated Journal	2
GGOEGAAJ032614	 Men's Short Sleeve Badge Tee Charcoal	2
GGOEGALP036314	 Women's Long Sleeve Tee Lavender	2
GGOEAAAB034817	Android BTTF Cosmos Graphic Tee	2
GGOEGADB059614	 Men's Quilted Insulated Vest Black	2
GGOEGADB056615	Men's Weatherblock Shell Jacket Black	2
9182553	 Men's Vintage Henley	2
9183223	 Spiral Leather Journal	2
GGOEGALJ057914	 Women's Short Sleeve Performance Tee Charcoal	2
GGOEGAEJ029914	 Women's V-Neck Tee Charcoal	2
9183212	Android RFID Journal	2
9182873	Android Toddler Short Sleeve T-shirt Pink	2
GGOEAAAJ032417	Android Men's Short Sleeve Tri-blend Hero Tee Grey	2
9180811	Plastic Sliding Flashlight	2
GGOEGATC060315	 Women's 1/4 Zip Performance Pullover Two-Tone Blue	2
GGOEGAEC033115	 Men's Long Sleeve Raglan Ocean Blue	2
GGOEGOXQ016399	Badge Holder	2
GGOEAAAJ032914	Android Men's Long & Lean Badge Tee Charcoal	2
GGOEGADB056614	Men's Weatherblock Shell Jacket Black	2
GGOEGKAA019299	Switch Tone Color Crayon Pen	2
GGOEGADB057313	 Men's Lightweight Microfleece Jacket Black	2
GGOEGAAL010613	 Men's 100% Cotton Short Sleeve Hero Tee Navy	2
9182701	Android Men's Long Sleeve Badge Crew Tee Heather	2
GGOEAAWT061754	Android Onesie Gold	2
GGOEGAAX0689	 Youth Girl Hoodie	2
GGOEGALP036317	 Women's Long Sleeve Tee Lavender	2
GGOEGAAX0576	 Women's Softshell Jacket Black/Grey	2
GGOEGAAX0595	 Men's Microfiber 1/4 Zip Pullover Blue/Indigo	2
GGOEYAAB031813	 Men's Short Sleeve Hero Tee Black	2
GGOEAAAL081116	Android Men's Pep Rally Short Sleeve Tee Navy	2
GGOEGAXR065129	 Toddler Short Sleeve Tee Red	2
GGOEGAAX0351	 Men's Vintage Henley	2
GGOEWAEA083899	 Dress Socks	2
GGOEGAXQ067128	 Toddler Short Sleeve Tee White	2
GGOEGAAQ057216	 Men's Colorblock Tee White/Heather	2
9180813	 Tube Power Bank	2
GGOEGOBG023599	Colored Pencil Set	2
GGOEGALJ034417	 Women's Vintage Hero Tee Platinum	2
GGOEGADB056916	 Men's Performance Full Zip Jacket Black	2
GGOEGAAL010615	 Men's 100% Cotton Short Sleeve Hero Tee Navy	2
GGOEGALJ057913	 Women's Short Sleeve Performance Tee Charcoal	2
GGOEGAFB035817	 Men's  Zip Hoodie	2
GGOEGAAJ073016	 Men's Performance Hero Tee Gunmetal	2
GGOEGOCB078299	 Leather Journal-Black	2
GGOEGAAX0626	Android Infant Short Sleeve Tee Pink	2
GGOEGACB023699	Yoga Block	2
9182820	 Baby Essentials Set	2
GGOEGAAX0339	 Men's Vintage Badge Tee White	2
GGOEGALL074615	 Women's Short Sleeve Badge Tee Navy	2
GGOEGAEJ035313	 Vintage Henley Grey/Black	2
GGOEGADB056616	Men's Weatherblock Shell Jacket Black	2
GGOEGAAX0280	 Women's Short Sleeve Hero Tee Grey	2
GGOEGAAJ032314	 Men's Short Sleeve Hero Tee Charcoal	2
GGOEGAAX0690	 Youth Short Sleeve Tee White	2
GGOEGFAQ016699	Bottle Opener Clip	2
GGOEGALQ036617	 Women's Scoop Neck Tee White	2
GGOEAAAL081114	Android Men's Pep Rally Short Sleeve Tee Navy	2
GGOEGAAX0356	 Men's Vintage Tank	2
GGOEGAAR010714	 Men's 100% Cotton Short Sleeve Hero Tee Red	2
GGOEGAAL059013	 Men's Short Sleeve Performance Badge Tee Navy	2
GGOEGAAX0586	 Women's Yoga Jacket Black	2
GGOEAAEH035216	Android Men's Vintage Henley	2
9182740	 Men's Airflow 1/4 Zip Pullover Black	2
GGOEGFQB013799	Compact Selfie Stick	2
GGOEGAAX0566	 Men's Weatherblock Shell Jacket Black	2
GGOEGODR017799	Recycled Mouse Pad	2
9182903	Android Youth Short Sleeve T-shirt Pewter	2
GGOEAXXX0810	Android Men's Outerstellar Short Sleeve Tee Black	2
GGOEAXXX0833	Android Men's Paradise Short Sleeve Tee Olive	2
GGOEGAFB035813	 Men's  Zip Hoodie	2
GGOEAAWT061753	Android Onesie Gold	2
GGOEGALP034315	 Women's Vintage Hero Tee Lavender	2
GGOEGBRA037499	Waterproof Backpack	2
GGOEGAWR061048	 Onesie Red/Graphite	2
GGOEGATJ060513	 Women's Quilted Insulated Vest White	2
GGOEGOCR017899	Recycled Paper Journal Set	2
GGOEGAEJ028917	 Women's Short Sleeve Hero Dark Grey	2
GGOEYAAJ033017	 Men's Long & Lean Tee Charcoal	2
GGOEGAER029715	 Women's Short Sleeve Hero Tee Red Heather	2
GGOEGAAX0602	 Women's 1/4 Zip Performance Pullover Black	2
GGOEGAAQ033917	 Men's Vintage Badge Tee White	2
GGOEGALJ034414	 Women's Vintage Hero Tee Platinum	2
GGOEAAEJ035713	Android Men's Vintage Tank	2
GGOEGAEC033116	 Men's Long Sleeve Raglan Ocean Blue	2
GGOEGAAX0289	 Women's Short Sleeve Hero Dark Grey	2
GGOEGAAJ032313	 Men's Short Sleeve Hero Tee Charcoal	2
9183228	 Cam Indoor Security Camera - USA	2
9183015	 Onesie Heather	2
GGOEGPJC203399	Crunch Noise Dog Toy	2
GGOEGAAC035017	 Men's Bayside Graphic Tee	2
GGOEAAAP081213	Android Men's Take Charge Short Sleeve Tee Purple	2
GGOEGAEJ028915	 Women's Short Sleeve Hero Dark Grey	2
GGOEGAPC058814	 Women's Shell Jacket Blue/Black	2
9182717	 Men's Short Sleeve Hero Tee Light Blue	2
GGOEGAAJ032613	 Men's Short Sleeve Badge Tee Charcoal	2
GGOEGAAX0568	 Men's Watershed Full Zip Hoodie Grey	2
GGOEGAXR065155	 Toddler Short Sleeve Tee Red	2
9182721	 Men's 100% Cotton Short Sleeve Hero Tee Black	2
GGOEGAAX0680	 Youth Baseball Raglan Heather/Black	2
GGOEAAEJ028215	Android Women's Short Sleeve Badge Tee Dark Heather	2
GGOEGAFB035816	 Men's  Zip Hoodie	2
GGOEAKDH019899	Windup Android	2
GGOEGEVB070899	 Bongo Cupholder Bluetooth Speaker	2
GGOEGGCX056299	Gift Card - $25.00	2
GGOEWCKQ085457	 Pack of 9 Decal Set	2
GGOEGAAB058916	 Men's Short Sleeve Performance Badge Tee Black	2
GGOEGAAC035016	 Men's Bayside Graphic Tee	2
GGOEGAAJ057013	 Men's Short Sleeve Performance Badge Tee Charcoal	2
GGOEGAAX0319	Android Men's Short Sleeve Hero Tee Heather	2
GGOEGDHJ082599	 17 oz Double Wall Stainless Steel Insulated Bottle	2
GGOEGAEB027815	 Women's Short Sleeve Hero Tee Black	2
GGOEAAXC066455	Android Toddler Short Sleeve T-shirt Aqua	2
GGOEGAAX0662	Android Toddler Short Sleeve T-shirt Pewter	2
GGOEGAAX0681	 Youth Sports Tee Navy	2
GGOEGALP034313	 Women's Vintage Hero Tee Lavender	2
GGOEGAAX0655	 Toddler Short Sleeve T-shirt Grey	2
GGOEAAAH083315	Android Men's Paradise Short Sleeve Tee Olive	2
9182793	 Men's Long & Lean Tee Charcoal	2
GGOEGBPB082099	UpCycled Handlebar Bag	2
9183220	 Leather Journal-Brown	2
GGOEGAAJ080615	 Men's Bike Short Sleeve Tee Charcoal	2
GGOEGAAJ059116	 Men's Short Sleeve Performance Badge Tee Pewter	2
9182980	 Pet Feeding Mat	2
9182784	 Women's Short Sleeve Hero Tee White	2
GGOEAAXN066329	Android Toddler Short Sleeve T-shirt Pink	2
GGOEAAAH083314	Android Men's Paradise Short Sleeve Tee Olive	2
GGOEGAXC065228	 Toddler Short Sleeve T-shirt Royal Blue	2
9182777	 Women's Performance Golf Polo Blue	2
9182778	 Women's Softshell Jacket Black/Grey	2
GGOEGAAX0604	 Women's Quilted Insulated Vest Black	2
GGOEGHPB071610	 Twill Cap	2
GGOEGADJ059814	 Men's Convertible Vest-Jacket Pewter	2
GGOEYAXR066130	 Toddler Short Sleeve Tee Red	2
GGOEGAAX0317	 Men's Short Sleeve Hero Tee White	2
GGOEGAAC032113	 Men's Short Sleeve Hero Tee Light Blue	2
GGOEGAAQ010416	 Men's 100% Cotton Short Sleeve Hero Tee White	2
GGOEAAXJ066229	Android Toddler Short Sleeve T-shirt Pewter	2
GGOEGAAJ032715	 Men's Long & Lean Tee Grey	2
GGOEGEHQ071199	 High Capacity 10,400mAh Charger	2
9180754	8 pc Android Sticker Sheet	2
GGOEADHH055999	22 oz Android Bottle	2
GGOEGAAX0343	 Women's Vintage Hero Tee Lavender	2
GGOEGAAX0231	 Collapsible Pet Bowl	2
GGOEWFKA083199	 Mood Original Window Decal	2
9182726	 Men's Long & Lean Tee Charcoal	2
9182788	Yoga Mat	2
9184620	 Men's Performance Full Zip Jacket Black	2
GGOENEBQ081599	 Cam Outdoor Security Camera - CA	2
GGOEGAAB010513	 Men's 100% Cotton Short Sleeve Hero Tee Black	2
GGOEGOAR013599	Ballpoint Stylus Pen	2
GGOEGAAX0588	 Women's Shell Jacket Blue/Black	2
GGOEGAAJ032813	 Men's Long & Lean Tee Charcoal	2
GGOEGAPB058215	 Women's Lightweight Microfleece Jacket	2
GGOEAAAB034813	Android BTTF Cosmos Graphic Tee	2
GGOEGBRJ037399	 Rucksack	2
GGOENEBQ079199	 Protect Smoke + CO White Wired Alarm-USA	2
GGOEYAEJ029616	 Women's Short Sleeve Tri-blend Badge Tee Grey	2
GGOEGALJ072914	 Women's Performance Hero Tee Gunmetal	2
GGOEYAEJ029516	 Women's Short Sleeve Tri-blend Badge Tee Charcoal	2
GGOEGEHQ072599	 4400mAh Power Bank	2
GGOEGBRB079599	25L Classic Rucksack	2
9184705	 Women's Typography Short Sleeve Tee	2
GGOEGADB059213	 Men's Airflow 1/4 Zip Pullover Black	2
9182780	 Women's Shell Jacket Blue/Black	2
GGOEGAAX0651	 Toddler Short Sleeve Tee Red	2
GGOEGHPJ080010	 French Terry Cap	2
GGOEGAAX0629	 Baby Essentials Set	2
GGOEGAEQ027913	 Women's Short Sleeve Hero Tee White	2
GGOEGHPA002910	 Trucker Hat	2
9182765	 Women's Convertible Vest-Jacket Sea Foam Green	2
GGOEAAAB034814	Android BTTF Cosmos Graphic Tee	2
GGOEGAAX0348	Android BTTF Cosmos Graphic Tee	2
9181138	 Rucksack	2
GGOEAAWT061750	Android Onesie Gold	2
GGOEGAWR061849	 Infant Short Sleeve Tee Red	2
GGOEGAPJ058014	 Women's 1/4 Zip Jacket Charcoal	2
GGOEAAYC068724	Android Youth Short Sleeve T-shirt Aqua	2
GGOEGAAX0656	 Toddler Hoodie Royal Blue	2
GGOEGPJC019099	7" Dog Frisbee	2
9184697	 Mood Original Window Decal	2
GGOEGOAR013099	 Stylus Pen w/ LED Light	2
GGOEGHGT019599	 Sunglasses	2
GGOEGAAR010715	 Men's 100% Cotton Short Sleeve Hero Tee Red	2
9183230	 Protect Smoke + CO White Battery Alarm-USA	2
GGOEGADB056618	Men's Weatherblock Shell Jacket Black	2
GGOEGALJ036415	 Women's Tee Grey	2
GGOEYAFB073115	 Men's Fleece Hoodie Black	2
GGOEAAAH083317	Android Men's Paradise Short Sleeve Tee Olive	2
GGOEGGOA017399	Maze Pen	2
GGOEGADJ056815	 Men's Watershed Full Zip Hoodie Grey	2
GGOEGADJ059718	 Men's Quilted Insulated Vest Battleship Grey	2
GGOEAXXX0808	Android Men's Engineer Short Sleeve Tee Charcoal	2
GGOEGAAX0622	 Infant Short Sleeve Tee White	2
GGOEGADJ056813	 Men's Watershed Full Zip Hoodie Grey	2
GGOEAAEJ028216	Android Women's Short Sleeve Badge Tee Dark Heather	2
GGOEGAAX0335	 Men's Long Sleeve Pullover Badge Tee Heather	2
GGOEGATB060414	 Women's Quilted Insulated Vest Black	2
GGOEGAEC033117	 Men's Long Sleeve Raglan Ocean Blue	2
GGOEGAEJ031317	 Tri-blend Hoodie Grey	2
GGOEGALB036516	 Women's Scoop Neck Tee Black	2
GGOEGAAX0037	 Sunglasses	2
GGOEGAAX0291	 Women's Short Sleeve Hero Tee Sky Blue	2
GGOEGAWR061053	 Onesie Red/Graphite	2
GGOEGAAX0279	 Women's Short Sleeve Hero Tee White	2
9182720	 Men's Short Sleeve Badge Tee Charcoal	2
GGOEGAYQ069024	 Youth Short Sleeve Tee White	2
GGOEYAEJ029517	 Women's Short Sleeve Tri-blend Badge Tee Charcoal	2
GGOEYAAJ033016	 Men's Long & Lean Tee Charcoal	2
GGOEYAAQ031716	 Men's Short Sleeve Hero Tee White	2
GGOEGAER029716	 Women's Short Sleeve Hero Tee Red Heather	2
GGOEGAYH067926	 Youth Girl Tee Green	2
GGOEAAXN066328	Android Toddler Short Sleeve T-shirt Pink	2
GGOEAAEJ033413	Android Men's Long Sleeve Badge Crew Tee Heather	2
GGOEGAEJ031315	 Tri-blend Hoodie Grey	2
9182761	 Women's Yoga Jacket Black	2
GGOEAAEJ030916	Android Women's Long Sleeve Blended Cardigan Grey	2
GGOEGADC059513	 Men's Microfiber 1/4 Zip Pullover Blue/Indigo	2
GGOEGAAX0580	 Women's 1/4 Zip Jacket Charcoal	2
9183186	 G Noise-reducing Bluetooth Headphones	2
GGOEGAAX0795	25L Classic Rucksack	2
GGOEGGCX056399	Gift Card - $250.00	2
9182754	 Men's Softshell Jacket Black/Grey	2
GGOEGFSR022099	 Kick Ball	2
GGOEGOCD078399	 Leather Perforated Journal	2
GGOEGAAC032114	 Men's Short Sleeve Hero Tee Light Blue	2
GGOEGAXL065929	 Toddler Raglan Shirt Blue Heather/Navy	2
GGOEGAAX0346	 Men's Vintage Tee	2
GGOEGAWC062848	 Infant Zip Hood Royal Blue	2
GGOEGCBN016899	 Pet Feeding Mat	2
GGOEAAYC068756	Android Youth Short Sleeve T-shirt Aqua	2
GGOEGAAX0688	Android Youth Short Sleeve T-shirt Pewter	2
GGOEAAAJ032413	Android Men's Short Sleeve Tri-blend Hero Tee Grey	2
GGOEYAEA035115	 Men's Vintage Henley	2
GGOEGAAX0732	 Women's Fleece Hoodie Black	2
GGOEAAWN062650	Android Infant Short Sleeve Tee Pink	2
GGOEGAAX0074	 22 oz Water Bottle	2
9182173	 Stylus Pen w/ LED Light	2
GGOEGADJ057116	 Men's Performance 1/4 Zip Pullover Heather/Black	2
GGOEGADC059517	 Men's Microfiber 1/4 Zip Pullover Blue/Indigo	2
GGOEWAAJ082814	 Men's Short Sleeve Tee	2
GGOEGAAX0299	 Women's V-Neck Tee Charcoal	2
GGOEWALJ082713	 Women's Short Sleeve Tee	2
GGOEAAAP081216	Android Men's Take Charge Short Sleeve Tee Purple	2
GGOEGAAX0325	 Men's Short Sleeve Hero Tee Charcoal	2
GGOEGAAX0360	 Women's Fleece Hoodie	2
GGOEGEVB070599	 G Noise-reducing Bluetooth Headphones	2
GGOEGOCR078499	 Spiral Leather Journal	2
GGOEGAAX0366	 Women's Scoop Neck Tee White	2
GGOEAAAB034916	Android BTTF Moonshot Graphic Tee	2
9180764	 Canvas Tote Natural/Navy	2
GGOEGAYB068024	 Youth Baseball Raglan Heather/Black	2
GGOEGAAX0664	Android Toddler Short Sleeve T-shirt Aqua	2
GGOEAAAP081217	Android Men's Take Charge Short Sleeve Tee Purple	2
GGOEGAAX0284	Women's  Short Sleeve Hero Tee Black	2
GGOEGAAX0685	 Youth Short Sleeve T-shirt Yellow	2
GGOEGAPB058614	 Women's Yoga Jacket Black	2
GGOEGATB060417	 Women's Quilted Insulated Vest Black	2
GGOEADHH073999	Android 17oz Stainless Steel Sport Bottle	2
GGOEGBMJ013399	Sport Bag	2
GGOEGAWC062849	 Infant Zip Hood Royal Blue	2
GGOEGPJR018999	7" Dog Frisbee	2
9182739	 Men's Watershed Full Zip Hoodie Grey	2
GGOEGALJ072913	 Women's Performance Hero Tee Gunmetal	2
GGOEGAAX0617	Android Onesie Gold	2
GGOEGAER035517	 Men's Vintage Tank	2
GGOEYAFB073116	 Men's Fleece Hoodie Black	2
GGOEGAAX0362	 Men's Pullover Hoodie Grey	2
GGOEGAEJ035317	 Vintage Henley Grey/Black	2
GGOEAAAL081115	Android Men's Pep Rally Short Sleeve Tee Navy	2
GGOEGEHQ024099	Clip-on Compact Charger	2
GGOEYHPA003510	 Trucker Hat	2
GGOEGAAR010716	 Men's 100% Cotton Short Sleeve Hero Tee Red	2
GGOEGAAX0605	 Women's Quilted Insulated Vest White	2
GGOEYAEA035116	 Men's Vintage Henley	2
GGOEGHGC019799	 Sunglasses	2
GGOEGALJ036417	 Women's Tee Grey	2
GGOEGALQ034216	 Women's Vintage Hero Tee White	2
GGOEYAEJ029613	 Women's Short Sleeve Tri-blend Badge Tee Grey	2
GGOEGAAL010614	 Men's 100% Cotton Short Sleeve Hero Tee Navy	2
GGOEGAAX0359	Android Men's  Zip Hoodie	2
GGOEGESC014099	Rocket Flashlight	2
GGOEGAEB027814	 Women's Short Sleeve Hero Tee Black	2
GGOEYAEJ029514	 Women's Short Sleeve Tri-blend Badge Tee Charcoal	2
GGOEAAAH083313	Android Men's Paradise Short Sleeve Tee Olive	2
GGOEGAAX0606	 Women's Convertible Vest-Jacket Black	2
9182723	 Men's 100% Cotton Short Sleeve Hero Tee White	2
GGOEAAYC068725	Android Youth Short Sleeve T-shirt Aqua	2
GGOEGAAX0295	 Women's Short Sleeve Tri-blend Badge Tee Charcoal	2
9183152	 Youth Short Sleeve Tee Red	2
9180905	 Men's Long Sleeve Raglan Ocean Blue	2
GGOEAAEH035213	Android Men's Vintage Henley	2
GGOEGAAJ073414	 Men's Short Sleeve Hero Tee Heather	2
9184681	 17 oz Double Wall Stainless Steel Insulated Bottle	2
9181150	Gift Card - $250.00	2
GGOEGBJC014399	 Tote Bag	2
9182745	 Men's Quilted Insulated Vest Black	2
GGOEGATC060313	 Women's 1/4 Zip Performance Pullover Two-Tone Blue	2
GGOEGAAX0081	Recycled Paper Journal Set	2
9180766	Sport Bag	2
GGOEGARJ058413	 Women's Yoga Pants	2
GGOEGAXR066030	 Toddler Sports T-shirt Red	2
GGOEGFKQ020399	 Laptop and Cell Phone Stickers	2
GGOEGAAX0597	 Men's Quilted Insulated Vest Battleship Grey	2
GGOEGAER035515	 Men's Vintage Tank	2
GGOEGADJ057114	 Men's Performance 1/4 Zip Pullover Heather/Black	2
GGOEGALJ060115	 Women's Short Sleeve Performance Tee Pewter	2
GGOEADWQ015699	Android Rise 14 oz Mug	2
GGOEGPXC023299	 Collapsible Pet Bowl	2
GGOEGAAX0334	Android Men's Long Sleeve Badge Crew Tee Heather	2
9182898	Android Youth Short Sleeve T-shirt Aqua	2
9182737	 Women's 3/4 Sleeve Baseball Raglan Heather/Black	2
GGOEGAPB058615	 Women's Yoga Jacket Black	2
GGOEGADB059216	 Men's Airflow 1/4 Zip Pullover Black	2
9180779	1 oz Hand Sanitizer	2
GGOEYDHJ019399	24 oz  Sergeant Stripe Bottle	2
GGOEAFKQ020599	Android Sticker Sheet Ultra Removable	2
GGOEYAEA035113	 Men's Vintage Henley	2
GGOEGAFJ036213	 Men's Pullover Hoodie Grey	2
GGOEGADC059514	 Men's Microfiber 1/4 Zip Pullover Blue/Indigo	2
GGOEGALQ034215	 Women's Vintage Hero Tee White	2
GGOEGATJ060515	 Women's Quilted Insulated Vest White	2
GGOEGAAC035013	 Men's Bayside Graphic Tee	2
GGOEAAAJ080816	Android Men's Engineer Short Sleeve Tee Charcoal	2
GGOEYAAJ032515	 Men's Short Sleeve Hero Tee Charcoal	2
GGOEGAEJ029915	 Women's V-Neck Tee Charcoal	2
GGOEYAFB073113	 Men's Fleece Hoodie Black	2
9180771	Yoga Mat Purple	2
9182502	 Women's Yoga Jacket Black	2
GGOEGADB056613	Men's Weatherblock Shell Jacket Black	2
GGOEAAEJ035716	Android Men's Vintage Tank	2
GGOEGAWQ062949	 Baby Essentials Set	2
GGOEGAAH034015	 Men's Vintage Badge Tee Sage	2
GGOEAAAB034914	Android BTTF Moonshot Graphic Tee	2
9182176	Android Women's Short Sleeve Badge Tee Dark Heather	2
GGOEGAAX0353	 Vintage Henley Grey/Black	2
GGOEGAER035516	 Men's Vintage Tank	2
GGOEGAXJ065730	 Toddler 1/4 Zip Fleece Pewter	2
GGOEAAAQ032013	Android Men's Short Sleeve Hero Tee White	2
GGOEGAEB084515	BLM Sweatshirt	2
GGOEAAEJ033415	Android Men's Long Sleeve Badge Crew Tee Heather	2
GGOEGAAX0323	 Men's Short Sleeve Hero Tee Charcoal	2
GGOEGAEB027816	 Women's Short Sleeve Hero Tee Black	2
9183221	 Leather Journal-Black	2
GGOEGATH060714	 Women's Convertible Vest-Jacket Sea Foam Green	2
GGOEGAAX0107	 Men's 100% Cotton Short Sleeve Hero Tee Red	2
GGOEGAAX0679	 Youth Girl Tee Green	2
GGOEGAAX0042	Android Stretch Fit Hat	2
9183205	 Zipper-front Sports Bag	2
GGOEWFKA083299	 Mood Ninja Window Decal	2
GGOEYAEJ029617	 Women's Short Sleeve Tri-blend Badge Tee Grey	2
GGOEGAWH061353	 Onesie Green	2
9184689	 Men's Short Sleeve Tee	2
GGOEGPXR023199	 Collapsible Pet Bowl	2
GGOEGAYH067956	 Youth Girl Tee Green	2
GGOEA0CH077599	Android Hard Cover Journal	2
GGOEAAAC080917	Android Lifted Men's Short Sleeve Tee Blue	2
9180759	 Lunch Bag	2
GGOEAAEH035217	Android Men's Vintage Henley	2
GGOEGADC059313	 Men's Airflow 1/4 Zip Pullover Lapis	2
GGOEGAAX0309	Android Women's Long Sleeve Blended Cardigan Grey	2
GGOEGAEJ031316	 Tri-blend Hoodie Grey	2
GGOEGAXJ065729	 Toddler 1/4 Zip Fleece Pewter	2
GGOEGAAQ033913	 Men's Vintage Badge Tee White	2
GGOEGAAB058917	 Men's Short Sleeve Performance Badge Tee Black	2
GGOEGAPB057517	Women's Weatherblock Shell Jacket Black	2
GGOEGOBC078699	 Luggage Tag	2
GGOEGBCR024399	 Lunch Bag	2
9182806	 Onesie Green	2
GGOEGAAX0318	 Men's Short Sleeve Hero Tee Black	2
GGOEGALB034113	 Women's Vintage Hero Tee Black	2
GGOEYOLR018699	 Leatherette Notebook Combo	2
GGOEGESB015099	Basecamp Explorer Powerbank Flashlight	2
GGOEGAYQ068924	 Youth Girl Hoodie	2
GGOEGAPB057816	Women's Performance Full Zip Jacket Black	2
GGOEGFKQ020799	 Doodle Decal	2
GGOEWXXX0828	 Men's Short Sleeve Tee	2
GGOEGHGH019699	 Sunglasses	2
GGOEGAXC065255	 Toddler Short Sleeve T-shirt Royal Blue	2
GGOEGAAX0582	 Women's Lightweight Microfleece Jacket	2
GGOEAAAB081013	Android Men's Outerstellar Short Sleeve Tee Black	2
GGOEGAAX0342	 Women's Vintage Hero Tee White	2
GGOEGAAX0314	 Men's 3/4 Sleeve Henley	2
GGOEGAFJ036217	 Men's Pullover Hoodie Grey	2
9183196	 4400mAh Power Bank	2
GGOEGCBB074399	 Device Holder Sticky Pad	2
GGOEAAAJ032917	Android Men's Long & Lean Badge Tee Charcoal	2
GGOEGAAX0327	 Men's Long & Lean Tee Grey	2
GGOEYHPB072210	 Twill Cap	2
GGOEGAAX0105	 Men's 100% Cotton Short Sleeve Hero Tee Black	2
GGOEGHPA003010	 Wool Heather Cap Heather/Navy	2
GGOEAHPB076114	Android Stretch Fit Hat	2
GGOEAAXJ066255	Android Toddler Short Sleeve T-shirt Pewter	2
GGOEGAPC058812	 Women's Shell Jacket Blue/Black	2
GGOEGAAX0572	 Men's Colorblock Tee White/Heather	2
9180840	Satin Black Ballpoint Pen	2
GGOEGAFJ036216	 Men's Pullover Hoodie Grey	2
9180757	Yoga Block	2
GGOEAAEJ035715	Android Men's Vintage Tank	2
GGOEAAXC066430	Android Toddler Short Sleeve T-shirt Aqua	2
GGOEGKWQ060910	 Bib White	2
GGOEYAEJ029615	 Women's Short Sleeve Tri-blend Badge Tee Grey	2
GGOEGAAX0683	 Youth Short Sleeve T-shirt Royal Blue	2
GGOEGAEJ030814	 Women's Long Sleeve Blended Cardigan Charcoal	2
GGOEGAEC033113	 Men's Long Sleeve Raglan Ocean Blue	2
9182863	 Toddler Sports T-shirt Red	2
GGOEGAAX0321	 Men's Short Sleeve Hero Tee Light Blue	2
GGOEAAAH083316	Android Men's Paradise Short Sleeve Tee Olive	2
GGOEGAEC029117	 Women's Short Sleeve Hero Tee Sky Blue	2
GGOEYAEA035117	 Men's Vintage Henley	2
GGOEGDHB072099	 Insulated Stainless Steel Bottle	2
9184676	UpCycled Handlebar Bag	2
9183112	 Men's Fleece Hoodie Black	2
GGOEGATB060617	 Women's Convertible Vest-Jacket Black	2
GGOEGAAH034016	 Men's Vintage Badge Tee Sage	2
GGOEGAAH034014	 Men's Vintage Badge Tee Sage	2
GGOENEBJ079499	 Learning Thermostat 3rd Gen-USA - Stainless Steel	2
9184675	UpCycled Bike Saddle Bag	2
GGOEGAXC065230	 Toddler Short Sleeve T-shirt Royal Blue	2
GGOEGALJ073314	 Women's Short Sleeve Hero Tee Heather	2
GGOENEBQ084699	 Learning Thermostat 3rd Gen-USA - White	2
GGOEGCNB021099	Seat Pack Organizer	2
GGOEGOAQ018099	Pen Pencil & Highlighter Set	2
9182725	 Men's Long & Lean Tee Grey	2
GGOEGALQ036616	 Women's Scoop Neck Tee White	2
9181019	 Tri-blend Hoodie Grey	2
GGOEGADC059515	 Men's Microfiber 1/4 Zip Pullover Blue/Indigo	2
9183091	 Youth Baseball Raglan Heather/Black	2
GGOEGALB034114	 Women's Vintage Hero Tee Black	2
GGOEGAWC061950	 Infant Short Sleeve Tee Royal Blue	2
9183188	 High Capacity 10,400mAh Charger	2
GGOEGAPB058217	 Women's Lightweight Microfleece Jacket	2
GGOEAHPB080210	Android 5-Panel Low Cap	2
9182848	 Toddler Hoodie Royal Blue	2
GGOEGAYT068525	 Youth Short Sleeve T-shirt Yellow	2
9182605	 Women's Tee Grey	2
GGOEGAYR068256	 Youth Short Sleeve Tee Red	2
GGOEGAAX0591	 Men's Short Sleeve Performance Badge Tee Pewter	2
GGOEGAAX0592	 Men's Airflow 1/4 Zip Pullover Black	2
GGOEGAAX0297	 Women's Short Sleeve Hero Tee Red Heather	2
GGOEGAEJ030817	 Women's Long Sleeve Blended Cardigan Charcoal	2
GGOEGAPB057813	Women's Performance Full Zip Jacket Black	2
GGOEGAYQ069025	 Youth Short Sleeve Tee White	2
GGOEGAWR061153	 Onesie Red	2
GGOEGOCL077699	 Hard Cover Journal	2
GGOENEBQ078999	 Cam Outdoor Security Camera - USA	2
GGOEGAEJ028114	 Women's Short Sleeve Badge Tee Grey	2
GGOEGAAJ032617	 Men's Short Sleeve Badge Tee Charcoal	2
GGOEYAWJ061449	 Onesie Heather	2
GGOEAHPJ004314	Android Stretch Fit Hat M/L	2
9182755	 Men's Colorblock Tee White/Heather	2
GGOEGAAX0761	Android Stretch Fit Hat Black	2
9183210	 RFID Journal	2
9183194	 Executive Umbrella	2
GGOEGAXL065930	 Toddler Raglan Shirt Blue Heather/Navy	2
GGOEYAEB035616	 Men's Vintage Tank	2
GGOEGBMC056599	Waterproof Gear Bag	2
GGOEGAEJ031313	 Tri-blend Hoodie Grey	2
9182581	 Women's Fleece Hoodie	2
GGOEGADJ057117	 Men's Performance 1/4 Zip Pullover Heather/Black	2
GGOEGAYH067924	 Youth Girl Tee Green	2
GGOEGALP036316	 Women's Long Sleeve Tee Lavender	2
GGOEGAWC062850	 Infant Zip Hood Royal Blue	2
GGOEYAAJ033015	 Men's Long & Lean Tee Charcoal	2
GGOEGAWQ062249	 Infant Short Sleeve Tee White	2
GGOEGAAX0575	 Women's Weatherblock Shell Jacket Black	2
GGOEGAEJ028913	 Women's Short Sleeve Hero Dark Grey	2
GGOEGAAH034017	 Men's Vintage Badge Tee Sage	2
GGOEGAAX0618	 Infant Short Sleeve Tee Red	2
GGOEGOLC014299	 Metallic Notebook Set	2
GGOEGAYH068456	 Youth Short Sleeve T-shirt Green	2
GGOEGBPB081999	UpCycled Bike Saddle Bag	2
GGOEGATB060214	 Women's 1/4 Zip Performance Pullover Black	2
GGOEGAWR061149	 Onesie Red	2
GGOEYAEJ029015	 Women's Short Sleeve Hero Tee Charcoal	2
GGOEAOCH077899	Android Spiral Journal with Pen	2
GGOEAAXC066429	Android Toddler Short Sleeve T-shirt Aqua	2
GGOEAOCB077499	Android RFID Journal	2
GGOEGAYQ068956	 Youth Girl Hoodie	2
GGOEGGCX056499	Gift Card - $50.00	2
9184737	 Pack of 9 Decal Set	2
GGOEGAAX0569	 Men's Performance Full Zip Jacket Black	2
9183229	 Cam Outdoor Security Camera - USA	2
GGOEAAFB035915	Android Men's  Zip Hoodie	2
GGOEGAAJ032616	 Men's Short Sleeve Badge Tee Charcoal	2
GGOEWXXX0827	 Women's Short Sleeve Tee	2
GGOEGAAX0579	 Women's Short Sleeve Performance Tee Charcoal	2
GGOEGAAX0106	 Men's 100% Cotton Short Sleeve Hero Tee Navy	2
GGOEGATJ060516	 Women's Quilted Insulated Vest White	2
GGOEGAAQ057215	 Men's Colorblock Tee White/Heather	2
GGOEGALB036513	 Women's Scoop Neck Tee Black	2
GGOEGADC059315	 Men's Airflow 1/4 Zip Pullover Lapis	2
GGOEGOCB017499	Leatherette Journal	2
9180809	 Flashlight	2
GGOEGAAX0729	 Women's Performance Hero Tee Gunmetal	2
GGOEGAWQ062248	 Infant Short Sleeve Tee White	2
GGOEAAAJ031913	Android Men's Short Sleeve Hero Tee Heather	2
GGOEGAUC057714	 Women's Performance Golf Polo Blue	2
GGOEYAEB035617	 Men's Vintage Tank	2
GGOEAAEJ033414	Android Men's Long Sleeve Badge Crew Tee Heather	2
GGOEGDHQ015399	26 oz Double Wall Insulated Bottle	2
GGOEGEVR014999	 Water Resistant Bluetooth Speaker	2
GGOEGAWN062750	 Infant Zip Hood Pink	2
GGOEGHPJ080110	 5-Panel Cap	2
GGOEGAAX0682	 Youth Short Sleeve Tee Red	2
GGOEGAAQ033918	 Men's Vintage Badge Tee White	2
GGOEGADJ056816	 Men's Watershed Full Zip Hoodie Grey	2
GGOEYAEJ029013	 Women's Short Sleeve Hero Tee Charcoal	2
GGOEAHPB076113	Android Stretch Fit Hat	2
9180792	20 oz Stainless Steel Insulated Tumbler	2
GGOEAAAJ032916	Android Men's Long & Lean Badge Tee Charcoal	2
9183213	Android Hard Cover Journal	2
GGOEGAWR061050	 Onesie Red/Graphite	2
GGADFBSBKS42347	PC gaming speakers	2
GGOEGAWR061848	 Infant Short Sleeve Tee Red	2
GGOEGAAB058915	 Men's Short Sleeve Performance Badge Tee Black	2
GGOEGESQ016799	Plastic Sliding Flashlight	2
GGOEGAXR066029	 Toddler Sports T-shirt Red	2
GGOEGAYL068124	 Youth Sports Tee Navy	2
9180793	26 oz Double Wall Insulated Bottle	2
GGOEGAER035513	 Men's Vintage Tank	2
GGOEGADJ059815	 Men's Convertible Vest-Jacket Pewter	2
GGOEGAXR066028	 Toddler Sports T-shirt Red	2
GGOEYDHJ056099	22 oz  Bottle Infuser	2
GGOEGAEC033114	 Men's Long Sleeve Raglan Ocean Blue	2
GGOEGAAX0365	 Women's Scoop Neck Tee Black	2
9182599	 Women's Long Sleeve Tee Lavender	2
GGOEGDHC074099	 17oz Stainless Steel Sport Bottle	2
GGOEGADB057316	 Men's Lightweight Microfleece Jacket Black	2
GGOEGAAJ032814	 Men's Long & Lean Tee Charcoal	2
9183214	 Hard Cover Journal	2
GGOEGAAJ032315	 Men's Short Sleeve Hero Tee Charcoal	2
GGOEGAAQ033916	 Men's Vintage Badge Tee White	2
GGOEGAQB036017	 Women's Fleece Hoodie	2
GGOEGAAX0611	 Onesie Red	2
GGOEGOCD078199	 Leather Journal-Brown	2
GGOEGAAX0652	 Toddler Short Sleeve T-shirt Royal Blue	2
GGOEGAER029713	 Women's Short Sleeve Hero Tee Red Heather	2
GGOEGAAX0281	 Women's Short Sleeve Badge Tee Grey	2
GGOEGAYL068126	 Youth Sports Tee Navy	2
GGOEYAAB031816	 Men's Short Sleeve Hero Tee Black	2
9181137	 Alpine Style Backpack	2
GGOEGAAX0596	 Men's Quilted Insulated Vest Black	2
GGOEGAAJ057015	 Men's Short Sleeve Performance Badge Tee Charcoal	2
GGOEGAAX0620	 Infant Short Sleeve Tee Green	2
GGOEGAAC035015	 Men's Bayside Graphic Tee	2
GGOEGAAX0601	 Women's Short Sleeve Performance Tee Pewter	2
GGOEAAYJ068824	Android Youth Short Sleeve T-shirt Pewter	2
GGOEAAAJ031915	Android Men's Short Sleeve Hero Tee Heather	2
GGOEGALQ034213	 Women's Vintage Hero Tee White	2
GGOEYAYR068626	 Youth Short Sleeve Tee Red	2
GGOEGAEA030614	 Women's Recycled Fabric Tee	2
GGOEGAAX0330	 Men's Long & Lean Tee Charcoal	2
GGOEAAEB028316	Android Women's Short Sleeve Hero Tee Black	2
9182995	 Car Clip Phone Holder	2
9180781	Suitcase Organizer Cubes	2
GGOEGAAB058918	 Men's Short Sleeve Performance Badge Tee Black	2
GGOEGADJ059714	 Men's Quilted Insulated Vest Battleship Grey	2
GGOEGAAC035014	 Men's Bayside Graphic Tee	2
GGOEGAYR068225	 Youth Short Sleeve Tee Red	2
GGOEYAXR066155	 Toddler Short Sleeve Tee Red	2
GGOEGALB036514	 Women's Scoop Neck Tee Black	2
GGOEGAEQ027916	 Women's Short Sleeve Hero Tee White	2
GGOEGAAX0282	Android Women's Short Sleeve Badge Tee Dark Heather	2
GGOEAAYJ068856	Android Youth Short Sleeve T-shirt Pewter	2
GGOEAAEB028313	Android Women's Short Sleeve Hero Tee Black	2
GGOEGAPB057812	Women's Performance Full Zip Jacket Black	2
GGOEACCQ017299	Android Lunch Kit	2
GGOEGOCC077999	 Spiral Journal with Pen	2
GGOEGADB059215	 Men's Airflow 1/4 Zip Pullover Black	2
GGOEGAPB058212	 Women's Lightweight Microfleece Jacket	2
GGOEGADC059317	 Men's Airflow 1/4 Zip Pullover Lapis	2
GGOEGALJ034416	 Women's Vintage Hero Tee Platinum	2
GGOEYAEB028414	Women's  Short Sleeve Hero Tee Black	2
GGOEGAEJ028115	 Women's Short Sleeve Badge Tee Grey	2
GGOEYAYR068625	 Youth Short Sleeve Tee Red	2
GGOEGAPB058617	 Women's Yoga Jacket Black	2
GGOEGAAB010515	 Men's 100% Cotton Short Sleeve Hero Tee Black	2
9184734	 Learning Thermostat 3rd Gen-USA - Copper	2
GGOEGAAJ032816	 Men's Long & Lean Tee Charcoal	2
GGOEGAAJ080614	 Men's Bike Short Sleeve Tee Charcoal	2
GGOEGAXC065229	 Toddler Short Sleeve T-shirt Royal Blue	2
GGOEGAYB068025	 Youth Baseball Raglan Heather/Black	2
GGOEGAAX0567	 Men's Softshell Jacket Black/Grey	2
9180756	Windup Android	2
GGOEAAWJ062548	Android Infant Short Sleeve Tee Pewter	2
GGOEGAAJ032714	 Men's Long & Lean Tee Grey	2
GGOEGAEJ030815	 Women's Long Sleeve Blended Cardigan Charcoal	2
GGOEGATB060216	 Women's 1/4 Zip Performance Pullover Black	2
GGOEGAEJ035314	 Vintage Henley Grey/Black	2
GGOEGAAX0352	Android Men's Vintage Henley	2
GGOEGAAX0357	Android Men's Vintage Tank	2
GGOEGAER029714	 Women's Short Sleeve Hero Tee Red Heather	2
GGOEGAAX0104	 Men's 100% Cotton Short Sleeve Hero Tee White	2
9182771	 Women's 1/4 Zip Jacket Charcoal	2
GGOEGADB059217	 Men's Airflow 1/4 Zip Pullover Black	2
GGOEGAAJ057016	 Men's Short Sleeve Performance Badge Tee Charcoal	2
GGOEGAYQ069026	 Youth Short Sleeve Tee White	2
GGOEGOFH020299	 Screen Cleaning Cloth	2
GGOEGALB034115	 Women's Vintage Hero Tee Black	2
GGOEGAAX0306	 Women's Recycled Fabric Tee	2
9182751	 Men's Performance Full Zip Jacket Black	2
GGOENEBB078899	 Cam Indoor Security Camera - USA	2
GGOEAAFB035913	Android Men's  Zip Hoodie	2
GGOEGALJ073317	 Women's Short Sleeve Hero Tee Heather	2
GGOEGATH060715	 Women's Convertible Vest-Jacket Sea Foam Green	2
GGOEGOAC021799	Ballpoint Pen Blue	2
GGOEYAXR066129	 Toddler Short Sleeve Tee Red	2
9184682	 Mobile Phone Vent Mount	2
GGOENEBD084799	 Learning Thermostat 3rd Gen-USA - Copper	2
GGOEGAXC065629	 Toddler Hoodie Royal Blue	2
GGOEGATB060615	 Women's Convertible Vest-Jacket Black	2
GGOEGAAX0571	 Men's Performance 1/4 Zip Pullover Heather/Black	2
GGOEGAXJ065728	 Toddler 1/4 Zip Fleece Pewter	2
GGOEGAAX0304	 Women's 3/4 Sleeve Baseball Raglan Heather/Black	2
9183096	 Youth Sports Tee Navy	2
GGOEGAAJ032317	 Men's Short Sleeve Hero Tee Charcoal	2
GGOEGAEJ028914	 Women's Short Sleeve Hero Dark Grey	2
GGOEGAAX0733	 Women's Short Sleeve Hero Tee Heather	2
GGOEGALQ034214	 Women's Vintage Hero Tee White	2
GGOEGAEJ031314	 Tri-blend Hoodie Grey	2
9183234	 Learning Thermostat 3rd Gen-USA - Stainless Steel	2
9182753	 Men's Weatherblock Shell Jacket Black	2
GGOEAAAJ080813	Android Men's Engineer Short Sleeve Tee Charcoal	2
GGOEGALJ073313	 Women's Short Sleeve Hero Tee Heather	2
GGOEGDHR018499	 22 oz Water Bottle	2
GGOEGAAX0663	Android Toddler Short Sleeve T-shirt Pink	2
GGOEGADC059314	 Men's Airflow 1/4 Zip Pullover Lapis	2
GGOEAAAJ032915	Android Men's Long & Lean Badge Tee Charcoal	2
GGOEGAYL068156	 Youth Sports Tee Navy	2
GGOEYAAB031814	 Men's Short Sleeve Hero Tee Black	2
GGOEAFKQ020499	8 pc Android Sticker Sheet	2
GGOEAAYC068726	Android Youth Short Sleeve T-shirt Aqua	2
GGOEGAAX0657	 Toddler 1/4 Zip Fleece Pewter	2
GGOEGBFC018799	Electronics Accessory Pouch	2
GGOEGCKQ013199	1 oz Hand Sanitizer	2
GGOEGAAJ057017	 Men's Short Sleeve Performance Badge Tee Charcoal	2
GGOEGAAX0344	 Women's Vintage Hero Tee Platinum	2
GGOEAAAB034917	Android BTTF Moonshot Graphic Tee	2
GGOEGAAJ059115	 Men's Short Sleeve Performance Badge Tee Pewter	2
9182709	Android Women's Long Sleeve Blended Cardigan Grey	2
GGOEGAAB010514	 Men's 100% Cotton Short Sleeve Hero Tee Black	2
GGOEGAWH061354	 Onesie Green	2
GGOEAAAB034915	Android BTTF Moonshot Graphic Tee	2
GGOEWXXX0835	 Men's Typography Short Sleeve Tee	2
9180824	Foam Can and Bottle Cooler	2
GGOEYAEJ029017	 Women's Short Sleeve Hero Tee Charcoal	2
GGOEAAAB034815	Android BTTF Cosmos Graphic Tee	2
GGOEGAXQ067129	 Toddler Short Sleeve Tee White	2
GGOEGAXL065955	 Toddler Raglan Shirt Blue Heather/Navy	2
GGOEGAAX0338	 Men's Vintage Badge Tee Black	2
GGOEGAAJ032817	 Men's Long & Lean Tee Charcoal	2
GGOEGAXC065630	 Toddler Hoodie Royal Blue	2
GGOEGAYT068526	 Youth Short Sleeve T-shirt Yellow	2
GGOEGAAB033814	 Men's Vintage Badge Tee Black	2
9181664	Waterproof Gear Bag	2
GGOEGOAB022499	Satin Black Ballpoint Pen	2
GGOEGESB015199	 Flashlight	2
GGOEGAAX0607	 Women's Convertible Vest-Jacket Sea Foam Green	2
GGOEGADB056917	 Men's Performance Full Zip Jacket Black	2
GGOEGADJ059717	 Men's Quilted Insulated Vest Battleship Grey	2
GGOBJGOWUSG69402	USB wired soundbar - in store only	2
GGOEGALJ072916	 Women's Performance Hero Tee Gunmetal	2
GGOEGAWR061850	 Infant Short Sleeve Tee Red	2
GGOEYAYR068656	 Youth Short Sleeve Tee Red	2
GGOEAAWN062648	Android Infant Short Sleeve Tee Pink	2
GGOEGALP034316	 Women's Vintage Hero Tee Lavender	2
9180814	Micro Wireless Earbud	2
GGOEGAAX0296	 Women's Short Sleeve Tri-blend Badge Tee Grey	2
GGOEGAUC057717	 Women's Performance Golf Polo Blue	2
GGOEGAAQ010414	 Men's 100% Cotton Short Sleeve Hero Tee White	2
GGOEGATH060717	 Women's Convertible Vest-Jacket Sea Foam Green	2
GGOEGAAX0746	 Women's Short Sleeve Badge Tee Navy	2
GGOEYAAJ032513	 Men's Short Sleeve Hero Tee Charcoal	2
9183118	 Women's Fleece Hoodie Black	2
GGOEGAXQ067155	 Toddler Short Sleeve Tee White	2
9180844	Gunmetal Roller Ball Pen	2
GGOEGAWQ062250	 Infant Short Sleeve Tee White	2
GGOEGETR014599	 Tube Power Bank	2
GGOEGADB056717	Men's Softshell Jacket Black/Grey	2
GGOEGADC059516	 Men's Microfiber 1/4 Zip Pullover Blue/Indigo	2
9182742	 Men's Convertible Vest-Jacket Pewter	2
GGOEGAWC061949	 Infant Short Sleeve Tee Royal Blue	2
GGOEWAAJ083513	 Men's Typography Short Sleeve Tee	2
GGOEGAAX0687	Android Youth Short Sleeve T-shirt Aqua	2
GGOEGDHR082199	 25 oz Red Stainless Steel Bottle	2
9181151	Gift Card - $50.00	2
GGOEGAEJ030813	 Women's Long Sleeve Blended Cardigan Charcoal	2
GGOEYHPA003610	 Wool Heather Cap Heather/Black	2
GGOEAAWJ062549	Android Infant Short Sleeve Tee Pewter	2
GGOEAHPJ074410	Android Twill Cap	2
9182769	 Women's Short Sleeve Performance Tee Pewter	2
GGOEGALJ060114	 Women's Short Sleeve Performance Tee Pewter	2
GGOEGAYH067925	 Youth Girl Tee Green	2
GGOEGAXC065655	 Toddler Hoodie Royal Blue	2
GGOEGALB034116	 Women's Vintage Hero Tee Black	2
GGOEAAAB081016	Android Men's Outerstellar Short Sleeve Tee Black	2
GGOEGAAX0349	Android BTTF Moonshot Graphic Tee	2
GGOEWAAJ082813	 Men's Short Sleeve Tee	2
GGOEGDHC015299	23 oz Wide Mouth Sport Bottle	2
GGOEGAEJ028013	 Women's Short Sleeve Hero Tee Grey	2
GGOEGAAB010516	 Men's 100% Cotton Short Sleeve Hero Tee Black	2
GGOEAAEH035215	Android Men's Vintage Henley	2
GGOEGAAX0358	 Men's  Zip Hoodie	2
GGOEGALJ034415	 Women's Vintage Hero Tee Platinum	2
GGOEGADJ056818	 Men's Watershed Full Zip Hoodie Grey	2
9182593	 Men's Pullover Hoodie Grey	2
GGOEGAYT068524	 Youth Short Sleeve T-shirt Yellow	2
9180762	 Tote Bag	2
GGOEGAAX0213	Yoga Mat	2
GGOEYAAQ031717	 Men's Short Sleeve Hero Tee  White	2
GGOEAXXX0809	Android Lifted Men's Short Sleeve Tee Blue	2
GGOEYOCR077399	 RFID Journal	2
9183226	Android Luggage Tag	2
GGOEGAFJ036214	 Men's Pullover Hoodie Grey	2
GGOEYAAB031817	 Men's Short Sleeve Hero Tee Black	2
GGOEAAAP081214	Android Men's Take Charge Short Sleeve Tee Purple	2
GGOEYAEB035615	 Men's Vintage Tank	2
GGOEAAYJ068826	Android Youth Short Sleeve T-shirt Pewter	2
GGOEGEVB071799	 Pocket Bluetooth Speaker	2
GGOEGBJL013999	 Canvas Tote Natural/Navy	2
9182812	 Infant Zip Hood Pink	2
GGOEGALL074613	 Women's Short Sleeve Badge Tee Navy	2
GGOEGFKA022299	Keyboard DOT Sticker	2
GGOEGAAX0584	 Women's Yoga Pants	2
GGOEGBRJ037299	 Alpine Style Backpack	2
GGOEGAFJ036215	 Men's Pullover Hoodie Grey	2
GGOEGAAX0364	 Women's Tee Grey	2
GGOEAHPA004110	Android Wool Heather Cap Heather/Black	2
GGOEGAAX0603	 Women's 1/4 Zip Performance Pullover Two-Tone Blue	2
GGOEGOAQ020099	Four Color Retractable Pen	2
GGOEGAAX0290	 Women's Short Sleeve Hero Tee Charcoal	2
GGOEGATH060716	 Women's Convertible Vest-Jacket Sea Foam Green	2
GGOEGAAX0328	 Men's Long & Lean Tee Charcoal	2
GGOEGOAB021499	Metal Texture Roller Pen	2
GGOEGAAB033817	 Men's Vintage Badge Tee Black	2
GGOEWFKA083099	 Mood Happy Window Decal	2
GGOEGAAJ080616	 Men's Bike Short Sleeve Tee Charcoal	2
GGOEGADJ057113	 Men's Performance 1/4 Zip Pullover Heather/Black	2
GGOEGAAL010616	 Men's 100% Cotton Short Sleeve Hero Tee Navy	2
GGOEGAWN062748	 Infant Zip Hood Pink	2
GGOEAAAJ031917	Android Men's Short Sleeve Hero Tee Heather	2
GGOEAAAJ080814	Android Men's Engineer Short Sleeve Tee Charcoal	2
9182997	 17oz Stainless Steel Sport Bottle	2
GGOEGAAX0331	 Men's Long Sleeve Raglan Ocean Blue	2
GGOEGAEC029114	 Women's Short Sleeve Hero Tee Sky Blue	2
GGOEYAAJ032516	 Men's Short Sleeve Hero Tee Charcoal	2
GGOEGAAX0581	 Women's Colorblock Tee White	2
GGOENEBQ079099	 Protect Smoke + CO White Battery Alarm-USA	2
GGOEAAAJ031916	Android Men's Short Sleeve Hero Tee Heather	2
GGOEAAEB028314	Android Women's Short Sleeve Hero Tee Black	2
GGOEGHPL003214	 Stretch Fit Hat M/L Navy	2![image](https://github.com/oyebolakolapo/LHL_Project_One_Kolapo/assets/40770957/b5e7283f-a9b2-40f0-b6ef-9c158bc051e6)


Question 2: 
find the total number of unique visitors (fullVisitorID) 
SQL Queries:
SELECT COUNT (DISTINCT fullvisitorid) AS Unique_visitors
FROM all_sessions
Answer:
[40]

Question 3: 
--Find the total number of unique visitors by referring sites 
SQL Queries:
SELECT COUNT (DISTINCT fullvisitorid) AS Unique_visitors_by_referring_sites
FROM all_sessions
WHERE channelgrouping ='Referral'
Answer:
[17]

Question 4: 
-- Find each unique product viewed by each visitorSQL Queries:
SELECT DISTINCT all_sessions.fullvisitorid, products.name
FROM all_sessions
INNER JOIN products ON all_sessions.productssku = products.productssku

Answer:
fullvisitorid	name
2.58E+16	 Cam Outdoor Security Camera - USA
8.61E+16	 Men's Vintage Badge Tee Sage
2.24E+17	 Men's 100% Cotton Short Sleeve Hero Tee Black
3.68E+17	SPF-15 Slim & Slender Lip Balm
4.01E+17	 Cam Outdoor Security Camera - USA
4.57E+17	 Men's Short Sleeve Hero Tee Charcoal
5.38E+17	 Sunglasses
8.99E+17	 Sunglasses
1.25E+18	 Men's Short Sleeve Badge Tee Charcoal
1.7E+18	 Learning Thermostat 3rd Gen-USA - Stainless Steel
2.31E+18	 Learning Thermostat 3rd Gen-USA - Stainless Steel
2.4E+18	 Laptop and Cell Phone Stickers
2.81E+18	 Learning Thermostat 3rd Gen-USA - Stainless Steel
3.22E+18	 Mood Original Window Decal
3.44E+18	 Bongo Cupholder Bluetooth Speaker
3.76E+18	 Cam Indoor Security Camera - USA
4.13E+18	Four Color Retractable Pen
4.4E+18	 Cam Indoor Security Camera - USA
4.41E+18	 Laptop and Cell Phone Stickers
4.85E+18	 Learning Thermostat 3rd Gen-USA - Stainless Steel
4.95E+18	 Womens 3/4 Sleeve Baseball Raglan Heather/Black
5.04E+18	 Learning Thermostat 3rd Gen-USA - White
5.1E+18	Red Spiral  Notebook
5.96E+18	 Men's Bike Short Sleeve Tee Charcoal
6.33E+18	 Cam Indoor Security Camera - USA
6.34E+18	 22 oz Water Bottle
6.57E+18	 Learning Thermostat 3rd Gen-USA - Stainless Steel
6.84E+18	 Sunglasses
7.36E+18	Android Wool Heather Cap Heather/Black
7.37E+18	 Men's  Zip Hoodie
7.68E+18	 Men's Airflow 1/4 Zip Pullover Lapis
8.65E+18	 Mobile Phone Vent Mount
8.8E+18	 Men's  Zip Hoodie
8.91E+18	 Men's Vintage Badge Tee White![image](https://github.com/oyebolakolapo/LHL_Project_One_Kolapo/assets/40770957/af7894a3-4fae-452d-a11f-16d751043445)


Question 5: 

SQL Queries:

Answer:
