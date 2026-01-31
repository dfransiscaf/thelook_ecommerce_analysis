# TheLook E-commerce Analysis



## Project Background

TheLook is a global e-commerce company that sells trendy apparel for men and women. Company's primary focus is providing a seamless online shopping experience with a wide variety of clothing categories, from casual wear to formal attire.

Established in 2019, TheLook's book of business have grown into a data-rich platform with 100.000 customers, possesses over 125.000 transactions, and generating sales revenue exceeding $2.71 milion. 

In-depth analysis is conducted to evaluate TheLook's performance in 2025. This comprehensive review provides valuable insights that internal cross-functional teams will utilize to streamline processes and enchance TheLook's commercial performance. The key insights and recommendations are provided on the following key areas:

## Key Metrics & North Star Framework

- **Revenue & Transaction Value:** Monitoring seasonality and identifying whether growth is driven by customer acquisition or purchase frequency. This involves tracking total sales, transaction volume, and average order value (AOV) to analyze spending patterns. Additionally, it evaluates pricing strategies to determine if products are positioned as premium or potentially overpriced.
- **Conversion & Funnel Efficiency:** Identifies top-performing categories to guide targeted campaigns and promotions. This analysis evaluates sales performance by source while comparing average order value (AOV) between first-time and repeat customers. These three perspectives provide a comprehensive view of how effectively the funnel attracts and converts high-value shoppers.
- **Market Level Retention:** Analyzes customer retention across global markets to ensure that acquisition costs remain sustainable. This analysis facilitates a localized strategic approach, identifying specific regional performance gaps to move away from "one-size-fits-all" tactics. By pinpointing high-churn vs. high-loyalty markets, it enables the business to deploy tailored retention programs that address specific regional needs.
- **Category Return Performance:** Evaluates product performance by pinpointing return and refund rates across various categories. This insight identifies potential quality issues and informs strategic inventory decisions to minimize operational losses.

