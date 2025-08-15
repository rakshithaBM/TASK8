# Task 8 – Sales Dashboard in Power BI

## 📌 Overview
This task focuses on building an interactive **Sales Analysis Dashboard** using Power BI.  
The dataset contains order details such as order date, product category, region, units sold, unit price, and total sales.  
The dashboard helps visualize sales trends, category performance, and regional insights.

---

## 🔹 Steps Performed
1. **Data Preparation**
   - Loaded dataset into Power BI.
   - Changed data types:
     - `Order Date` → Date
     - `Units Sold`, `Unit Price`, `Sales` → Decimal Number
   - Created `Sales` column:
     ```DAX
     Sales = 'TableName'[Units Sold] * 'TableName'[Unit Price]
     ```
   - Created `MonthYear` column:
     ```DAX
     MonthYear = FORMAT('TableName'[Order Date], "MMM yyyy")
     ```

2. **Visualizations Created**
   - **Line Chart** – Sales trend by Month-Year.
   - **Bar Chart** – Sales by Region.
   - **Donut Chart** – Sales by Product Category.
   - **Card Visuals** – Total Sales, Total Units Sold.
   - **Slicers** – Category filter, Region filter.

3. **Dashboard Formatting**
   - Added title, applied color themes.
   - Sorted Month-Year by actual `Order Date` to maintain chronological order.
   - Applied filters to make visuals interactive.

---

## 📊 Key Insights
- Sales peaked in **March 2024** driven mainly by strong Electronics sales.
- East region recorded the highest revenue, outperforming all other regions consistently throughout the year.
- Electronics category dominated total sales, followed by Furniture and Office Supplies.
- Steady upward trend observed in monthly sales over the last two quarters, indicating growing customer demand.

---

## 🛠 Tools Used
- **Power BI Desktop** for data modeling and visualization.
- **DAX** for calculated columns.

---

## 📂 Files in this Repository
- `Task8_Sales_Dashboard.pbix` – Power BI dashboard file.
- `sales_dataset.csv` – Dataset used for analysis.
- `README.md` – Documentation of the project.

---

## 📢 Conclusion
This dashboard allows quick tracking of sales performance, identifying best-selling categories, and analyzing regional performance.  
The insights can help businesses optimize inventory, plan marketing campaigns, and improve regional sales strategies.
