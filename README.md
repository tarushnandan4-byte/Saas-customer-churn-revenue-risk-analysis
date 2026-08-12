# Saas-customer-churn-revenue-risk-analysis
End-to-end SaaS customer churn and revenue risk analysis using Python, Pandas, and Power BI to identify churn trends, At-Risk MRR, high-value customer segments, and retention priorities.

# SaaS Customer Churn & Revenue Risk Analysis

![Dashboard Executive Overview](screenshots/dashboard_overview.png)
*(Note: Make sure your image filename inside the `screenshots` folder matches this link)*

## 📌 Business Overview & Problem
In B2B SaaS models, customer retention directly dictates long-term enterprise valuation and Monthly Recurring Revenue (MRR) predictability. This project evaluates churn drivers, revenue exposure, and usage metrics across 5,000 customer accounts to identify leading indicators of customer attrition and prioritize retention efforts.

### Key Business Questions Addressed
* **Logo vs. Revenue Exposure:** Is account loss aligned with MRR loss, or are high-value enterprise accounts churning?
* **Root-Cause Friction:** What are the primary drivers behind account cancellations?
* **Early Warning Indicators:** Can we isolate active accounts showing warning signs before they cancel?

---

## 📊 Executive Findings & Strategy Insights

* **Revenue Leakage Exceeds Account Loss:** **Logo Churn sits at 9.72%** (2024 Executive Overview: **9.84%**), while **MRR Churn sits higher at 10.40%**, confirming revenue loss is concentrated in larger customer accounts.
* **Enterprise Risk Exposure:** Enterprise accounts represent **73.17% ($1.08M) of total At-Risk MRR**, making Enterprise retention the top strategic priority.
* **Primary Churn Drivers:**
  * 💰 **Pricing & Budget (32.5%):** Budget limits (17.3%) and pricing friction (15.2%) combined account for nearly 1 in 3 churn events.
  * ⚙️ **Product Capability Gaps (19.0%):** Missing features is the single largest individual churn reason.
  * 🎧 **Support Friction (17.3%):** Resolution turnaround times heavily influence renewal decisions.
* **Proactive Action List:** Created an automated pipeline isolating **1,205 active high-risk accounts** (low product usage coupled with open support tickets) representing **$2.65M in active MRR at risk**.

---

## 🛠️ Tech Stack & Methodology

* **Python & Pandas:** Data cleaning, multi-table relational merges (5 sources into 5,000 × 27 master table), and churn risk filtering.
* **Matplotlib & Seaborn:** Hypothesis testing, boxplots for MRR distribution, and feature correlation scatter plots.
* **Power BI:** Interactive executive dashboard with dynamic filtering by Country, Plan Tier, and Year.

---

## 📈 Key Visual Insights

### 1. Risk Exposure by Subscription Tier
Boxplot analysis highlights substantial MRR variance among Enterprise clients, confirming the need for dedicated account management for top-tier subscriptions.

![MRR Distribution](screenshots/mrr_distribution_boxplot.png)

### 2. Usage vs. Support Engagement
Evaluating usage events against support tickets shows churned customers distributed across multiple usage levels, proving attrition is driven by feature fit and pricing rather than passive inactivity.

![Usage vs Support Tickets](screenshots/usage_vs_tickets_scatter.png)

---

## 📁 Repository Structure

```text
Saas-customer-churn-revenue-risk-analysis/
│
├── analysis/               # SQL queries or additional analytical scripts
├── cleaned_data/           # Output datasets (df_master_powerbi.csv, action lists)
├── data/                   # Raw input CSV files
├── notebooks/              # Primary Jupyter Notebook (.ipynb)
├── screenshots/            # Dashboard and visualization assets
└── README.md               # Executive documentation
