# Swiggy Data-Analytics Dashboard (Excel)
To Analyse Swiggy’s restaurant listings across 9 Indian cities (market, food and quality) and track the company’s business performance over 9 quarters (Q1 FY25 to Q1 FY27).

Data sources :
1. swiggy.csv: 8,679 restaurant listings after cleaning (8,680 before), with area, city, price, ratings, cuisines, and delivery time. It is a snapshot with no dates.
2. Swiggy shareholder letters for Q4 FY25 and Q1 FY27: revenue, net loss, and GOV for Food delivery and Instamart.

Tools: Excel only: Power Query, PivotTables, PivotCharts, slicers, the Data Model, a filled map, and formulas.

Workbook structure : 
1. Readme; Raw_Resturant (untouched copy of the CSV).
2. Clean_Resturant (cleaned table).
3. Cuisines (one row per restaurant and cuisine). 
4. Dashboard_1 (market overview). 
5. Dashboard_2 (food and quality).
6. Dashboard_3 (business trend).
7. An Analysis sheet behind each dashboard that holds its PivotTables and calculations.

Cleaning steps :
1. Trimmed extra spaces in text columns.
2. Replaced 5 prices of 0 with blank, so averages ignore them.
3. Removed 1 duplicate listing (Cake Adda, Kuber Nagar).
4. Added Price Band (Budget up to ₹200, Mid up to ₹400, Premium above), Rating Band, and State.
5. Split Food type into a separate Cuisines table (599 cuisines) and fixed indian to Indian.
6. Marked 3,272 restaurants as Unrated (see Assumptions).

Dashboard Images :
1. Swiggy Market Overview (where the listings are, and city and price patterns)
<img width="1457" height="942" alt="Dashboard 1_Swiggy" src="https://github.com/user-attachments/assets/13e694ac-2087-46f6-95cf-371fe53d568f" />

2. Swiggy Food & Quality (top cuisines, ratings, and top rated restaurants)
<img width="1557" height="971" alt="Dashboard 2_Swiggy" src="https://github.com/user-attachments/assets/cd7fbaa1-7a61-44c1-a2ea-1b152dacfda4" />

3. Swiggy Business Trend (Swiggy’s revenue, losses, and Instamart growth)
<img width="1567" height="957" alt="Dashboard 3_Swiggy" src="https://github.com/user-attachments/assets/997cdd2c-74ae-4302-b1fb-cecd34e0a887" />

Assumptions and limitations :
1. Each row is a listing, so a restaurant with several branches appears several times.
2. Total ratings has only 8 values (20, 50, 80, 100, 500, 1000, 5000, 10000), so it’s a band, not an exact count.
3. Every restaurant in the 80-ratings band has exactly 2.9, which looks like a placeholder for new restaurants. I labelled these Unrated. I inferred this from the pattern, and the data doesn’t confirm it.
4. The data has no dates, so it can’t show a trend. The trend comes from the company financials only.
5. The Price column isn’t defined in the dataset, so I treat it as an average price.
6. Company revenue also includes Supply Chain and Distribution, a business-to-business segment (see findings).

Key findings :

Market (Page 1):
1. The data has 8,679 listings across 9 cities. Kolkata has the most (1,346, 15.5%), and the top 3 cities (Kolkata, Mumbai, Chennai) hold 43% of listings.
2. Maharashtra (Mumbai plus Pune) holds 2,367 listings, 27.3% of the total.
3. The busiest area is Rohini (257 listings), followed by Chembur (208).
4. By price band, Mid is 48%, Budget 32%, and Premium 21%. Mumbai is the most expensive city (average ₹394) and Surat the cheapest (₹271).
5. Hyderabad is Budget-heavy (41% of its listings), while Mumbai has 28% Premium and Surat only 8%.
Delivery :
1. The average delivery time is 54 minutes. Ahmedabad is the fastest at 44.7 and Kolkata the slowest at 67.8.
2. Kolkata has the most restaurants and the slowest delivery. 72% of its listings take 60 minutes or more, against 6% in Ahmedabad.

Food and quality (Page 2):
1. Chinese is the top cuisine (2,588 listings, 30% of all listings), then North Indian (1,921) and Indian (1,774). The data holds 599 cuisines, about 2.7 per listing.
2. 3,272 restaurants (38%) are Unrated. Pune has the most (47.4%) and Hyderabad the fewest (27.9%).
3. The average rating is 4.11 for rated restaurants, but 3.66 if Unrated ones are included, so leaving them in would understate quality.
4. Among rated restaurants, 74% are High (4.0 or above).
5. Premium restaurants rate slightly higher (4.20) than Budget (4.10) and Mid (4.08), but the link between price and rating is weak.
6. Delivery time and rating show almost no relationship.
7. Nine restaurants tie for the top rating (4.70), so there is no single clear winner.

Business trend (Page 3):
1. FY26 revenue was ₹23,053 crore, up 51% from ₹15,227 crore in FY25. Net loss rose 33%, from ₹3,117 crore to ₹4,154 crore.
2. The net loss as a share of revenue fell from 19.0% (Q1 FY25) to 11.6% (Q1 FY27). The loss peaked at ₹1,197 crore in Q1 FY26 and fell to ₹791 crore.
3. Instamart GOV grew from ₹2,724 crore to ₹7,907 crore (about 2.9 times), against 39% growth for Food delivery (₹6,808 crore to ₹9,490 crore).
4. Instamart’s share of Food plus Instamart GOV rose from 28.6% to a peak of 47.0% in Q3 FY26, then eased to 45.5%. Its GOV has been flat for three quarters (7,938, 7,881, 7,907).
5. Revenue growth isn’t only Food and Instamart. Supply Chain and Distribution was ₹3,195 crore of ₹6,812 crore in Q1 FY27 (47%).

Business suggestions (based on the data) :
1. Fix delivery in Kolkata, Chennai and Pune. 72%, 49% and 43% of their listings take an hour or more. More delivery partners or better restaurant-to-customer matching there would have the biggest effect.
2. Get new restaurants rated. With 38% unrated, customers can’t judge those restaurants. Prompting early customers to rate would improve trust and make the ratings useful.
3. Look at Pune and Delhi first for ratings, since they have the highest unrated shares (47% and 44%).
4. Match price mix to each city. Surat has very little Premium, and Hyderabad leans Budget, so these are gaps to test. Check demand before acting, since this data only shows what restaurants list, not what customers order.
5. Watch Instamart’s growth. Its losses are shrinking, but its GOV has stopped growing for three quarters, so the next quarters show whether growth returns.







