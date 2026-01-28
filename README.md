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

An interactive Tableau dashboard used to report and explore sales trends can be found [here](https://public.tableau.com/views/RevenueGrowth2025/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).



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
  <img width="1199" height="599" alt="Dashboard 1 (9)" src="https://github.com/user-attachments/assets/d8f26eff-5d67-49d6-a868-f1e9380fbc81" />

</p>

#### **1. Revenue Growth and Market Dominance**
* Sales grew consistently throughout 2025, with China emerging as the primary market leader, indicating significant dominance in the APAC region.
* December recorded the highest growth, with a 23% increase compared to the previous month, marking it the best-performing period of the year.

#### **2. Quarterly Insights and Seasonal Trends**
* The fourth quarter showed exceptional performance, driven by seasonal shopping trends and year-end marketing campaigns. Outerwear and Coats were identified as the top-performing categories during this period.
* Conversely, revenue saw a sharp 6.5% decline in February, identifying it as a weak period that requires further strategic attention compared to the year-end surge.

#### **3. Strategic Recommendations**
* Leverage the strong brand presence in China by developing more localized marketing campaigns to further solidify market share in the APAC region.
* To sustain momentum during peak seasons (like Q4), implement targeted loyalty programs focusing on high-performing categories such as Outerwear.
* Investigate the February slump to identify external factors (competition/market shifts) and reassess pricing and promotion strategies to regain momentum earlier in the year.

## Insights Deep Dive
### Revenue & Transaction Value

<img width="1199" height="599" alt="Dashboard 1 (19)" src="https://github.com/user-attachments/assets/c4980119-08b1-4fa4-93ba-c024df3a5b49" />

#### **1. Total Sales**
* Total sales experienced a consistent upward trend throughout the year.
* December emerged as the strongest month with $139,414 in sales and 1,592 unique buyers, likely driven by holiday shopping. On the other hand, February recorded the lowest performance with $59,336 in sales from 698 unique buyers.
* The average monthly sales for the year stood at $87,481.

#### **2. Average Order Value (AOV)**
* The Average Order Value (AOV) remained relatively stable throughout the year, with only minor fluctuations around the $59.992 average.
* The value peaked in August at 63.410 and saw its lowest point in February at 56.800, indicating consistent customer spending behavior despite changes in total sales volume.

#### **3. Number of Orders**
* Order volume closely follows sales trends, confirming that revenue growth is primarily driven by an increase in transaction count rather than just higher pricing.
* December reached a peak of 2,326 orders, while February remained the lowest with 1,018 orders. The monthly average for the year was 1,458 orders.
* While spending per order (AOV) was stable, the steady growth in order frequency was the main driver for the overall increase in total revenue.

<img width="1199" height="599" alt="Dashboard 1 (21)" src="https://github.com/user-attachments/assets/b5fcb346-30b1-403f-87f6-615efd5995bd" />


* The monthly AOV indicates a stable basket size throughout the year, suggesting consistent consumer spending. However, a deep dive into the Price Delta reveals specific "high-ticket" items within certain categories.
* For instance, in the Shorts category, there is a significant outlier with a price delta of $953.23 above the category average of $45.77. Similarly, the Outerwear & Coats category features premium items retailing at $903.00, representing a price delta $756.98 higher than the category average of $146.02.

### Conversion & Funnel Efficiency 

<img width="1199" height="599" alt="Dashboard 1 (22)" src="https://github.com/user-attachments/assets/83ef27c0-d60d-48f9-b0d9-4009821f47e5" />

* Outerwear & Coats consistently led sales over the year, exceeding $129,269 with 871 orders. This suggests a premium pricing strategy, as it generates the highest revenue despite having fewer orders than other top categories.
* Jeans and Sweaters secured the second and third positions, generating $123,552 (1,242 orders) and $82,425 (1,074 orders) respectively, showing strong market demand.
* Clothing Sets recorded the lowest performance with only $2,221 in revenue and 28 orders, indicating a potential need for assortment review or marketing focus.
* In terms of transaction frequency, Intimates outperformed all other categories with 1,338 orders, despite not breaking into the Top 10 by revenue. This indicates a high-volume, low-margin product profile.

<img width="1199" height="599" alt="Dashboard 1 (16)" src="https://github.com/user-attachments/assets/514753c2-dedf-4590-8321-af851bea24ea" />

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

<img width="1199" height="599" alt="Dashboard 1 (17)" src="https://github.com/user-attachments/assets/207be02d-6b1a-40e0-a12f-e5577e0ef83c" />

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

### Customer Loyalty & Retention

<img width="1199" height="599" alt="Dashboard 1 (13)" src="https://github.com/user-attachments/assets/c802a47a-ddb4-44c6-90a4-d5cfd68749d7" />

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

### Quality & Operational Excellence

<img width="1199" height="599" alt="Dashboard 1 (12)" src="https://github.com/user-attachments/assets/ab556c31-d2c2-4a70-a713-35655cf4be1f" />

## Recommendations:

Based on the insights and findings above, we would recommend the [stakeholder team] to consider the following: 

* Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
* Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
* Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
* Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
* Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  


## Assumptions and Caveats:

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

* Assumption 1 (ex: missing country records were for customers based in the US, and were re-coded to be US citizens)
  
* Assumption 1 (ex: data for December 2021 was missing - this was imputed using a combination of historical trends and December 2020 data)
  
* Assumption 1 (ex: because 3% of the refund date column contained non-sensical dates, these were excluded from the analysis)
