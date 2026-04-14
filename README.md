# 📊 Vendor Performance Analysis

## 🚀 Project Overview
This project focuses on analyzing vendor performance using transactional inventory data to uncover insights on profitability, pricing strategies, and inventory efficiency.

The analysis integrates multiple datasets including purchases, sales, vendor invoices, and pricing data to build a unified analytical view for decision-making.

---

## 🎯 Objectives
- Identify **top-performing vendors and brands**
- Analyze **profitability and margin trends**
- Evaluate **inventory turnover and stock efficiency**
- Detect **low-performing products needing pricing or promotional adjustments**
- Understand the impact of **bulk purchasing on cost optimization**

---

## 🗂️ Dataset Description
The project uses a relational database (`inventory.db`) with the following tables:

- **Purchases** → Vendor transactions (quantity, cost, brands)
- **Purchase Prices** → Product pricing per vendor
- **Vendor Invoice** → Aggregated purchase data + freight cost
- **Sales** → Sales transactions (revenue, quantity, pricing)

---

## 🛠️ Tech Stack
- **Python**
- **Pandas, NumPy**
- **SQL (SQLite)**
- **Matplotlib, Seaborn**
- **SciPy (Statistical Analysis)**

---

## 🔄 Data Processing
- Connected to SQLite database and extracted data using SQL queries  
- Created a **vendor_sales_summary** table by joining:
  - Purchases
  - Sales
  - Vendor invoices
  - Pricing data  
- Performed **data cleaning**:
  - Removed negative and zero values in profit, sales, and margins  
- Feature engineering:
  - Gross Profit  
  - Profit Margin  
  - Stock Turnover  

---

## 📈 Exploratory Data Analysis (EDA)
- Distribution analysis using histograms and boxplots  
- Outlier detection across pricing, freight, and sales  
- Correlation heatmap to identify relationships between variables  

### Key Observations:
- Strong correlation (**0.999**) between purchase and sales quantities → efficient inventory flow  
- Large variation in **freight cost** → potential logistics inefficiencies  
- Presence of **loss-making transactions** (negative profit)  
- Some products show **zero sales despite purchases** → dead stock  

---

## 📊 Key Insights

### 💰 Profitability Insights
- High-performing vendors tend to have **lower margins but higher volume**
- Low-performing vendors maintain **higher margins but low sales**

### 📦 Inventory Insights
- Stock turnover varies widely → some products sell fast, others remain unsold  
- Significant capital is locked in **slow-moving inventory**

### 📉 Pricing Insights
- Weak correlation between purchase price and sales performance  
- Bulk purchasing reduces unit price by **~70%**, improving margins  

### 🎯 Business Recommendations
- Optimize **pricing strategies** for high-volume vendors  
- Improve **marketing for high-margin low-sales products**  
- Reduce **excess inventory** for slow-moving items  
- Negotiate **bulk purchase deals** to lower costs  

---

## 📌 Advanced Analysis
- Identified **brands with low sales but high margins** for targeted promotion  
- Conducted **correlation analysis** to understand drivers of profitability  
- Estimated **confidence intervals for profit margins**:
  - High-performing vendors: ~30–31%  
  - Low-performing vendors: ~40–42%  

---

## 📷 Visualizations
- Histograms for distribution analysis  
- Boxplots for outlier detection  
- Correlation heatmap  
- Brand-level performance scatter plots  

---


---

## ✅ Conclusion
This project provides actionable insights into vendor performance by combining SQL-based data engineering with Python-driven analysis. It helps businesses make data-driven decisions in pricing, procurement, and inventory management.
