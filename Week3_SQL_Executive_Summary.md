# 🗄️ Phase 3: SQL Data Analysis & Engine Architecture

## 1. Problem Statement
The objective of this phase was to transition from flat-file observation to relational database querying. The goal was to leverage declarative SQL to validate Phase 2 insights at scale, dynamically calculate business metrics without altering raw data, and isolate specific operational and marketing bottlenecks.

## 2. Methodology & Execution Logic
* **The Granularity Audit:** Utilized `GROUP BY` and standard aggregations (`MIN`, `MAX`, `AVG`) to instantly validate structural categorization flaws across 1,200 rows.
* **Execution Order Navigation:** Successfully bypassed the "Alias Trap" by leveraging the `HAVING` clause to filter post-aggregated revenue thresholds (e.g., filtering out products generating < $25,000).
* **Dynamic Feature Engineering:** Calculated complex business metrics (Cart Abandonment Loss) entirely on the fly within the `SELECT` statement, preserving absolute database normalization and storage efficiency.
* **Subquery Architecture:** Deployed nested `SELECT` statements within mathematical calculations to determine percentage-based part-to-whole relationships.

## 3. Key Findings & Verified Insights
* **The Marketing ROI (Subquery Analysis):** Instagram is the undisputed top-performing acquisition channel, driving 21.77% of total gross revenue, followed closely by Email marketing (20.70%). 
* **The UI/UX Bleed (Cart Abandonment):** Grouping engineered lost-revenue metrics by product revealed that `Tablets` are the primary frontend checkout bottleneck, bleeding over $174,690 in potential revenue. 
* **The Operational Bottleneck (Cancellations):** A pre-aggregation `WHERE` filter exposed that front-end abandonment is disconnected from back-end operations. `Chairs` suffer the highest cancellation revenue loss ($48,660). Further isolation by `PaymentMethod` proved this is an infrastructure failure: Credit Cards and Gift Cards account for the vast majority of cancellations, indicating a severe issue with fraud-prevention false positives and split-payment UI processing.
* **The Temporal Audit (Synthetic Flatline):** Extracting and grouping order volumes by `YEAR` and `MONTH` revealed a completely uniform distribution lacking standard e-commerce seasonality or YoY growth. This confirms the dataset is synthetic, intentionally invalidating the use of time-series predictive forecasting in future BI phases.
