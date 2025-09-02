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
Fact Tables:
* shipments: This is the primary fact table, containing transactional data for each shipment, including measures like Boxes and Cost, as well as keys to other dimension tables.
Dimension Tables:
* calendar: A dedicated dimension table for all time-based analysis, including attributes like Date, Month, and Year, which is critical for time intelligence functions.
* products: A dimension table containing product details such as Category and Cost per box.
* people: A dimension table used for analyzing performance by individuals or teams, a key component for a user-centric dashboard.
* locations: A dimension table that provides geographical context with attributes like Geo and Region.
* Parameter: A unique table used to create dynamic features, such as the zoom slider, demonstrating an understanding of advanced Power BI techniques.
This data structure ensures that the dashboard is both highly performant and scalable for future growth.
