# Sales Data Analysis Project
This project collects and analyzes sales data from a retail store from various regions. The goal is to uncover key insights such as top-selling products, regional performance, and monthly sales trends using pivot analysis. By calculating metrics suh as total sales by product,region e.t.c, businesses can identify which regions are thriving and which may require additional attention or resources. This analysis will not only highlight regional strengths but also reveal opportunities for improvement, enabling strategic decision-making.

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
- Total revenue by Region: The total revenue by region was calculated using =SUMIF(range,criteria [sum_range]) function.

## Pivot Analysis
Pivot analysis is a powerful data analysis technique that allows users to summarize, reorganize, and analyze large datasets. The following metrics was summarized using pivot analysis;
- Total sales by Region: This analysis summarizes the total sales figures for each geographical region (North, South, East, West).
- Total Sales by product: This metric aggregates total sales for each product, providing a clear view of which products are driving revenue. 
- Total Sales by Month: This analysis tracks total sales over time, organized by month.
- Top 5 Product by Total Sales: This analysis highlights the five products with the highest total sales figures

## Other interesting report performed include
- Grand Total Sales: This determined the overall sum of total sales using SUM function.
- Average sales: The average sales of the overall total sales using AVERAGE function.
- Highest Sales: The highest sales of the overall total sales using MAX function.
- Lowest sales: The lowest sales of the overall total sales using MIN function.
- Total number of product: The total number of products uaing COUNTA function.  

# Data Visualization
![Total Sales by Region](https://github.com/user-attachments/assets/ab8c799a-74d9-4ae3-8783-d20aef091506)
![Total Sales by Product](https://github.com/user-attachments/assets/c514376d-8c6c-4936-acd6-0eb236044a4b)
![Total S![Top 5 Product by Total Sales](https://github.com/user-attachments/assets/d60abf6f-1bb4-4c7c-8a9e-1c1df6708d46)
ales by Month](https://github.com/user-attachments/assets/3bcd0a25-eee8-42af-b8ed-21b50f094546)

