# Telecom-Customer-Churn-Analysis
The Telecom customer churn analysis project demonstrates revenue, churn, service adoption, and segment analysis through technical, analytical, data storytelling skills..

## Table Of Contents

1. Dataset Background & Overview
2. Objectives 
3. Data Structure Overview (ERD)
4. Executive Summary
5. Insights Deep Dive
   - Revenue & Profitability Analysis
   - Customer Churn & Retention Analysis
   - Customer Segmentation Analysis
   - Services Adoption Analysis
6. Strategic Recommendations
7. Caveats & Assumptions <br /> 


## 1. Dataset Background and Overview

The telco customer churn dataset contains fictional company data that provides home phone and internet service to customers in an urban area of California. Originally, the data was composed of 5 files with demographics, location, population, services, and status data. For this project, the data is cleaned, validated, and transformed for data integrity and further analysis. Also, it is split into 6 tables for SQL analysis.

It provides valuable multifaceted customer data, including their demographics, geographical location, adoption of multiple services, and churn status. The dataset allows us to identify the key factors influencing customer churn and develop a strategic approach to increase the retention rate. The dataset supports achieving business goals that improve revenue growth and customer retention by understanding root causes of churn, customer segmentation, service adoption and usage patterns. The data source from Kaggle originated from the IBM TechXchange Community blog.

👉 Source Dataset from Kaggle: 
https://www.kaggle.com/datasets/shilongzhuang/telecom-customer-churn-by-maven-analytics/data

👉 Data cleaning log document included a data dictionary + Link <br /> 


## 2. Objectives

- Define business KPIs & metrics aligned with business goals.
- Identify revenue stream and profitability across customer segments.
- Analyze the root causes of churn drivers, early churn risk customers, and prioritize retention strategies.
- Evaluate service performance to identify which service combinations generate high revenue and which customer - segments have cross-sell potential.
- Segment customers by revenue contribution and service adoption to tailor customer support. <br /> 


## 3. Data Structure Overview (ERD)

The data entity relationship diagram is created in a brief format using three columns and primary and foreign keys. 

<img width="685" height="579" alt="ERD_telcom_churn_data" src="https://github.com/user-attachments/assets/2205ec07-bed8-4550-96bf-253133b4f87f" />

👉 Entity Relationship Diagram (ERD) created on draw.io

👉 SQL query for data preparation: cleaning, validation, transformation and analysis + GitHub


## 4. Executive Summary 

<img width="1039" height="639" alt="telco_executive_dashboard" src="https://github.com/user-attachments/assets/f1b47b05-9c23-49ca-949b-9fb63bb32018" />

- Churn remains a significant growth constraint: A 26.56% churn rate means more than one in four customers leave. Competition and higher monthly charges are the primary drivers, indicating weak price-value perception.
  **Action**: Benchmark competitor offers, strengthen value-based pricing, and introduce targeted retention incentives for high-charge customers.
  
- Revenue concentration creates geographic risk: Los Angeles and San Diego contribute a large share of revenue. San Diego is especially concerning because churned revenue exceeds retained revenue, driven by service dissatisfaction and competition. **Action**: Launch a San Diego retention program focused on service recovery, customer feedback, and competitive win-back offers.

- Low service adoption increases churn exposure: Customers with limited service adoption churn more across internet types, while medium-adoption fibre-optic customers show the highest churn rate.
  **Action**: Promote relevant add-ons, onboarding education, and bundled services that increase product engagement and perceived value.
  
- Pricing must reflect customer usage: High monthly charges are associated with higher churn, particularly among low-data users, while heavy-data users retain more frequently.
  **Action**: Create usage-based plans, downgrade options, and proactive alerts for customers paying more than their consumption justifies.
  
- Month-to-month contracts represent the largest financial risk: These customers account for 88.36% of churned customers and 67.31% of churned revenue.
  **Action**: Prioritize contract migration campaigns using loyalty discounts, price guarantees, and annual-plan incentives.
  
- Retention strategies should reflect customer value: Bronze customers have the highest churn rate at 45.23% but the lowest estimated CLV, while Platinum customers have lower churn at 14.85% but the highest CLV.
  **Action**: Use scalable, low-cost retention for Bronze customers and high-touch, proactive account management for Platinum customers.

👉 Executive Summary Dashboard on Tableau + Link: https://public.tableau.com/app/profile/wonhee.lee/viz/TelecomExecutiveSummaryDashboard/ExecutiveSummary

## 5. Insights Deep Dive

### 5-1 Revenue & Profitability Analysis

