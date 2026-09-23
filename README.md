# Sales_Project
An interactive Excel dashboard that analyzes 3,900 retail customer purchases to show who is buying, what they buy, and how discounts and subscriptions relate to spending.

 Project Overview

A retail business wants to understand its customers better. This project cleans and segments the purchase data, then summarizes it in PivotTables and an interactive dashboard with slicers so a non-technical stakeholder can filter by Gender, Category, Subscription Status, and Age Group without touching a formula.

Business questions answered

Which customer age groups and genders generate the most revenue?
Which product categories and items sell best?
How much of the revenue comes from discounted purchases?
Do subscribers buy more often than non-subscribers?
How do spending patterns vary by season, region, and payment or shipping method?

 Dataset
Property	Detail
File	Sales.xlsx
Records	3,900 purchases (one row per customer, unique Customer ID)
Columns	18 original fields + 2 engineered fields
Customer ages	18 to 70 (average 44)
Locations	50 US states
Products	25 items across 4 categories

Original fields: Customer ID, Age, Gender, Item Purchased, Category, Purchase Amount (USD), Location, Size, Color, Season, Review Rating, Subscription Status, Shipping Type, Discount Applied, Promo Code Used, Previous Purchases, Payment Method, Frequency of Purchases.

Engineered fields (Excel formulas on the Data 2 sheet)

Data Preparation
Checked for duplicates: none found, and every Customer ID is unique
Found 37 missing Review Ratings (~1%): left as blank rather than imputed, and excluded from rating averages
Confirmed Discount Applied and Promo Code Used are identical in all 3,900 rows, so they were treated as one signal
Created age and purchase-amount segments to make the data easier to compare
📊 Dashboard Contents

Charts

Age Group vs Purchase Amount
Gender vs Purchase Amount
Category vs Purchase Amount
Subscription Status vs Previous Purchases
Percent of Purchases Made with a Discount (pie)

Slicers: Gender · Category · Subscription Status · Age Group

🔍 Key Findings

Total revenue: $233,081 · Average purchase: $59.76 · Average review rating: 3.75 / 5

Elders (51+) drive the most revenue ($88,480, 38%), but because there are more of them, not because they spend more. Average spend per purchase is almost flat across segments: Youth $60.65, Adult $59.76, Older Adult $59.07, Elder $59.95. Elders are 1,476 of the 3,900 customers.
Men account for 68% of purchases and 68% of revenue ($157,890). Average spend is nearly the same for men ($59.54) and women ($60.25), so the gap is a customer-volume gap. This points to an opportunity to grow the female customer base.
Clothing is the top category ($104,264, 45%), followed by Accessories ($74,200), Footwear ($36,093), and Outerwear ($18,524). Outerwear has the lowest average purchase ($57.17).
43% of purchases used a discount, generating $99,411 (43% of revenue). Discounted purchases average slightly less ($59.28) than full-price ones ($60.13), so discounts are not inflating basket size.
Subscribers are 27% of customers and 27% of revenue. They average slightly more previous purchases (26.1 vs 25.1), a small difference that suggests subscription alone is not yet a strong loyalty driver.
Sales are evenly spread. Fall is the strongest season ($60,018) and the top five states (Montana, Illinois, California, Idaho, Nevada) are separated by only ~$270 in revenue. No single item, season, or region dominates.

 Recommendations
Target acquisition, not basket size. Spend per purchase is consistent across every segment, so growth will come from adding customers, especially women and younger shoppers.
Re-test discount strategy. Discounts reach 43% of purchases without raising average spend. A targeted or tiered discount could protect margin.
Give subscribers a reason to spend more. Their behavior is nearly identical to non-subscribers, so consider perks tied to purchase value or frequency.
Plan inventory for Fall, the highest-revenue season, and review why Outerwear underperforms.
Field	Logic
Group (age segment)	Youth ≤ 25 · Adult 26–35 · Older Adult 36–50 · Elder 51+
Purchase Amount Group
