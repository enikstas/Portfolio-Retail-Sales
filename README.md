# 🏖️ Retail Sales Dashboard

## 📝 Introduction
This project uses generated sales data for retail stores in Florida during the summer of 2025 to demonstrate my skills in data analysis, visualization, and interpretation. The dataset simulates realistic sales patterns, capturing the impact of tourist peaks, and time of day.

---
## ❔ Objective
**The goal is to analyze sales data to:**
- Identify top-performing stores and product categories.
- Evaluate return rates across product categories to optimize inventory.
- Detect peak sales hours and days to improve staffing and promotions.

---
## 💼 Tools
- **sales.csv**: Generated dataset (3.502 rows) containing sales transactions from June 1 to August 31, 2025. Columns include `sales_id`, `date` (MM/DD/YYYY HH:MM AM/PM), `Shop`, `product category`, `product name`, `quantity`, `price`, and `is_returned`.
- **FloridaRetailSales.pbix**: Power BI dashboard file with interactive visualizations, KPIs, and filters for exploring sales trends.

---
## 🚀 Project Workflow

### ✔ Phase 1: Data Preparation
- Loaded `sales.csv` into Power BI and verified data integrity (no missing values or duplicate `sales_id`).
- Created calculated columns: `revenue` (`quantity * price`), `sale_date` (date only), `sale_hour` (hour of transaction), and `day_of_week`.

### ✔ Phase 2: Data Modeling
- Built relationships between `sale_date` for accurate aggregation.
- Created DAX measures for key metrics:
  - `Total Revenue = SUM('Sales'[revenue])`
  - `Total Quantity = SUM('Sales'[quantity])`
  - `Average Transaction Value = DIVIDE(SUM('Sales'[revenue]), DISTINCTCOUNT('Sales'[sales_id]))`
  - `Return Rate = DIVIDE(COUNTROWS(FILTER('Sales', 'Sales'[is_returned] = TRUE())), COUNT('Sales'[sales_id]), 0)`

### ✔ Phase 3: Analysis
- Aggregated sales by store, product category, and time to identify trends.
- Analyzed return rates to detect problematic products.
- Compared sales performance across peak tourist periods (Independence Day, Labor Day).

### ✔ Phase 4: Power BI Dashboard
- **KPI Cards**: Total Revenue, Total Quantity, Average Transaction Value, Return Rate.
- **Sales Trends**: Line chart for revenue by date, highlighting tourist peaks (July 1–7, August 28–September 3).
- **Store Performance**: Treemap chart for revenue share by store (Shop A–E).
- **Category Analysis:** Bar chart showing revenue of products sold, quantity of products sold, and quantity of products returned.
- **Hourly Patterns**: Bar chart for sales volume by hour, emphasizing 10:00 AM–4:00 PM for products.
- **Interactive Filters**: Shop, Day of Week, Product Category, Product name.

---
## 📊 Key Business Insights
- **Top Stores**: Shop D (Tourist) generates ~30% of total revenue due to high tourist traffic.
- **Popular Categories**: Clothing and Accessories dominate sales, especially in Coastal stores during sunny weather.
- **Weather Impact**: Rainy days reduce sales by 40% for beach-related products (e.g., Swimsuit, Sunscreen).
- **Return Rates**: Clothing has a 10% return rate, indicating potential sizing or quality issues.
- **Peak Hours**: Sales peak between 10:00 AM and 4:00 PM for beach products, suggesting optimal staffing times.

---
## 💻 Dashboard Preview
![RetailSales preview](https://github.com/user-attachments/assets/6c867a5e-1ad5-4e45-a1e0-12cea869c2ae)

## 🔎 Outcome
- Developed an interactive Power BI dashboard to explore retail sales trends.
- Demonstrated proficiency in data cleaning, modeling, and visualization for business decision-making.
- Provided actionable insights for inventory management, staffing, and promotional strategies.
- Ready for use in portfolios, interviews, or client presentations.

---

✅ Shared for transparency and accessibility of the analysis.
## 📬 Connect
Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/enikstas/) to discuss data analytics, retail insights, or collaborations!
