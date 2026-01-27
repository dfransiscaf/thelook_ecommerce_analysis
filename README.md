# TheLook E-commerce Analysis



## Project Background

TheLook is a global e-commerce company that sells trendy apparel for men and women. Company's primary focus is providing a seamless online shopping experience with a wide variety of clothing categories, from casual wear to formal attire.

Established in 2019, TheLook's book of business have grown into a data-rich platform with 100.000 customers, possesses over 125.000 transactions, and generating sales revenue exceeding $2.71 milion. 

In-depth analysis is conducted to evaluate TheLook's performance over the past several years (2019-2025). This comprehensive review provides valuable insights that internal cross-functional teams will utilize to streamline processes and enchance TheLook's commercial performance. The key insights and recommendations are provided on the following key areas:

## Key Metrics & North Star Framework

- **Revenue & Transaction Value (The Value Pillar):** Monitoring Gross Merchandise Value (GMV) and total sales revenue over specific periods. This includes tracking the number of successful transactions and Average Order Value (AOV) to understand spending patterns.
- **Conversion & Funnel Efficiency (The Reach Pillar):** Evaluating the conversion rate from website visitors to completed purchases. This involves identifying "friction points" in the user journey and assessing funnel effectiveness to maximize customer acquisition and initial retention.
- **Customer Loyalty & Retention (The Stickiness Pillar):** Analyzing Customer Lifetime Value (LTV) to ensure the cost of acquisition is sustainable. This focuses on long-term profitability and reducing "One-Time Buyer" rates through repeat purchase analysis.
- **Quality & Operational Excellence (The Quality Pillar):** Analyzing product performance, market impact, and return/refund rates across different categories. This informs strategic decisions on inventory and identifies quality issues to minimize operational loss.

The SQL queries used to inspect and clean the data for this analysis can be found here [![Gist](https://img.shields.io/badge/Gist-SQL_Scripts-blue?style=for-the-badge&logo=github)](https://gist.github.com/dfransiscaf/e800ad6973e750b8945e19470b479351)

Targed SQL queries regarding various business questions can be found here [![Gist](https://img.shields.io/badge/Gist-SQL_Scripts-blue?style=for-the-badge&logo=github)](https://gist.github.com/dfransiscaf/62fa3baa3210b0265abe2e671e8c3447)

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
* Sales grew consistently throughout 2025, with **China** emerging as the primary market leader, indicating significant dominance in the APAC region.
* **December** recorded the highest growth, with a **23% increase** compared to the previous month, marking it the best-performing period of the year.

#### **2. Quarterly Insights and Seasonal Trends**
* The fourth quarter showed exceptional performance, driven by seasonal shopping trends and year-end marketing campaigns. **Outerwear and Coats** were identified as the top-performing categories during this period.
* Conversely, revenue saw a sharp **6.5% decline in February**, identifying it as a weak period that requires further strategic attention compared to the year-end surge.

#### **3. Strategic Recommendations**
* Leverage the strong brand presence in China by developing more **localized marketing campaigns** to further solidify market share in the APAC region.
* To sustain momentum during peak seasons (like Q4), implement targeted **loyalty programs** focusing on high-performing categories such as Outerwear.
* Investigate the February slump to identify external factors (competition/market shifts) and reassess **pricing and promotion strategies** to regain momentum earlier in the year.

## Insights Deep Dive
### Revenue & Transaction Value

<img width="1199" height="599" alt="Dashboard 1 (10)" src="https://github.com/user-attachments/assets/2f9f8502-90f4-426b-aff9-d52516c8cb3c" />

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.


<img width="1199" height="599" alt="Dashboard 1 (3)" src="https://github.com/user-attachments/assets/3b945132-c108-4191-9a50-52aab95d2fa5" />

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

### Conversion & Funnel Efficiency 

<img width="1199" height="599" alt="Dashboard 1 (7)" src="https://github.com/user-attachments/assets/d38ab3fb-74f6-43ee-bf70-43b2a2ee9f3b" />

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

<img width="1199" height="599" alt="Dashboard 1 (11)" src="https://github.com/user-attachments/assets/2a4bb1fd-ffc3-4150-bb09-5bd7e7aa827f" />

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
