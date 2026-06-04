# 🗄️ DecodeLabs: Phase 3 SQL Analysis

## 📌 Project Overview
This repository contains my Week 3 deliverables for the DecodeLabs Data Analytics Internship. The objective of this phase was to transition from flat-file Exploratory Data Analysis (EDA) to relational database querying using SQL Server. 

The focus was on utilizing declarative SQL to extract dynamic business intelligence, validate structural data integrity, and isolate operational bottlenecks without altering the raw database structure.

## 📂 Repository Contents
* **[`Phase3_Queries.sql`](Phase3_Queries.sql):** The raw SQL script containing all executed queries, structured with advanced aggregations, subqueries, and execution-order logic (WHERE vs. HAVING).
* **[`Week3_SQL_Executive_Summary.md`](Week3_SQL_Executive_Summary.md):** The strategic breakdown of the SQL findings, translating the code into actionable business insights regarding Marketing ROI, Checkout UI bottlenecks, and synthetic timeline validation.

## 🛠️ Tools & Engine 
* **Database Engine:** SQL Server (SSMS)
* **Core Concepts Deployed:** * Granularity Auditing (Min/Max/Avg)
  * Dynamic Feature Engineering (Mathematical Aggregations)
  * Execution Order Logic
  * Nested Subqueries (Part-to-Whole analysis)

## 🏆 Key Architectural Wins
1. **Isolated UI vs. Operational Leaks:** Mathematically separated Cart Abandonment losses (Tablets) from Back-End Cancellation losses (Chairs) using pre- and post-aggregation filters.
2. **Exposed Payment Infrastructure Flaws:** Grouped cancellation data by Payment Method to prove that digital gateways (Credit/Gift Cards) were failing, not standard cash-on-delivery.
3. **Validated a Synthetic Timeline:** Grouped transaction volume by Year and Month to expose a flatlined dataset, effectively preventing the misuse of time-series forecasting in future BI phases.
