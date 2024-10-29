# Sales Data Analysis Project
This project collects and analyzes sales data from a retail store from various regions.The goal is to uncover key insights such as top-selling products, regional performance, and monthly sales trends using pivot analysis. By calculating metrics suh as total sales by product,region e.t.c, businesses can identify which regions are thriving and which may require additional attention or resources. This analysis will not only highlight regional strengths but also reveal opportunities for improvement, enabling strategic decision-making.
# Data Collected
## Data Structure
The dataset includes the following key columns:
1. Product: The name or type of product sold.
2. Region: The geographical area where the sale operates (North, South, East, West).
3. Order Date: The date when the order was placed.
4. Quantity: The number of units sold.
5. Unit Price: The price of each unit of the product.
6. Total Sales: The total revenue from each sale (calculated as Quantity × Unit Price).
# Data Cleaning
The data was cleaned by removing duplicates prior to data analysis. Data cleaning helps eliminate errors and allows for smoother analysis.
# Project Objectives
The project performed an initial exploration which include
- Total Sales: The total sales from each sale was calculated as (Quantity × Unit Price).
- Average Sales per product: The average sales per product was calculated using the AVERAGEIF(range,criteria [average_range]) function. 
- Total revenue by Region: The total revenue by region was calculated using =SUMIF(Table1[Region],D2,Table1[TotalSales])
- Total sales by Region: This determined the total revenue generated in each region
- 
 
