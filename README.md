# Vendor-Sales-Data-Analysis


## 📂 Download or View Files  

You can access the **Vendor Sales Data files** (dataset, Power BI dashboard, and notebook) directly from Google Drive:  

👉 **[Click here to open Vendor Sales Data on Google Drive]([(https://drive.google.com/file/d/1MqDFrfIciNtRixvQ_JDPnmP-2BjDyJxG/view?usp=sharing)](https://drive.google.com/file/d/1MqDFrfIciNtRixvQ_JDPnmP-2BjDyJxG/view?usp=sharing))**  



# 📊 Vendor Sales Performance Analysis

This project combines **Power BI** and **Python (Jupyter Notebook)** to analyze vendor and brand performance using sales and purchase data.  
It helps identify **top vendors**, **low-performing brands**, and **profit opportunities** based on data-driven insights.

---

## 🔍 Objectives

- Identify **brands that need promotional or pricing adjustments** (low sales, high profit margin).
- Determine **vendors contributing the most to total purchases**.
- Evaluate **how much of total procurement depends on top vendors**.
- Analyze **sales and profit patterns** across vendors and brands.

---

## 🧠 Tools & Technologies

- **Python** (Pandas, Matplotlib, Seaborn, SQLAlchemy)
- **Power BI** for interactive visualization
- **MySQL** as the database
- **GitHub** for version control

---

## 🧰 Steps Performed

### 🔹 1. Data Extraction
- Connected Python with MySQL database using SQLAlchemy:
  ```python
  from sqlalchemy import create_engine
  engine = create_engine("mysql+pymysql://root:password@localhost:3306/inventory")
  df = pd.read_sql("SELECT * FROM vendor_sales_summary", engine)



## 🔹 Data Cleaning & EDA

- Imported dataset from MySQL and removed blank or invalid records.

- Handled missing values and outliers using Pandas and boxplots.

- Verified data consistency (data types, duplicates, formatting).

- Performed Exploratory Data Analysis (EDA) using Seaborn and Matplotlib to visualize distributions and correlations.

## 🔹 Business Analysis

- Identified top vendors contributing the most to total purchases.

- Calculated total procurement share of top 10 vendors.

- Detected underperforming brands — low sales (<599.648) but high profit margin (>65%).

- Compared vendor and brand performance through sales and profit metrics.

## 🔹 Power BI Dashboard

- Created interactive visualizations to summarize and present insights:

- KPI Cards: Total Sales, Total Purchase, Profit Margin, and Unsold Capital.

- Donut Chart: Shows Purchase Contribution % by vendor (Top 10 vendors highlighted).

- Scatter Plot: Highlights Target Brands (low sales, high profit).

- Bar Charts: Display Top Vendors and Low-Performing Vendors for strategic insights.