<img width="1037" height="638" alt="telco_revenue_dashboard" src="https://github.com/user-attachments/assets/5cdf88bd-72cd-4bad-a113-08a6c1fd3f34" />

- Revenue remains strong but is partially exposed to churn risk. Total revenue is $21.04 million, while $3.97M (approximately 19%) is at risk. Gross revenue of $21.06M was reduced by only $13,438 in refunds, indicating that refunds have minimal impact on overall profitability. Revenue per customer is $3,039.
- Long-tenure customers are the primary revenue engine. Customers with more than four years of tenure contribute 65% of total revenue, demonstrating the significant financial value of long-term retention. Within this segment, two-year contract customers alone generate 37% of total revenue, showing that contractual commitment and customer longevity are closely connected to revenue stability.
- Revenue is concentrated among highly engaged, high-value customers. Loyal lifecycle customers, platinum-value customers and customers with high service adoption collectively account for 54% of total revenue. This indicates that profitability depends heavily on customers who maintain long relationships, purchase multiple services and generate above-average lifetime value.
- Refund exposure is financially small but concentrated among existing customers. The refund rate is only 0.06%, yet approximately 80% of refunds involve retained customers. High-service-adoption customers account for 53% of refunds, while gold customers represent the largest refund share at 34.69%.

👉 Revenue Dashboard on Tableau 

### 5-2 Customer Churn & Retention Analysis

<img width="1166" height="637" alt="telco_churn_dashboard" src="https://github.com/user-attachments/assets/bc245d47-a392-47f3-8636-4f3918ed297f" />

- Churn represents a material financial risk. Of 6,923 customers, 1,839 have churned, producing a 26.56% churn rate, $3.65 million in lost revenue and $3.97 million in remaining at-risk revenue.
- The first six months are the most vulnerable stage. Early-tenure customers account for 41% of churned customers, while new lifecycle customers show the highest churn rate at 53%. Although their current revenue contribution is lower, this pattern limits future customer lifetime value.
- Revenue exposure shifts as customers mature. Loyal customers have churn below 10%, but their larger accumulated value creates substantial revenue exposure when churn occurs. This distinguishes high churn probability from high financial impact.
- Competition, service dissatisfaction and pricing are the leading churn drivers. Churned customers also pay higher average monthly charges than retained customers, suggesting that perceived value may not justify pricing.
- Low product engagement is strongly associated with churn. Low-adoption customers churn at approximately 44%–45%, regardless of unlimited-data status, compared with roughly 25% among high-adoption customers.
- Contract flexibility carries significant churn risk. Month-to-month customers have a 46% churn rate and represent over 88% of all churn, far exceeding longer-term contracts.
- Risk is financially concentrated. The high-risk, high-value segment contains 346 customers and exposes $2.28 million, making it the most commercially significant churn segment.

👉 Customer churn and retention Dashboard on Tableau  

### 5-3 Customer Segments Analysis

<img width="1169" height="628" alt="telco_customer_dashboard" src="https://github.com/user-attachments/assets/baad7103-4774-4e98-8123-80faf92dd270" />

- Customer value is strongly linked to retention and lifetime economics. The average estimated CLV is $2,284, and high-value customers represent 25% of the customer base with a relatively low 14.85% churn rate, indicating that higher-value segments tend to be more stable and financially durable.
- Lower-value customers show weaker long-term potential. Customer value tiers with higher churn rates also show lower CLV estimation, suggesting that churn risk and limited revenue depth are concentrated in less valuable customer groups.
- Family status reveals clear revenue concentration. Couples without dependents generate the highest revenue at $8.7M and contain the largest loyal customer base, while singles without dependents contribute around $7M, making these household profiles major revenue anchors.
- Premium lifecycle-value alignment drives superior monetization. Platinum customers in the loyal lifecycle tier generate $7,619 revenue per customer, showing the strongest combination of loyalty, value and profitability.
- Single, low-data-usage customers represent a broad growth pool. This segment has the largest customer count at 1,342 and the highest total service count at 7,747, indicating substantial embedded revenue potential.
- Tenure risk is front-loaded. Early-tenure customers account for 19.38% of total customers in high-risk segments, while customers over four years show much lower high-risk density despite having the largest customer base.

👉 Customer Segments Performance Dashboard on Tableau  

### 5-4 Services Adoption Analysis

<img width="1169" height="627" alt="telco_service_dashboard" src="https://github.com/user-attachments/assets/e19def46-c73c-44eb-b2b6-f93cdf7d8dcf" />

