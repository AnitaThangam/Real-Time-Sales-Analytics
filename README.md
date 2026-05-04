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

**Results**
- Total Sales:
- <img width="397" height="230" alt="image" src="https://github.com/user-attachments/assets/158ed072-2faf-4a59-8d40-c7854e184ddc" />

- Top Product:
- <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/aed24564-b958-4299-a15f-d97f6d3ed451" />

- Best Region:
- <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/b7dd482c-5408-484e-9f3b-64cb4a98b699" />

- Ranking Products
- I used window function to rank top-performing products based on revenue
- <img width="700" height="500" alt="image" src="https://github.com/user-attachments/assets/30c28ca6-ffb3-480f-ade6-8f1c5334770b" />

-I used JOIN to combine sales data with region-level information to get more business context.
-<img width="800" height="600" alt="image" src="https://github.com/user-attachments/assets/961d7bc1-1858-4b28-bbbb-36c3f15dd25a" />


**Dashboard Preview**

<img width="900" height="600" alt="image" src="https://github.com/user-attachments/assets/69b0ad39-cea0-4efa-a472-35ac82b77b58" />

Example:
1. Top 5 products contribute majority of revenue
2. West region shows highest sales performance
3. Sales trend indicates seasonal variation
4. Customer concentration observed among top buyers

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
Real-time behavior is simulated using batch data streaming in Python.
