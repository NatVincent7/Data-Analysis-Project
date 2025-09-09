# Superstore Sales Analysis and Dashboard

## Data
Kaggle: https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting

## Project Overview
This project focuses on analyzing sales data from a retail superstore to uncover key drivers of performance. By combining data cleaning, exploratory data analysis (EDA), shipping performance analysis, and regional sales analysis, this project aims to provide actionable business insights that can be used for strategic decision-making in inventory management, logistics, and regional marketing.

## Key Features
-[x] **Exploratory Data Analysis (EDA):**  
  Identify top-selling products, sales by category, and overall sales trends.
  
-[x] **Data Cleaning & Transformation:**  
  Handle missing values, convert date columns to datetime, and derive new metrics such as shipping delay.

-[x] **Shipping Performance & Efficiency:**  
  Calculate and visualize shipping delays to assess logistics efficiency.

-[x] **Regional & Geographic Sales Analysis:**  
  Group and visualize sales by Region and State to identify high- and low-performing areas.

-[x] **Dashboard & Reporting:**  
Create interactive dashboards with tools like Tableau to communicate insights.

## Tools and Technologies Used
- **Python** for data manipulation and analysis.
- **Pandas** for data wrangling.
- **Matplotlib & Seaborn** for data visualization.
- **SQLite** (optional) for data storage.
- **Tableau** for interactive dashboards.

## Dataset
The dataset used is **"Superstore Sales.csv"**, which contains the following columns:
- **Order Date:** Date when the order was placed.
- **Ship Date:** Date when the order was shipped.
- **Product Name:** Name of the product sold.
- **Sales:** Revenue generated from the sale.
- **Category:** Product category.
- **Postal Code:** Customer's postal code.

---

## Conclusion
**Inventory Optimization**
Sales nearly doubled cumulatively from Q1 through Q4, with peaks in Q3 and Q4 driven by seasonal demand (likely holiday shopping and year-end business purchases).

**Revenue**
Year-over-year (YoY) sales showed mixed trends: a slight decline of approximately 4% in 2016 (potentially due to economic headwinds or competitive pressures), followed by significant growth of 20-30% in both 2017 and 2018, reflecting overall upward momentum in the superstore's performance.

**Regional Marketing**
The top 5 states by sales volume are California, New York, Texas, Washington, and Pennsylvania, respectively, accounting for a significant portion of total revenue due to higher population density and economic activity.

**Top Products**
The Canon imageCLASS 2200 Advanced Copier was the top-performing product by revenue for 2017-2018, driven by increasing demand for multifunctional devices that integrate printing, copying, scanning, and faxing to enhance office productivity and document management amid digital transformation trends.

**Next Analysis**
**Shipping Efficiency**: Building on the discovered average shipping delays by class, compare them against promised delivery ranges. Identify bottlenecks using logistic regression on factors like distance or carrier, and recommend partnerships to reduce delays exceeding 2 days for improved customer satisfaction.
**Regional Sales Drivers**: Drill down into top states by analyzing drivers via multiple linear regression (e.g., variables like income levels, ad spend, or industry presence). For instance, if tech sectors correlate highly in California, focus B2B marketing there; track quarterly to refine strategies for higher ROI.
**Customer Demand Trends and Predictions**: Investigate temporal demand patterns, such as the surge in the Canon imageCLASS 2200 Advanced Copier during 2017-2018, likely fueled by economic recovery boosting print demand (1-2% industry growth), rising need for affordable multifunctional devices in offices transitioning to digital workflows, and productivity enhancements amid improving business conditions.

## Dashboard Link
https://public.tableau.com/views/SuperstoreSalesDashboard_17558584893820/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