- Service adoption is a major revenue engine. Across 6,923 customers, average adoption is 5.17 services, while multi-service customers generate 84.98% of the $21.04 million total revenue. High-adoption customers represent 46.94% of the customer base.
- Value and engagement are strongly connected. Platinum customers with high service adoption contribute 56% of revenue, showing that the most valuable relationships are concentrated among customers using multiple products.
- Core connectivity creates the foundation for monetization. Phone service exceeds 90% adoption, internet reaches 78%, and unlimited data reaches 67% among internet customers. Customers combining phone and internet generate twice the revenue per customer of single-connectivity users and contribute 85% of revenue from 69% of customers.
- Add-on services increase customer value. Device protection delivers the highest revenue per customer at $4,921, with 85% adoption among high-adoption customers, indicating a strong relationship between protection services and higher-value accounts.
- High adoption produces superior economics. This tier generates $15.78 million, revenue per customer of $4,857, and estimated CLTV of $3,837. However, the medium-adoption tier records the highest churn rate at 40.9%, revealing a vulnerable transition stage.
- Streaming bundles show strong monetization. Customers using all three streaming services represent 23.69% of customers but contribute 41.29% of revenue, with revenue per customer exceeding $5,295.

👉 Service Adoption Performance Dashboard on Tableau 


## 6. Strategic Recommendations

### 6-1 Customer Success and Retention Teams:

- Prioritize the $3.97 million in at-risk revenue, especially among high-value, long-tenure customers. Use proactive account reviews, early-warning churn indicators and personalized retention outreach to protect the revenue base most critical to profitability.
- Treat the medium-adoption tier as the main intervention segment because its 40.9% churn rate signals weak engagement during the transition to multi-service usage. Use onboarding support, service education and proactive experience checks to strengthen perceived value.
- Prioritize early-tenure customers, especially those within high-risk contract and lifecycle segments, because churn risk is front-loaded at the beginning of the relationship. Strengthen onboarding, first-bill support and early engagement monitoring to prevent low-CLV customers from churning before they mature.

### 6-2 Product, Commercial, Marketing and Growth Teams:

- Strengthen migration toward two-year contracts and higher service adoption through bundled plans, loyalty benefits and targeted cross-selling. Because long-tenure, highly engaged customers generate most revenue, increasing contract commitment and product usage can improve customer lifetime value and revenue stability.
- Accelerate cross-selling from single-service and medium-adoption customers into phone–internet bundles, unlimited data, device protection and streaming packages. Prioritize offers based on current usage and customer value to increase services per customer and revenue concentration.
- Build targeted growth campaigns around high-potential household segments, especially single low-data-usage customers and couples without dependents. These groups show strong customer volume, service count and revenue potential, making them suitable for personalized cross-sell and bundle expansion.

### 6-3 Commercial, Pricing, Finance, and Customer Experience: 

- Investigate refund patterns among retained, gold-tier and high-adoption customers. Although the overall refund rate is only 0.06%, its concentration among valuable customers may indicate billing complexity, service-quality issues or unmet expectations. Track refund reasons and recurring service complaints to prevent dissatisfaction from becoming future churn.
- Reduce month-to-month and price-related churn by offering targeted incentives to migrate suitable customers to longer contracts. Review competitor pricing, monthly-charge fairness and recurring service complaints, since month-to-month customers generate over 88% of churn, and churned customers pay higher average monthly charges.
- Protect platinum, high-adoption and dual-connectivity customers, who generate a disproportionate share of revenue. Develop differentiated loyalty benefits and account monitoring for high-risk, high-value customers while measuring cross-sell success through adoption uplift, revenue per customer, CLTV and churn.
  

## 7. Appendix

### 7-1 Caveats And Assumptions

- The dataset does not include a date column, which limits the ability to analyze historical trends or measure revenue growth on a month-over-month (MoM) or year-over-year (YoY) basis.
- Customer Lifetime Value (CLV) is an estimate based on a simplified, business-oriented formula because the dataset does not contain profit margin, customer acquisition cost, or complete historical transaction data.

  For this analysis, CLV is calculated as: **Estimated CLV = Monthly Charge * Tenure In Months**
  
- The period in Tenure In Months represents the total months retained in the telecom company, and it is used as a customer lifetime value. 
- The Stakeholders referenced in the strategic recommendations are hypothetical and were assigned based on a simulated telecom company scenario. They do not represent confirmed stakeholders from an actual telecom company.

### 7-2 Tech Stack Used

- **Data Preparation**: Excel & Power Query Editor, SQLite, Python, VS Code
- **BI tool**:  Tableau
- **AI-assisted**: ChatGPT, Copilot, Gemini


  👩‍💻 Welcome constructive feedbacks or opinions on my project.

