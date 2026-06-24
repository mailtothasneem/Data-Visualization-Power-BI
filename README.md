## Data-Visualization-Power-BI
Data visualization in Power BI transforms cleaned and modeled datasets into interactive visuals that highlight business performance. By combining charts, maps, and KPIs, the dashboard provides actionable insights for decision‑making.

## 🎯 Project Overview
Business Problem:
  This project demonstrates how Power BI can transform raw sales data into actionable insights through interactive dashboards.

Objective:
  Clean and prepare datasets for analysis.Create DAX measures for KPIs (Sales, Profit, Target Achievement).Build a robust data model with relationships.Create DAX measures for KPIs (Sales, Profit, Target Achievement).Visualize sales trends, category performance, and regional distribution.Provide insights to support decision‑making.

Target Audience
 Build a robust data model with relationships.Create DAX measures for KPIs (Sales, Profit, Target Achievement).Visualize sales trends, category performance, and regional distribution.

Provide insights to support 
* Target Audience: Executive Leadership → Strategic overview of performance.
* Sales Operations → Category and region‑wise analysis.
* Finance Teams → Profitability and margin tracking.

## 🗃️ Data Sources & Architecture
* Source Systems: Local Excel/CSV files (List of Orders, Order Details, Sales Target).
* Data Volume:5,00 rows covering Jan–Nov 2026.
* Storage Mode:Import mode for optimized performance.

## ⚙️ Data Transformation (ETL)

* Tool Used:Power Query Editor.

* Key Cleanups: Merged Orders and Order Details using Order ID.Converted text dates into proper Date type.
* Removed duplicates and null values.
* Applied TRIM/CLEAN for text fields.
* Unpivoted monthly target columns for normalized comparison.

# Custom Functions:
* Profit Margin calculation (Profit ÷ Sales) × 100.
* Automated Target Achievement logic.
* Dynamic Date formatting.

## 🧠 Data Model & DAX
* Model Type: State your schema design
 * Fact Tables:
 * Order Details (Sales transactions).
 * Sales Target (Monthly targets).Orders (Customer, State, City, Date).
 * Product Dimension (Category, Sub‑Category, Brand).


* Key Measures:
Total Sales = SUM('Order Details'[Amount])
Total Profit = SUM('Order Details'[Profit])
Target Achievement % = DIVIDE([Total Sales], SUM('Sales Target'[Target]))
Revenue per Order = DIVIDE([Total Sales], DISTINCTCOUNT('Orders'[Order ID]))
YoY Growth % = DIVIDE([Total Sales] - [Prior Year Sales], [Prior Year Sales])

  
## 🖥️ Dashboard Features
* Page 1: Overview:** Dashboard,sales target.
* Page 2: Deep Dive:** KPI cards,matrix,multi cards.
* Page 3,4: Performance:** Profit margins,visualizations.


## 💡 Key Insights
* Trend A: Furniture generated highest sales but lagged in target achievement.Clothing consistently met targets and had strong profit margins.Electronics showed growth potential but fluctuating performance.Madhya Pradesh emerged as the top state by order count.

Thank You
Entri Elevate

