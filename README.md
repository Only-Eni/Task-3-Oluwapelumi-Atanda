# 🗄️ DecodeLabs: Phase 3 SQL Data Architecture

## 📌 Project Overview
This repository contains my Week 3 deliverables for the DecodeLabs Data Analytics Internship. The objective of this phase was to transition from flat-file Exploratory Data Analysis (EDA) to relational database querying using SQL Server. 

The focus was on utilizing declarative SQL to extract dynamic business intelligence, validate structural data integrity, and isolate operational bottlenecks without permanently altering the raw database structure.

## 🏆 Key Architectural Wins
1. **Isolated UI vs. Operational Leaks:** Mathematically separated Cart Abandonment losses (Tablets bleeding $174k+) from Back-End Cancellation losses (Chairs bleeding $48k+) using pre- and post-aggregation filters (`WHERE` vs. `HAVING`).
2. **Exposed Payment Infrastructure Flaws:** Grouped cancellation data by Payment Method to prove that digital gateways (Credit Cards/Gift Cards) were failing on the backend, not standard cash-on-delivery.
3. **Validated a Synthetic Timeline:** Grouped transaction volume by Year and Month to expose a completely flatlined dataset (~38 orders/month for 2.5 years). This structural audit effectively prevents the misuse of time-series forecasting in future BI phases.
4. **Marketing ROI via Subqueries:** Deployed nested `SELECT` statements to calculate part-to-whole relationships, proving Instagram drives 21.7% of total gross revenue.

## 📂 Repository Contents
* **[`Phase3_Queries.sql`](#):** The raw SQL script containing all executed queries, structured with advanced aggregations, subqueries, and execution-order logic.
* **[`Week3_SQL_Executive_Summary.md`](#):** The strategic breakdown of the SQL findings and architectural discoveries.
