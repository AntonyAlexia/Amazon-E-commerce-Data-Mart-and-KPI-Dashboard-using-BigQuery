# Amazon-E-commerce-Data-Mart-and-KPI-Dashboard-using-BigQuery

# 📌 Project Overview
In this project, I built a full-scale E-commerce analytics Data Mart using Google BigQuery based on Amazon sales data.
The goal is to create a professional-grade star schema, enable complex business analysis through clean dimensions and fact tables, and generate business KPIs such as revenue trends and best-selling locations.

# 📌 Dataset
Source: Amazon Sale Report.csv (raw e-commerce transaction data)

Columns included: Order ID, Order Date, Status, SKU, Product Category, Quantity, Amount, Shipping City, Shipping State, etc.

# 📌 Project Steps
1. Data Cleaning & Staging
Uploaded raw CSV into BigQuery

Parsed and cleaned important fields:

Standardized dates

Removed cancelled orders

Casted numeric fields safely

Created a staging table (staging.stg_amazon_sales).

2. Dimension Tables Creation
dim_product: Clean unique product catalog (SKU, Category)

dim_date: Date breakdown (Year, Month, Day)

dim_location: Customer location mapping (City, State, Country)

3. Fact Table Creation
fact_sales:
Connected transactions to dimensions using IDs.
Columns: ProductID, DateID, LocationID, Quantity, TotalAmount.

4. Analytical Queries (KPIs)
Total Revenue by Product Category

Monthly Revenue Trend

Top 10 Cities by Revenue

# 📌 Final Star Schema Design (ER Diagram)

             +-----------------+
             |   dim_product    |
             +-----------------+
                     |
                     |
+-----------+   +-----------+   +-----------+
|dim_date   |   |fact_sales |   |dim_location|
+-----------+   +-----------+   +-----------+
# 📌  KPIs
Total Revenue by Product Category

Product Category	Total Revenue
Kurta	₹2,000,000
Set	₹1,500,000
Top	₹800,000
Monthly Revenue Trend

Year	Month	Monthly Revenue
2022	04	₹600,000
2022	05	₹700,000
Top 10 Locations by Revenue

City	State	Revenue
Mumbai	Maharashtra	₹300,000
Bengaluru	Karnataka	₹250,000

# 📌 Future Enhancements
Build an automated dashboard using Looker Studio or Power BI.

Implement streaming ingestion for real-time sales tracking.

Add Customer Dimension for personalized KPIs like Lifetime Value.

# 📌 Tools and Technologies
Google BigQuery (Data Warehouse)

SQL (Data Modeling & Analysis)

Google Cloud Platform

Power BI (Dashboard plan - optional)

📌 Author
Built by Antony Alexia Sebasthikannu | 📈 Data Analytics & Engineering Enthusiast |
🚀 Passionate about clean data, great insights, and powerful storytelling.

