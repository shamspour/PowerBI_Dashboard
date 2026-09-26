# Sales Performance & Profitability Analysis

## Project Overview

This Power BI project analyzes sales performance across products, customers, geographic markets, transaction types, and time periods.

The objective is to understand what drives revenue and profitability, identify meaningful differences across sales segments, and examine how performance changes throughout the year.

The analysis is based on **10,000 sales transactions from 2023**, covering **200 customers and 40 product IDs**.

![Dashboard Overview](Images/overview.gif)

### Interactive Dashboard

[Open the report in Power BI Service](https://app.powerbi.com/view?r=eyJrIjoiMDNmMTZhOWItNTAwOC00ODE4LTljNjItODAyM2Y3NjA2MWJjIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9)

---

## Business Question

**What drives revenue and profitability across products, transaction types, markets, and time?**

The analysis focuses on three questions:

- Which products and customers contribute most to revenue and profit?
- How does performance differ across transaction types and geographic markets?
- How does sales performance change across months, quarters, and weekdays?

---

## Dataset

The project uses a pharmaceutical sales dataset containing transaction-level sales records together with customer and product information.

After data-quality checks, the analytical dataset contains:

| Metric | Scope |
|---|---:|
| Transactions | 10,000 |
| Customers | 200 |
| Product IDs | 40 |
| Units Sold | 151,713 |
| Analysis Period | Jan–Dec 2023 |

The model combines:

- Sales transactions: customer, product, date, units sold, and transaction type
- Customer attributes: country, age, and gender
- Product attributes: product name, selling price, and production cost
- Calendar attributes: month, quarter, and weekday

---

## Data Preparation & Modeling

The data was prepared in **Power Query** and structured using a star-schema approach.

Key preparation and modeling steps included:

- validating transaction records and data completeness
- checking duplicates and inconsistent records
- standardizing data types and dates
- creating a dedicated calendar table
- establishing relationships between sales, customer, product, and date tables
- creating reusable DAX measures for KPIs and time-based comparisons

---

## Key Metrics

The report tracks:

**Revenue · Profit · COGS · Profit Margin · Units Sold · Transactions · Customers**

Additional DAX logic supports:

- Month-over-Month comparisons
- dynamic Top-N and Bottom-N rankings
- product and customer ranking
- contribution-to-total analysis
- switching between Revenue, Profit, Transactions, and Units

---

## Analysis

### 1. Sales Performance & Profitability

This page evaluates product and customer performance across multiple commercial KPIs rather than relying on revenue alone.

Dynamic Top-N and Bottom-N rankings allow products and customers to be compared by Revenue, Profit, Transactions, or Units Sold.

![Sales Performance](Images/1.gif)

### Key finding

The Top 10 product IDs generate approximately **41% of total revenue**.

**Doxycycline** is the highest-revenue product at approximately **$2.15M**, but represents only around **5.3% of total revenue**, indicating that sales are distributed across several products rather than dominated by a single product.

---

## 2. Customer & Market Segments

This analysis compares transaction types, geographic markets, and customer characteristics.

The strongest commercial difference appears between **Seller-type** and **User-type transactions**.

![Customer and Market Segments](Images/2.gif)

### Key findings

- Seller-type transactions represent only **24.95% of transactions** but generate approximately **87.55% of total revenue**.
- Seller transactions average approximately **53.3 units per transaction**, compared with **2.5 units** for User transactions.
- Canada and Australia together account for approximately **65.7% of revenue**.
- However, these markets also represent roughly two-thirds of the customer base, suggesting that geographic revenue concentration is largely associated with customer distribution rather than substantially higher revenue per customer.
- The Top 10 customers generate only approximately **8.9% of total revenue**, indicating relatively low dependence on a small group of individual customers.

---

## 3. Sales Trends

The final page examines monthly, quarterly, and weekday performance during 2023.

![Sales Trends](Images/3.gif)

### Key findings

Monthly revenue shows noticeable short-term variation:

- largest Month-over-Month increase: **September, approximately +23.3%**
- largest Month-over-Month decrease: **February, approximately −22.4%**

Quarterly revenue increases from approximately **$9.67M in Q1** to **$10.48M in Q4**, representing an increase of roughly **8.5%**.

Because the validated dataset contains one full year, these patterns are interpreted as **monthly and quarterly performance variation rather than evidence of long-term seasonality**.

---

## Key Insights

1. **Transaction type is a major revenue driver.**  
   Seller-type transactions generate 87.55% of revenue while accounting for only 24.95% of transactions.

2. **Revenue is distributed across multiple products.**  
   The Top 10 products generate approximately 41% of revenue, while the leading product contributes only about 5.3%.

3. **Geographic concentration should be interpreted carefully.**  
   Canada and Australia dominate revenue largely because they also contain a large share of customers.

4. **Individual-customer concentration is relatively low.**  
   The Top 10 customers account for only around 8.9% of revenue.

5. **Monthly volatility is greater than quarterly variation.**  
   Individual months show sizeable changes, while quarterly performance remains comparatively stable.

---

## Tools & Technical Skills

**Power BI**
- interactive dashboard development
- slicers and cross-filtering
- dynamic ranking
- field parameters
- report navigation

**Power Query**
- data cleaning
- data transformation
- type validation
- calendar preparation

**DAX**
- Revenue
- Profit
- COGS
- Profit Margin
- Month-over-Month comparison
- Top/Bottom ranking
- contribution analysis
- context-aware calculations

**Data Modeling**
- star schema
- fact and dimension tables
- relationships
- dedicated measure table

---

## Limitations

This project is a portfolio case study rather than an analysis of a real pharmaceutical company.

The validated dataset covers **one full year (2023)**. Monthly and quarterly patterns can therefore be analyzed, but the dataset is not sufficient to establish multi-year seasonality or long-term market trends.

Customer demographic variables are used descriptively and should not be interpreted as evidence of preferences, motivations, or causal purchasing behavior.

The analysis identifies patterns and associations in the available data and does not establish causal relationships.

---

## Data Source & Attribution

The dataset was adapted from material associated with the YouTube tutorial **Power BI Sales Dashboard**.

The original dataset served as the starting point for the project. The portfolio analysis, business framing, KPI interpretation, findings, and documentation were developed as part of this independent analytics case study.

[Original Tutorial](https://www.youtube.com/watch?v=ovQ9czcvotk)
