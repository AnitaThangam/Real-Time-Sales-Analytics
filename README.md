**REAL-TIME ANALYSIS PIPELINE**

**Overview**

Businesses often struggle to monitor sales performance in real time.
This project simulates a real-time sales analytics pipeline to track key business metrics and generate actionable insights.
It demonstrates an end-to-end workflow from data ingestion to visualization.

**Objectives**

Simulate real-time data streaming using Python
Perform KPI analysis using SQL
Build interactive dashboards using Power BI
Enable data-driven decision-making through insights

**Architecture**

Data Source → Python (Simulation) → CSV → SQL → Power BI Dashboard

**Tech Stack**

Python (Pandas)
SQL (SQLite)
Power BI

**Features**

Simulated real-time data streaming using batch processing
KPI tracking (Total Sales, Orders, Customers)

**Python Implementation**
Simulated real-time data by appending batches to a live dataset
Generated cleaned_sales_final.csv to mimic streaming data
Automated data flow for continuous updates
Sales trend and regional performance analysis
Interactive dashboard with filters and slicers
Customer and product-level insights

**SQL Analysis**

Example queries used for business insights:

-- Total Revenue
SELECT SUM(sales) AS total_revenue FROM cleaned_sales_final;

-- Top Products
SELECT product_name, SUM(sales) AS revenue
FROM live_sales
GROUP BY product_name
ORDER BY revenue DESC
LIMIT 5;

**Key Insights**

A small set of products contributes to the majority of revenue
Certain regions consistently outperform others
Sales trends indicate seasonal demand patterns
High-value customers significantly impact total revenue

**How to Run**

1. Clone the repository
git clone https://github.com/AnitaThangam/Real-Time-Sales-Analytics.git

2. Install dependencies
pip install pandas

3. Run simulation
python python/REAL_TIME_SALES.ipynb

5. Import into SQL
Upload cleaned_sales_final.csv into SQLite Online

6. Run queries
Use queries from:sql/Real-Time SQL Analysis

**Outcome**

Built an end-to-end analytics pipeline
Enabled real-time KPI monitoring
Improved business decision-making using data

**Business Impact**

This project demonstrates how organizations can leverage real-time analytics to monitor performance, identify trends, and make faster data-driven decisions.
