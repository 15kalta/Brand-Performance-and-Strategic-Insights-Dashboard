# Brand-Performan-Strategic-Insights-Dashboard

## 🍫 Awesome Chocolates: Sales & Profitability Insights Dashboard
A dynamic, interactive data visualization tool built to explore the performance of a chocolate brand, focusing on sales, profitability, and operational efficiency metrics to drive business strategy.
## Purpose of the Dashboard
This Power BI dashboard is a strategic decision-making tool that provides stakeholders with a comprehensive view of Awesome Chocolates' performance. It transforms raw data into actionable insights by focusing on key metrics.

The dashboard's core purpose is to track and analyze sales, profit, and shipment data over a 13-month period. It specifically highlights month-over-month (MoM) changes, a critical metric that provides immediate context on business momentum. By visualizing these changes, the dashboard enables users to quickly understand performance trends, identify areas for improvement, and make informed decisions to optimize product strategy and drive revenue growth.
## Tech Stack
The dashboard was built using the following tools and technologies:
* Power BI Desktop – The primary platform for designing and creating the dashboard.
* Power Query – Utilized for data loading and the initial data transformation and cleaning process.
* Data Modeling – Established relationships among tables using a Star Schema approach.
* DAX (Data Analysis Expressions) – Crucial for creating complex, custom measures, including time intelligence functions, Month-over-Month (MoM) calculations, and dynamic visuals using Field Parameters.
* Dashboard Design – Focused on wireframe design, page layout, and applying themes for a professional and user-friendly interface.
* Advanced Visualization – Created a Profit % Gauge Chart and a Dynamic Trend Analysis Chart with a zoom slider.
* User Experience Enhancements – Implemented Bookmarks for conditional views (Product vs. People), tooltip design, and filter panels to make the dashboard highly interactive.
## Data Source
The project's dataset was obtained from Kaggle and is structured to enable a comprehensive analysis of business performance over a 13-month period.
The data model adheres to a star schema, a best practice for business intelligence, consisting of key dimension and fact tables that are interconnected for efficient querying and analysis.
### Fact Tables:
* shipments: This is the primary fact table, containing transactional data for each shipment, including measures like Boxes and Cost, as well as keys to other dimension tables.
### Dimension Tables:
* calendar: A dedicated dimension table for all time-based analysis, including attributes like Date, Month, and Year, which is critical for time intelligence functions.
* products: A dimension table containing product details such as Category and Cost per box.
* people: A dimension table used for analyzing performance by individuals or teams, a key component for a user-centric dashboard.
* locations: A dimension table that provides geographical context with attributes like Geo and Region.
* Parameter: A unique table used to create dynamic features, such as the zoom slider, demonstrating an understanding of advanced Power BI techniques.
This data structure ensures that the dashboard is both highly performant and scalable for future growth.
# Features / Highlights
## Business Problem
The "Awesome Chocolates" team was facing several key business challenges due to a lack of a unified data-driven reporting system. They needed to move beyond fragmented data to a holistic, real-time view of their performance.
* Financial Performance: How can we gain real-time visibility into core financial metrics like sales and profit, and track our performance against previous months to quickly respond to market shifts?
* Operational Efficiency: How can we identify inefficiencies within our supply chain, such as low-box shipments, and optimize our logistics to reduce costs and improve overall performance?
* Product Strategy: Which products are the most profitable, and how can we use this information to make data-driven decisions on pricing, marketing, and product development?
* Performance Monitoring: How can we create a system that allows stakeholders to easily track Key Performance Indicators (KPIs) against set targets, moving from reactive reporting to proactive decision-making?
## Goal of the Dashboard
The primary goal of this dashboard is to empower stakeholders to move from reactive reporting to proactive decision-making. It serves as a centralized hub for actionable business intelligence.
Specifically, this tool is designed to:
* Enable Strategic Decision-Making: Provide executives and managers with a consolidated, top-level view of sales, profit, and costs to guide strategic planning and resource allocation.
* Enhance Operational Efficiency: Uncover key trends and insights within shipment and product data to identify inefficiencies and optimize the supply chain.
* Drive Profitability: Allow for granular analysis of product performance, helping to identify high-margin items to focus on and low-margin products to reconsider.
* Monitor Performance in Real-Time: Give the team a dynamic tool to track Key Performance Indicators (KPIs), such as month-over-month changes, against business targets.
# Walkthrough of Key Visuals
## Key Performance Indicators (KPIs)
* Total Sales
This KPI represents the overall revenue generated.
Formula: Total Sales = SUM('Sales'[Total Sales])
Value: $34M
* Total Profit
This is a core financial metric that calculates the total profit after costs.
Formula: Profit = DIVIDE([Total Profit], [Total Sales])
Value: $21M
* Total Boxes
This metric tracks the total number of boxes sold, which is an important operational KPI for managing inventory and logistics.
Formula: Total Boxes = SUM('Shipments'[Boxes])
Value: 2M
* Total Shipments
This metric counts the total number of shipments, essential for supply chain analysis.
Formula: Total Shipments = DISTINCTCOUNT('Shipments'[Shipments])
Value: 6K
* Profit %
This metric shows the profit margin as a percentage, a key measure of a product's or the company's profitability.
Formula: Profit % = DIVIDE([Profit], [Total Sales])
Value: 60.29% (from the gauge chart visual)
* Month-over-Month (MoM) Sales Growth
This metric measures the percentage change in sales from the previous month, providing insight into business momentum.
Formula: Latest MoM Sales Change % = VAR prev_month_sales = CALCULATE( [Total Sales], DATEADD( 'calendar'[Date], -1, MONTH ) ) RETURN DIVIDE( [Total Sales] - prev_month_sales, prev_month_sales )
Value: -10.76%
