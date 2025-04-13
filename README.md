# 📊 Sales Performance Dashboard – Power BI | Excel | MySQL

This project features a fully interactive and insightful **Sales Performance Dashboard** built using **Power BI**, designed for a **Consumer Electronics** business to track key KPIs like Total Revenue, Profit, and Sales Orders. The goal was to empower data-driven decisions by visualizing trends, top-performing products, and channel-wise revenue contributions.

---

## 🚀 Key Insights from the Dashboard

- 📌 **Total Revenue, Profit, Cost, and Sales Orders** – displayed using card visuals.
- 📈 **Monthly Revenue Trend** – helps identify seasonal performance fluctuations.
- 🧩 **Top 5 / Bottom 5 Products by Revenue** – via donut charts.
- 🌍 **Channel-wise and Product-wise Profit Analysis** – using stacked bar/column charts.
- 🔍 **Dynamic Filters** – including slicers for Channel and Date range to enable flexible analysis.

---

## 🛠 Skills & Tools Used

- ✔ **Power BI** – Data visualization, custom DAX measures, interactive dashboard
- ✔ **Power Query** – Data cleaning, transformation (e.g., handling nulls, renaming fields)
- ✔ **Excel** – Data source formatting, structured tables
- ✔ **MySQL** – For staging and organizing raw sales data before loading into Power BI

---

## 🗃 Data Model Overview

- **Tables Used:** Customers, Products, Date, Markets, Transactions
- Built a star schema model with proper relationships to enable drill-down and slicer-level insights.

---

## 🔧 Sample SQL Query (Used for Preprocessing in MySQL)

```sql
SELECT 
    Product_Name, 
    SUM(Revenue) AS Total_Revenue, 
    SUM(Profit) AS Total_Profit
FROM transactions
GROUP BY Product_Name
ORDER BY Total_Revenue DESC
LIMIT 5;