The SQL queries used to inspect and clean the data for this analysis can be found here [![Gist](https://img.shields.io/badge/Gist-SQL_Scripts-blue?style=for-the-badge&logo=github)](https://gist.github.com/dfransiscaf/e800ad6973e750b8945e19470b479351)

Targeted SQL queries regarding various business questions can be found here [![Gist](https://img.shields.io/badge/Gist-SQL_Scripts-blue?style=for-the-badge&logo=github)](https://gist.github.com/dfransiscaf/62fa3baa3210b0265abe2e671e8c3447)

An interactive Tableau dashboard used to report and explore sales trends can be found [here](https://public.tableau.com/views/SalesDashboard_17698378364650/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).



## Data Structure & Initial Checks

TheLook eCommerce is a comprehensive, synthetic dataset hosted on BigQuery Public Data. It consists of seven main tables containing over 120,000+ transactional records. The dataset provides a holistic view of a digital retail business, including:
- **distribution_centers:** Locations of physical warehouses.
- **events:** User behavior logs (page views, cart additions, etc.) for funnel and conversion analysis.
- **inventory_items:** Detailed stock records, including product costs and warehouse entry dates.
- **order_items:** Granular, item-level transaction history, including sale prices and specific fulfillment statuses.
- **orders:** High-level transaction records containing order metadata (user ID, order timestamp).
- **products:** Product catalog featuring category names, brands, and retail prices.
- **users:** Customer demographic profiles including age, gender, and registration details.

<img width="1593" height="1004" alt="ERD - TheLook" src="https://github.com/user-attachments/assets/ca1e8e71-3273-45a1-b8a9-a5187d408c8f" />

Initial Data Audit 
Conducted an initial data audit on the raw dataset and found several issues that required cleaning:
- **Handling Missing Values:** fills in the blanks by adding a default value.
- **Remove Duplicates:** Ensure only one record per entity by identifying and retaining the most relevant row.
- **Remove Unwanted Spaces:** Remove unnecessary spaces to ensure data consistency and uniformity across all records.
- **Data Normalization & Standardization:** Mapping coded values to user-friendly descriptions.
- **Date Integrity & Anomalies :** Removed future-dated transactions to ensure historical accuracy.

## Executive Summary

### Overview of Findings

This dashboard provides a comprehensive analysis of TheLook eCommerce performance throughout 2025, monitoring core KPIs including Total Sales, Order Volume, and Customer Growth. It tracks monthly revenue trends to identify seasonal momentum while pinpointing top-performing product categories and geographic markets. The analysis is designed to provide a clear view of global business health and identify key drivers behind the year's growth.

<p align="center">
  <img width="1199" height="599" alt="1  thelook dashboard" src="https://github.com/user-attachments/assets/82358251-775b-4802-b814-2b5cb2fda43e" />

</p>

#### **1. Revenue Growth and Market Dominance**
* Sales grew consistently throughout 2025, with China emerging as the primary market leader.
* December recorded the highest growth, with a 20,14% increase compared to the previous month, marking it the best-performing period of the year.

#### **2. Quarterly Insights and Seasonal Trends**
* The fourth quarter showed exceptional performance, driven by seasonal shopping trends and year-end marketing campaigns. Outerwear and Coats were identified as the top-performing categories during this period.
* Conversely, revenue experienced a slight 3.73% dip in February, identifying it as a period that requires further strategic attention compared to the year-end surge.

#### **3. Strategic Recommendations**
* Leverage the strong brand presence in China by developing more localized marketing campaigns to further solidify market share in the APAC region.
* To sustain momentum during peak seasons (like Q4), implement targeted loyalty programs focusing on high-performing categories such as Outerwear.
* Investigate the February slump to identify external factors (competition/market shifts) and reassess pricing and promotion strategies to regain momentum earlier in the year.

## Insights Deep Dive
### Revenue & Transaction Value

<img width="1199" height="599" alt="2  thelook sales trend" src="https://github.com/user-attachments/assets/a99a81ff-ad69-40cb-b835-eace0fa133cb" />

#### **1. Total Sales**
* Total sales showed an overall upward trajectory, finishing the year with a strong surge despite minor fluctuations in the first half.
* December emerged as the strongest month with $132.706 in sales and 1.526 unique buyers, likely driven by holiday shopping. On the other hand, February recorded the lowest performance with $58,970 in sales from 684 unique buyers.
* The average monthly sales for the year stood at $82.205.

#### **2. Average Order Value (AOV)**
* The Average Order Value (AOV) remained relatively stable throughout the year, with only minor fluctuations around the $59.05 average.
* The value peaked in July at $61.20 and saw its lowest point in January at $55.24, indicating consistent customer spending behavior despite changes in total sales volume. 

#### **3. Number of Orders**
* Order volume closely follows sales trends, confirming that revenue growth is primarily driven by an increase in transaction count rather than just higher pricing.
* December reached a peak of 2.180 orders, while February remained the lowest with 998 orders. The monthly average for the year was 1.385,5 orders.
* Despite initial fluctuations in the first half of the year, the business gained significant momentum in the later months. With AOV remaining stable, this growth was primarily driven by a surge in order volume during the peak season.

####

<img width="1199" height="599" alt="3  thelook retail price" src="https://github.com/user-attachments/assets/b82d9797-19e2-450f-90ff-9af1fc3dd8ea" />

####

* The monthly AOV indicates a stable basket size throughout the year, suggesting consistent consumer spending. However, a deep dive into the Price Delta reveals specific "high-ticket" items within certain categories.
* For instance, the Shorts category contains a significant outlier. The 'Alpha Industries Rip Short' priced at $999, which is $953 above the category average of $46. Similarly, the Outerwear & Coats category features premium items such as 'The North Face Denali Down Women's Jacket' retailing at $903, representing a price delta of $757 compared to the $146 category average. These extreme outliers warrant further investigation to determine if they represent a high-end niche segment or potential data entry errors

### Conversion & Funnel Efficiency 

<img width="1199" height="599" alt="4  thelook category" src="https://github.com/user-attachments/assets/3d0fb7a8-4d5a-4985-b098-7320e059268f" />

####

* Outerwear & Coats consistently led sales over the year, exceeding $116,405 with 819 orders. This suggests a premium pricing strategy, as it generates the highest revenue despite having fewer orders than other top categories.
* Jeans and Sweaters secured the second and third positions, generating $114,783 (1,141 orders) and $78,353 (1,057 orders) respectively, showing strong market demand.
* Clothing Sets recorded the lowest performance with only $2,034 in revenue and 23 orders, indicating a potential need for assortment review or marketing focus.
* In terms of transaction frequency, Intimates outperformed all other categories with 1,245 orders, despite not breaking into the Top 10 by revenue. This indicates a high-volume, low-margin product profile.

####

<img width="1199" height="599" alt="5  thelook first repeat" src="https://github.com/user-attachments/assets/23050db3-e2c3-46d5-8fa1-6318fb63f015" />

####

* The AOV for first-time orders shows a near-linear trend, holding steady between $56 and $61. This suggests a predictable spending pattern for new users that remains largely unaffected by seasonal shifts.
* In contrast, repeat customers exhibited higher volatility, with a notable peak in February at $93.05 followed by several sharp dips. Despite the fluctuations, repeat customers historically spend significantly more per transaction than first-time buyers.
* The data confirms that loyalty drives value; existing customers are willing to commit to larger basket sizes over time. This trend reinforces the importance of retention strategies as a primary driver for increasing revenue per user.

####

<img width="1199" height="599" alt="6  thelook channel" src="https://github.com/user-attachments/assets/ad3948a4-9461-45c9-bfee-79eb002ba1b6" />

#####

* Search is the primary acquisition channel, contributing over $586,365 in total annual sales. This dominance suggests strong brand equity, where customers are actively looking for the brand, leading to high-intent purchases.
* With a consistent average contribution, the Search channel proves to be the most mature and dependable source of income for the platform.
* Looking at the lower end, Display recorded the bottom performance at $32,402 in total sales. This significant gap suggests that display-based advertising is currently less effective at driving direct conversions, presenting an opportunity to either re-evaluate the ad creative or reallocate the budget to higher-performing channels.
* "The Other category represents a significant portion of revenue, which can be attributed to Direct Traffic and non-tracked referrals. While this indicates strong organic brand recall, where customers navigate directly to the platform, it also highlights an opportunity to refine our attribution modeling to better identify these high-performing traffic sources.
  
#####

### Market Level Retention

<img width="1199" height="599" alt="7  thelook market level" src="https://github.com/user-attachments/assets/c9c86407-3bb6-4336-af30-945b480fd828" />

#####

* Across all primary markets, China recorded the highest volume of churned users (24,570 users), representing an 86.37% churn rate. This high volume is closely followed by the United States (86.12%) and Brasil (86.32%), indicating a common challenge in long-term retention across major regions.
* Despite the high churn volume, China maintains its position as the market leader in engagement, holding the highest percentage of Active (5.79%) and Warm (7.85%) users.
* Similar patterns are observed in Brasil and the United States. Brasil slightly outperforms other major regions with a 5.49% Active and 8.19% Warm user base, while the United States follows closely with 5.64% Active and 8.24% Warm users.
* At the opposite end of the spectrum, countries like Austria and Colombia exhibit the lowest engagement levels, though these figures are skewed by small sample sizes. Austria reflects a 100% churn rate from a single user, while Colombia’s 8 users are all classified as churned, leaving the region with zero active or warm customers. These markets remain underdeveloped, indicating that current brand presence is negligible and would require a foundational market-entry strategy rather than a standard retention campaign.

### Category Return Performance

<img width="1199" height="599" alt="8  thelook return" src="https://github.com/user-attachments/assets/acf6d957-5fcf-4fe8-98b9-3fde633cb4e8" />

#####

* Pants recorded the highest return rate at 11.28%, followed by Blazers & Jackets (11.1%) and Outerwear & Coats (10.91%). This indicates a higher dissatisfaction or sizing mismatch in these specific categories throughout the year.
* Initimates dominated the sales volume with 1,245 orders. However, the high transaction count also led to a significant volume of returns (478 items). This suggests that even a standard return percentage in high-volume segments can create a heavy operational burden, necessitating more precise size guides.
* In contrast, Jumpsuits & Rompers and Underwear proved to be the most reliable products with the lowest return rates at 6.54% and 8.59%, respectively.
* However, the low return rate for Jumpsuits & Rompers is also correlated with its low sales volume, as it ranks at the bottom of the total purchase orders. This suggests that while the product is rarely returned, it also has the lowest market demand.


#####

## Recommendations:

Based on the insights and findings above, we would recommend that the stakeholder team consider the following: 

#### **1. Revenue & Transaction Value** 
* Address the sales dip in February by launching targeted marketing campaigns to maintain momentum during low-season periods.
* Evaluate high-priced outliers in premium categories to ensure pricing aligns with market expectations and doesn't deter conversion.
* Re-engage lost customers through personalized remarketing or adjusted pricing strategies specifically designed for returning users.

#### **2. Conversion & Funnel Efficiency**
* Optimize inventory levels for high-performing categories (Outerwear & Coats, Jeans, and Sweaters) while deprioritizing low-demand items like Clothing Sets.
* Leverage the high volume of Intimates (over 1,000 orders) as a gateway for cross-selling or bundling with high-margin items.
* Implement a VIP/Loyalty Program for repeat customers to stabilize their spending volatility and capitalize on their high AOV potential.
* Double down on the high-performing Search channel to capture existing demand, while re-evaluating the Display ads budget to find more cost-effective ways of acquiring new customers to ensure a healthy long-term sales funnel.

#### **3. Market Level Retention**
* Maintain China’s market leadership by implementing country-specific retention strategies to mitigate the high churn volume while sustaining its massive active user base.
* Conduct a market re-evaluation for Austria and Colombia. Given the small user base and high churn rate in Colombia, the focus should shift from simple expansion to identifying product-market fit or testing localized marketing campaigns to establish a viable initial foothold.

#### **4. Category Return Performance**
* Review category with return rates >10% by improving size guides and product descriptions to prevent revenue loss.
* Strengthen quality control across all categories and for high-priced items, as frequent returns on these products significantly increase operational costs and hurt net profit.


## Assumptions and Caveats:

Throughout the analysis, several assumptions were made to address data challenges and ensure accuracy. These assumptions and caveats are noted below:
* Duplicate records identified within the email data were removed to ensure only one unique record per customer entity, retaining the most relevant data point.
* To maintain data integrity, missing values in Brand Name and Product Name were imputed with default values: 'Unknown_Brand' and 'Unnamed Product', respectively.
* Significant price outliers were identified in specific categories with the highest price deltas. These were kept in the analysis but warrant further investigation to determine whether they represent luxury, high-margin items or data entry errors.
* Return rates for the most recent period may be subject to change, as the standard 30-day return window may not have fully closed.
* All financial metrics are analyzed in USD and do not account for global currency fluctuations in international markets.
