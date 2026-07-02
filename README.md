# SQL Finance Portfolio
### Andres Jim | Senior Financial Analyst
 
[![SQL](https://img.shields.io/badge/SQL-Financial%20Analytics-1F4E79?style=flat-square)](https://github.com/andresjim1027/sql-finance-portfolio)
[![Status](https://img.shields.io/badge/Status-In%20Progress-2E75B6?style=flat-square)](https://github.com/andresjim1027/sql-finance-portfolio)
 
---
 
## About This Portfolio
 
I'm a senior financial analyst building SQL as a core skill to complement my FP&A background. This portfolio demonstrates SQL applied to real finance problems — not toy exercises. Every project mirrors a deliverable I would produce at work: variance reports, trend analysis, headcount modeling, and executive dashboard feeds.
 
**Tools used:** SQL (SQLite) · DB Browser for SQLite · Excel · Power BI
 
---
 
## Projects
 
| # | Project | SQL Concepts | Status |
|---|---------|-------------|--------|
| 1 | [Budget vs. Actuals Variance Report](#project-1--budget-vs-actuals-variance-report) | JOINs, CTEs, GROUP BY, CASE WHEN | 🔄 In Progress |
| 2 | [Expense Trend & Period-over-Period Analysis](#project-2--expense-trend--period-over-period-analysis) | Window Functions, LAG(), Rolling AVG | 🔜 Coming Soon |
| 3 | [Headcount & People Cost Analysis](#project-3--headcount--people-cost-analysis) | Multi-Table JOINs, CTEs, Cost per HC | 🔜 Coming Soon |
| 4 | [Executive KPI Summary Query](#project-4--executive-kpi-summary-query) | Chained CTEs, P&L Logic, Dashboard Feed | 🔜 Coming Soon |
 
---
 
## Project 1 — Budget vs. Actuals Variance Report
 
**Business Question:** How is each department tracking against budget this month? Which cost centers are over 10% above their budget? Is there any unbudgeted spend?
 
**Scenario:** Built a monthly variance report in SQL that a CFO or VP Finance would use during month-end close — showing actuals vs. budget side by side, with dollar and percent variance, and flagging over-budget departments.
 
**Dataset:** Mock general ledger (500 rows), budget table, and chart of accounts across 8 departments and 12 months.
 
**SQL Concepts Demonstrated:**
- `INNER JOIN` and `LEFT JOIN` across 3 tables
- `GROUP BY` and `SUM()` aggregation
- Variance math: `(actual - budget)` and `(actual - budget) / budget * 100`
- `CASE WHEN` to flag departments over threshold
- Multi-step `WITH` clause (CTEs) for readable, production-quality queries
- `LEFT JOIN` to surface unbudgeted spend (actuals with no matching budget line)
📁 [View project files](./01_budget_vs_actuals/)
 
---
 
## Project 2 — Expense Trend & Period-over-Period Analysis
 
**Business Question:** How is spending trending month over month? Which departments are accelerating? How does this year compare to last year?
 
**Scenario:** Built a trend analysis report using advanced SQL to show MoM change, rolling 3-month averages, YoY comparisons, and department spend rankings — the kind of analysis that drives operating reviews.
 
**SQL Concepts Demonstrated:**
- `LAG()` window function for prior period comparison
- `SUM() OVER` and `AVG() OVER` for running totals and rolling averages
- `RANK() OVER` for department spend rankings
- YoY variance using `LAG()` with a 12-period offset
- `PARTITION BY` for calculations scoped by department
📁 [View project files](./02_expense_trend_analysis/)
 
---
 
## Project 3 — Headcount & People Cost Analysis
 
**Business Question:** How does actual headcount compare to plan? What is the cost per employee by department? Where are we over on people costs?
 
**Scenario:** Joined HR headcount data to GL payroll actuals to build a complete people cost analysis — the kind of cross-functional work that finance teams do every quarter with HRBP partners.
 
**SQL Concepts Demonstrated:**
- Multi-table JOINs across HR and finance data sources
- Cost per headcount calculation: `people_cost / actual_hc`
- Headcount variance vs. plan
- MoM headcount change using `LAG()`
- Chained CTEs for multi-step logic
📁 [View project files](./03_headcount_people_cost/)
 
---
 
## Project 4 — Executive KPI Summary Query
 
**Business Question:** Can we produce a single, refreshable SQL query that outputs all key P&L metrics — Revenue, COGS, Gross Margin, OpEx, EBITDA — with current month, prior month, YTD, and budget variance?
 
**Scenario:** Built the underlying data layer for a CFO Power BI dashboard. One query, scheduled to refresh nightly, that replaces a manually updated Excel file used during leadership reviews.
 
**SQL Concepts Demonstrated:**
- Chained CTEs (5 steps: revenue, COGS, OpEx, budget, final join)
- `CASE WHEN` on account codes to map GL lines to P&L categories
- `SUM() OVER` for YTD accumulation
- `LAG()` for prior month comparison
- Metric ordering column for correct P&L sort in Power BI
📁 [View project files](./04_executive_kpi_summary/)
 
---
 
## Skills Demonstrated
 
| Category | Skills |
|----------|--------|
| **Core SQL** | SELECT, FROM, WHERE, GROUP BY, HAVING, ORDER BY |
| **Joins** | INNER JOIN, LEFT JOIN, multi-table joins |
| **Aggregations** | SUM, COUNT, AVG, MIN, MAX |
| **Advanced SQL** | CTEs (WITH clause), subqueries, CASE WHEN |
| **Window Functions** | LAG, LEAD, RANK, SUM OVER, AVG OVER, PARTITION BY |
| **Finance Domain** | Budget vs. actuals, variance analysis, P&L structure, headcount modeling, FP&A reporting |
 
---
 
## Connect
 
- 💼 [LinkedIn](https://www.linkedin.com/in/andresjim1027)
- 📧 Available on request
---
 
*Portfolio built as part of a structured 6-week SQL curriculum focused on FP&A applications.*
 
