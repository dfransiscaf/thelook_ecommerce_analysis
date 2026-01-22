# TheLook E-commerce Analysis



## Project Background

TheLook is a global e-commerce company that sells trendy apparel for men and women. Company's primary focus is providing a seamless online shopping experience with a wide variety of clothing categories, from casual wear to formal attire.

Established in 2019, TheLook's book of business have grown into a data-rich platform with 100.000 customers, possesses over 125.000 transactions, and generating sales revenue exceeding $2.71 milion. 

In-depth analysis is conducted to evaluate TheLook's performance over the past several years (2019-2025). This comprehensive review provides valuable insights that internal cross-functional teams will utilize to streamline processes and enchance TheLook's commercial performance. The key insights and recommendations are provided on the following key areas:

### Key Metrics & North Star Framework

- **Revenue & Transaction Value (The Value Pillar):** Monitoring Gross Merchandise Value (GMV) and total sales revenue over specific periods. This includes tracking the number of successful transactions and Average Order Value (AOV) to understand spending patterns.
- **Conversion & Funnel Efficiency (The Reach Pillar):** Evaluating the conversion rate from website visitors to completed purchases. This involves identifying "friction points" in the user journey and assessing funnel effectiveness to maximize customer acquisition and initial retention.
- **Customer Loyalty & Retention (The Stickiness Pillar):** Analyzing Customer Lifetime Value (LTV) to ensure the cost of acquisition is sustainable. This focuses on long-term profitability and reducing "One-Time Buyer" rates through repeat purchase analysis.
- **Quality & Operational Excellence (The Quality Pillar):** Analyzing product performance, market impact, and return/refund rates across different categories. This informs strategic decisions on inventory and identifies quality issues to minimize operational loss.

The SQL queries used to inspect and clean the data for this analysis can be found here [![Gist](https://img.shields.io/badge/Gist-SQL_Scripts-blue?style=for-the-badge&logo=github)](https://gist.github.com/dfransiscaf/e800ad6973e750b8945e19470b479351)

Targed SQL queries regarding various business questions can be found here [![Gist](https://img.shields.io/badge/Gist-SQL_Scripts-blue?style=for-the-badge&logo=github)](https://gist.github.com/dfransiscaf/62fa3baa3210b0265abe2e671e8c3447)

An interactive Tableau dashboard used to report and explore sales trends can be found here [link].



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

#### Overview of Findings

Explain the overarching findings, trends, and themes in 2-3 sentences here. This section should address the question: "If a stakeholder were to take away 3 main insights from your project, what are the most important things they should know?" You can put yourself in the shoes of a specific stakeholder - for example, a marketing manager or finance director - to think creatively about this section.

[Visualization, including a graph of overall trends or snapshot of a dashboard]

<p align="center">
  <img width="606" height="457" alt="Sheet 1 (1)" src="https://github.com/user-attachments/assets/08cdcc99-cf18-490c-b7c6-b57a039617e7" />
</p>

1. Revenue Growth and Peak Performance
- in 2025 sales consistently growing each quarter
- q4 is the highest revenue and making it the best performing period
2. Quarterly insights & seasional trends
- q2 and q4 of each year typically show strong performance likely due to seasonal shopping trends and marketing efforts
- q1 the revenue quickly dropped, signalling an overall weak performance compared to previous year
3. Ket takeways and recomendations
- investigate the causes of 2022 decline (e.g., market changes, competition, internal factors)
- leverage high performing periods to refine marketing and sales strategies
- reasses business strategy focusing pricing, promotions, and customer engagement to regain momentum

## Insights Deep Dive
#### Category 1:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 1]


#### Category 2:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 2]


#### Category 3:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 3]


#### Category 4:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 4]



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
