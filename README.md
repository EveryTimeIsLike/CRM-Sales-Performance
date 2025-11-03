💼 CRM Sales Performance Analysis

Project Overview
This project analyzes end-to-end sales performance for a global B2B software company using CRM data.
The goal was to understand sales efficiency, product profitability, and customer value — ultimately helping leadership identify top performers and streamline the sales funnel.

🎯 Business Objectives

Measure overall pipeline health — deal flow, conversion rate, and cycle time.
Evaluate agent and manager performance across offices and regions.
Analyze product portfolio profitability and pricing integrity.
Assess customer account structure and revenue concentration.

🧩 Data & Preparation

Datasets Used:
sales_pipeline.csv – Opportunities, deal stages, product sold, revenue.
sales_teams.csv – Sales agents, managers, and regional offices.
products.csv – Product details and series.
accounts.csv – Customer data, revenue, and company hierarchy.
data_dictionary.csv – Metadata and field definitions.

Data Preparation Steps:

Cleaned and validated field formats (engage_date, close_date, numeric consistency).
Joined datasets in BigQuery for a unified sales data model.
Created CTEs for time-to-close metrics and deal-stage breakdowns.
Standardized product names and removed nulls for consistent aggregation.

⚙️ Analytical Approach & SQL Highlights

Objective 1 – Pipeline Metrics
Opportunities created per month (EXTRACT(Month FROM engage_date)) to identify demand peaks.
Average deal duration for Won, Lost, and Open deals using DATE_DIFF().
Deal-stage distribution with % share and lost ratio.
Product-level win rates to highlight strong offerings.

Objective 2 – Sales Agent Performance
Win rate and revenue per sales agent to rank top performers.
Manager-level aggregation for leadership benchmarking.
Regional performance for key product (GTX Plus Pro).

Objective 3 – Product Analysis
Top product by revenue vs units sold (March focus).
Average gap between sales_price and close_value to detect pricing data issues.
Revenue by product series for portfolio prioritization.

Objective 4 – Account Analysis
Revenue by office location to find underperforming markets.
Gap in years between oldest and newest customers (MIN/MAX(year_established)).
Subsidiaries with most lost opportunities.
Consolidated revenue for parent companies (e.g., Acme Corporation + subsidiaries).

📈 Key Insights

Top 3 agents achieved >65 % win rate, far above company average (~40 %).
West regional office led both win rate and revenue share.
Several products showed >20 % variance between sales and close value, suggesting CRM pricing data quality issues.
70 % of total revenue was concentrated in <20 % of customer accounts (Pareto distribution).
Acme Corporation group was the top customer when subsidiaries were consolidated.

💡 Business Impact

✅ Standardized sales performance KPIs across all teams.
✅ Improved forecast accuracy and pipeline visibility.
✅ Revealed underperforming regions and pricing inconsistencies.
✅ Informed future sales incentive design and regional strategy.

🛠️ Tools & Skills

Database	Google BigQuery
Query Language	SQL (CTEs, Window Functions, Aggregations, Joins)
BI & Visualization	Power BI
Analysis Focus	Sales Funnel, Win Rate, Product Profitability, Account Value
Business Skills	Revenue Optimization, Forecasting, Stakeholder Reporting
