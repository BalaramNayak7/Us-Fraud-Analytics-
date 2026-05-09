# Us-Fraud-Analytics-

Objective

Built an interactive fraud analytics dashboard to monitor transaction performance, detect fraud patterns, and identify high-risk customers and regions for better decision-making.

Tools & Technologies

Power BI (DAX, Data Modeling, Visualization)
SQL (Data Analysis & Validation)
Excel (Data Preparation)

Key KPIs

Total Transactions & Total Transaction Amount
Fraud Cases & Fraud Amount
Fraud Rate % & Success Rate %
Avg Transaction Amount & Avg Fraud Amount

Dashboard Pages

1️⃣ Transactions Overview

Monthly trend of Total vs Fraud Amount
Transaction distribution by type (Online, POS, ATM)
Success vs Failed transaction comparison
Top states by transaction volume

2️⃣ Fraud Analysis

Fraud trend with MoM growth
Top states contributing to fraud
Fraud distribution by transaction type
High-value transaction impact on fraud

3️⃣ Customer Insights

Total & high-risk customers
Avg transactions per customer
Top customers by fraud amount
Fraud contribution by customers

Key Insights

Online transactions contribute the highest fraud share
Fraud is concentrated in a few high-risk states
High-value transactions show higher fraud probability
A small group of customers drives significant fraud

SQL

SELECT 
    COUNT(CASE WHEN is_fraud = 1 THEN 1 END) * 100.0 / COUNT(*) AS fraud_rate
FROM transactions;
Top States by Fraud Cases

SELECT 
    state,
    COUNT(*) AS fraud_cases
FROM transactions
WHERE is_fraud = 1
GROUP BY state
ORDER BY fraud_cases DESC;

Outcome

Delivered a business-focused dashboard enabling quick identification of fraud trends, high-risk areas, and customer behavior, supporting data-driven risk mitigation strategies.
