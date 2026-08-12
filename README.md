# Saas-customer-churn-revenue-risk-analysis
End-to-end SaaS customer churn and revenue risk analysis using Python, Pandas, and Power BI to identify churn trends, At-Risk MRR, high-value customer segments, and retention priorities.

# SaaS Customer Churn & Revenue Risk Analysis

## 📌 Project Overview

This project analyzes customer churn and recurring revenue risk for a SaaS business using Python, Pandas, and Power BI.

The analysis combines customer accounts, subscriptions, churn events, product usage, and support ticket data to identify churn patterns, revenue exposure, high-value customer segments, and retention priorities.

The goal is not only to understand **how many customers are churning**, but also to determine **where the greatest financial risk exists and which customers should be prioritized for retention.**

---

## 🎯 Business Problem

Customer churn can have a significant impact on recurring SaaS revenue. However, the number of churned customers alone does not fully represent the financial impact.

A small number of high-value customers can represent substantially more revenue risk than a large number of low-value customers.

This analysis therefore focuses on two key areas:

- Customer churn
- Revenue exposed to churn

The project aims to help business teams identify the customer segments and markets where retention efforts can have the greatest financial impact.

---

## 🔍 Key Business Questions

The analysis addresses the following questions:

1. How is customer churn changing over time?
2. How much recurring revenue is currently at risk?
3. Which subscription plan contributes the most At-Risk MRR?
4. Which countries have the highest concentration of churned customers?
5. Is revenue risk growing faster than the customer base?
6. Which high-value customer segments should be prioritized for retention?
7. Where should the business focus its customer retention efforts?

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **Jupyter Notebook**
- **Power BI**
- **DAX**
- **Microsoft Excel / CSV**

---

## 📂 Dataset

The project uses multiple SaaS business datasets covering:

- Customer accounts
- Subscription plans
- Churn events
- Product feature usage
- Customer support tickets

These datasets were combined to create a consolidated analytical dataset for Power BI.

### Source Tables

- `ravenstack_accounts.csv`
- `ravenstack_subscriptions.csv`
- `ravenstack_churn_events.csv`
- `ravenstack_feature_usage.csv`
- `ravenstack_support_tickets.csv`

---

## 🧹 Data Preparation

The raw datasets were first audited and prepared using Python and Pandas.

The data preparation process included:

- Inspecting dataset structure
- Checking data types
- Identifying missing values
- Checking duplicate records
- Reviewing categorical values
- Validating customer identifiers
- Cleaning inconsistent fields
- Converting date fields
- Joining multiple datasets
- Creating the consolidated analytical dataset
- Preparing data for Power BI analysis

The complete data preparation workflow is available in:

`notebooks/01_SaaS_Churn_Data_Audit.ipynb`

The cleaned dataset used for Power BI is available in:

`cleaned_data/df_master_powerbi.csv`

---

## 📊 Power BI Dashboard

The Power BI dashboard provides an executive-level view of customer churn and revenue exposure.

### Dashboard KPIs

- Active Accounts
- Churn Rate %
- At-Risk MRR
- Year-over-Year changes

### Dashboard Visuals

- Monthly Churn Rate trend
- Churned Accounts by Country
- At-Risk MRR by Plan Tier
- Executive Insights panel

The dashboard is designed to answer the key management question:

> **Where is customer churn creating the greatest financial risk, and where should retention efforts be focused?**

---

## 💡 Key Insights

### 1. Revenue risk is growing faster than the customer base

In 2024, Active Accounts increased by approximately **17.3% YoY**, while At-Risk MRR increased by approximately **25.0% YoY**.

This indicates that revenue exposure is growing faster than the customer base.

**Business implication:**  
The company should focus not only on reducing the number of churned customers, but also on protecting higher-value recurring revenue.

---

### 2. Enterprise customers represent the largest revenue exposure

Enterprise customers account for approximately **73% of At-Risk MRR**, representing about **$1.08M** of revenue exposure in 2024.

**Business implication:**  
Enterprise customers should be a primary focus of retention efforts because preventing churn within this segment can protect significantly more recurring revenue.

---

### 3. The United States has the highest churn concentration

The United States has the largest number of churned accounts compared with the other countries shown in the dashboard.

Churned US accounts increased from **128 in 2023 to 160 in 2024**.

**Business implication:**  
The US market should be investigated further to identify the underlying drivers of customer churn.

---

### 4. Churn remains a significant retention challenge

The overall churn rate in 2024 was approximately **9.84%**, compared with approximately **9.58% in 2023**.

Although the increase is relatively small, the combination of higher churn and increased At-Risk MRR creates a more significant revenue protection challenge.

---

### 5. Retention should be value-based

The analysis demonstrates why customer count alone is not enough to evaluate churn risk.

A business should prioritize customers based on:

- Revenue contribution
- Subscription plan
- Churn risk
- Customer value
- Usage patterns
- Support activity

This allows retention teams to focus their resources on customers where intervention can have the greatest financial impact.

---

## 🎯 Business Recommendations

Based on the analysis, the following actions are recommended:

### Prioritize Enterprise Customers

Develop targeted retention strategies for high-value Enterprise accounts because they represent the largest share of At-Risk MRR.

### Investigate US Churn Drivers

Conduct deeper analysis of US customers to identify whether churn is associated with:

- Product usage
- Support activity
- Subscription characteristics
- Customer engagement
- Other behavioral patterns

### Focus on Revenue Protection

Track At-Risk MRR alongside churn rate to ensure that retention strategies focus on financial impact rather than customer volume alone.

### Build Targeted Retention Lists

Use customer-level risk analysis to identify high-value accounts that require proactive intervention.

The project includes:

`analysis/high_risk_accounts_action_list.csv`

which can support targeted retention actions.

---

## 📈 Year-over-Year Analysis

The project compares 2023 and 2024 to understand how customer growth and revenue risk changed over time.

| Metric | 2023 | 2024 |
|---|---:|---:|
| Active Accounts | 2.08K | 2.44K |
| Churn Rate | 9.58% | 9.84% |
| At-Risk MRR | $1.18M | $1.47M |
| Active Account Growth | — | +17.3% YoY |
| At-Risk MRR Growth | — | +25.0% YoY |

The comparison highlights an important business concern:

> **Revenue exposure is increasing faster than the customer base.**

---

## 📁 Project Structure

```text
saas-customer-churn-revenue-risk-analysis/
│
├── analysis/
│   └── high_risk_accounts_action_list.csv
│
├── data/
│   ├── ravenstack_accounts.csv
│   ├── ravenstack_churn_events.csv
│   ├── ravenstack_feature_usage.csv
│   ├── ravenstack_subscriptions.csv
│   └── ravenstack_support_tickets.csv
│
├── cleaned_data/
│   └── df_master_powerbi.csv
│
├── notebooks/
│   └── 01_SaaS_Churn_Data_Audit.ipynb
│
├── screenshots/
│   ├── dashboard_overview.png
│   ├── data_cleaning.png
│   └── data_model.png
│
└── README.md
