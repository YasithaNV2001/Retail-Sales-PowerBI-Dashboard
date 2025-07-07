# 🛍️ Retail Sales Analysis Dashboard (Power BI)

This Power BI project provides insights into the sales performance, profitability, customer segments, and shipping efficiency of a retail business. The dashboard is designed to help stakeholders monitor KPIs, explore regional performance, and identify key trends and bottlenecks.

---

## 📊 Project Overview

- 🧾 Built using raw retail sales data (orders, shipping, returns, product categories, etc.)
- 📈 Transformed and modeled in Power BI using Power Query, relationships, and DAX
- 💡 Interactive dashboard with filters for Region, Segment, Category, and Time
- 🧠 Created calculated columns and measures (YTD, MTD, Profit Margin, Ship Delay)
- 🗂️ Dimensional model with Date and Customer dimension tables

---

## 🔧 Tools Used

- **Power BI Desktop**
- **Power Query**
- **DAX (Data Analysis Expressions)**
- **Custom Date Table**
- **Heatmap-style formatting**
- **Matrix, Line, Column, and Card visuals**

---

## 📁 Report Structure

### 📌 Page 1: Sales Overview

- 🚀 Key Metrics: Total Sales, Profit, Orders, Avg. Profit Margin
- 📅 Monthly sales trend (line chart)
- 🧱 Sales vs Profit by Category (clustered column)
- 🔍 Slicers: Year, Quarter, Month, Region, Segment

🖼️ ![Sales Overview Page](screenshots/page1_sales_overview.png)

---

### 📌 Page 2: Regional & Segment Insights

- 🗺️ Sales by Region and Segment
- 📊 Profit and Orders by Region & Ship Mode
- 🔥 Heatmap of average shipping delay (Region × Month)

🖼️ ![Regional Insights Page](screenshots/page2_region_segment.png)

---

### 📌 Page 3: Product & Customer Analysis

- 🏆 Top 10 Products by Profit (table with data bars)
- 📈 Sales vs Profit (scatter plot)
- 🧑 Customer segment behavior by Region
- 📦 Returns and Repeat Customers

🖼️ ![Product and Customer Page](screenshots/page3_product_customer.png)

---

## 📈 Measures & Calculated Columns

Some DAX examples used in the report:

```dax
Profit Margin = DIVIDE(SUM(Sales[Profit]), SUM(Sales[Sales]))
Ship Delay (Days) = DATEDIFF(Sales[Order Date], Sales[Ship Date], DAY)
Sales YTD = TOTALYTD(SUM(Sales[Sales]), 'DateTable'[Date])
```

## 📚 Folder Structure
Retail-Sales-PowerBI/
│
├── data/
│   └── retail_raw_dataset.csv
│
├── pbix/
│   └── RetailSalesDashboard.pbix
│
├── screenshots/
│   ├── page1_sales_overview.png
│   ├── page2_region_segment.png
│   └── page3_product_customer.png
│
├── README.md
└── transformation_steps.md
