# Superstore Sales Analysis and Forecasting

## Project Overview

This project uses real sales data from a retail superstore (from Kaggle) to answer a simple but important business question: **"How can we understand past sales trends and predict future performance?"** By cleaning the data, exploring key sales drivers, and applying a forecasting model, the project turns raw numbers into insights that support better decision-making.

## Business Story

Imagine a retail superstore manager who is unsure about which products to stock more of, when to run promotions, or how seasonal changes affect sales. By analyzing the sales data, we uncovered several insights:

- **Key Products & Categories:**  
  We identified top-selling products and high-performing categories that drive most revenue.

- **Seasonal Trends:**  
  Sales patterns change over the year—with noticeable peaks and dips that suggest the best times to promote or adjust inventory.

- **Future Sales Forecast:**  
  Using a SARIMAX model, we forecast future sales, giving the manager a glimpse into what to expect and how to prepare for upcoming trends.

These insights can help the business optimize inventory, plan targeted promotions, and ultimately increase profit.

## Key Features

- **Exploratory Data Analysis (EDA):**  
  Investigated the data to find top-selling products, sales trends by category, and seasonal patterns.

- **Data Cleaning:**  
  Handled missing values, properly formatted date columns, and derived new features (like month and quarter).

- **Time Series Analysis:**  
  Decomposed the sales data into trend, seasonal, and residual components.

- **Forecasting:**  
  Used a SARIMAX model to predict future sales, providing a forward-looking view.

## Tools and Technologies

- **Python & Pandas:** For data cleaning and analysis.
- **Matplotlib & Seaborn:** To create initial visualizations.
- **Plotly:** For interactive charts that help visualize the data in a dashboard.
- **Statsmodels:** To build the SARIMAX forecasting model.
- **SQLite:** For storing the cleaned data and running SQL queries if needed.

## Dataset Details

The dataset, named `Superstore Sales.csv`, includes:

- **Order Date:** When each order was placed.
- **Ship Date:** When the order was shipped.
- **Product Name:** Which product was sold.
- **Sales:** Revenue from each sale.
- **Category:** The product category.
- **Postal Code:** Customer’s postal code (used for regional analysis).

## Conclusion

This project demonstrates how a retail superstore can use data analysis and forecasting to gain valuable insights. By understanding which products sell best, identifying seasonal trends, and predicting future sales, the business can make smarter decisions—improving inventory management, optimizing promotions, and ultimately boosting profits.
