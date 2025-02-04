# Project Title: Sales Data Project

[Project Overview](#project-overview)

[Data Structure](#data-structure)

[Data Cleaning](#data-cleaning)

[Project Objectives](#project-objectives)

[Pivot Analysis](#pivot-analysis)

[Other Report](#other-report)

[Formula Used](#formula-used)

[Data Visualization](#data-visualization)

[Sales Analysis Dashboard](#sales-analysis-dashboard)

[Sales Analysis Summary](#sales-analysis-summary)

# Project Overview
This project collects and analyzes sales data from a retail store from various regions. The goal is to uncover key insights such as top-selling products, regional performance, and monthly sales trends using pivot analysis. By calculating metrics suh as total sales by product,region e.t.c, businesses can identify which regions are thriving and which may require additional attention or resources. This analysis will not only highlight regional strengths but also reveal opportunities for improvement, enabling strategic decision-making.

# Data Structure
The dataset includes the following key columns:
1. Product: The name or type of product sold.
2. Region: The geographical area where the sale operates (North, South, East, West).
3. Order Date: The date when the order was placed.
4. Quantity: The number of units sold.
5. Unit Price: The price of each unit of the product.
6. Total Sales: The total revenue from each sale 

# Data Cleaning
The data was cleaned by removing duplicates prior to data analysis. Data cleaning helps eliminate errors and allows for smoother analysis.

# Project Objectives
The project performed an initial exploration which include
- Total Sales: This is the total sales for product sold. This was calculated using the SUM function.
- Average Sales per product: The average sales is the average sales for each product category. This was calculated using the AVERAGEIF function
- Total revenue by Region: The total revenue by region was calculated using SUMIF function.

## Pivot Analysis
Pivot analysis is a powerful data analysis technique that allows users to summarize, reorganize, and analyze large datasets. The following metrics was summarized using pivot analysis;
- Total sales by Region: This analysis summarizes the total sales figures for each geographical region (North, South, East, West).
- Total Sales by product: This metric aggregates total sales for each product, providing a clear view of which products are driving revenue. 
- Total Sales by Month: This analysis tracks total sales over time, organized by month.
- Top 5 Product by Total Sales: This analysis highlights the five products with the highest total sales figures

## Other Report
- Grand Total Sales: This determined the overall sum of total sales using SUM function.
- Average sales: The average sales of the overall total sales using AVERAGE function.
- Highest Sales: The highest sales of the overall total sales using MAX function.
- Lowest sales: The lowest sales of the overall total sales using MIN function.
- Total number of product: The total number of products using COUNTA function.

## Formula Used
### Total Sales
```
=SUM([@Quantity]*[@UnitPrice])
```
### Average Sales per Product (Gloves, Hat, Jacket, Shirt, Shoes, Socks)
```
=AVERAGEIF(Table1[Product],C7,Table1[TotalSales])
=AVERAGEIF(Table1[Product],C9914,Table1[TotalSales])
=AVERAGEIF(Table1[Product],C6,Table1[TotalSales])
=AVERAGEIF(Table1[Product],C9911,Table1[TotalSales])
=AVERAGEIF(Table1[Product],C9912,Table1[TotalSales])
=AVERAGEIF(Table1[Product],C9905,Table1[TotalSales])
```
### Total Revenue per Region (North, South, East, West)
```
=SUMIF(Table1[Region],D9911,Table1[TotalSales])
=SUMIF(Table1[Region],D9907,Table1[TotalSales])
=SUMIF(Table1[Region],D9909,Table1[TotalSales])
=SUMIF(Table1[Region],D9905,Table1[TotalSales])
```
### Grand Total Sales
```
=SUM(Table1[TotalSales])
```
### Average Sales
```
=AVERAGE(Table1[TotalSales])
```
### Highest Sales
```
=MAX(Table1[TotalSales])
```
### Lowest Sales
```
=MIN(Table1[TotalSales])
```
### Total Number of Product
```
=COUNTA(Table1[Product])
```
# Data Visualization
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, maps, and infographics, data visualization tools and techniques help to make complex data more accessible, understandable, and usable. 

### Pivot Analysis for Sales Data
![Total Sales by Region](https://github.com/user-attachments/assets/ab8c799a-74d9-4ae3-8783-d20aef091506)
![Total Sales by Product](https://github.com/user-attachments/assets/c514376d-8c6c-4936-acd6-0eb236044a4b)
![Top 5 Product by Total Sales](https://github.com/user-attachments/assets/d60abf6f-1bb4-4c7c-8a9e-1c1df6708d46)
![Total Sales by Month](https://github.com/user-attachments/assets/3bcd0a25-eee8-42af-b8ed-21b50f094546)

### Bar Chart diagram Showing Report for Sales Data
![Bar Chart for Sales Data 1](https://github.com/user-attachments/assets/634729be-a29a-48d8-a09f-80c4dea4d9c4)
![Bar Chart for Sales Data 2](https://github.com/user-attachments/assets/77472143-6cba-4958-920e-8cbe1c14bd96)

# Structured Query Language (SQL)
Structured Query Language, is a standardized programming language used for managing and manipulating relational databases.
SQL was used to analyzed sales data. The following query was written to extract key insights. 

```
Select * from [dbo].[LITA Capstone]
```
### Total sales for each product category
```
Select Product, SUM(Quantity*UnitPrice) AS Total_Sales 
		FROM [dbo].[LITA Capstone]
		GROUP BY Product
```
![TOTAL SALES OF EACH PRODUCT](https://github.com/user-attachments/assets/abaf611e-d71b-429b-a994-7c0a63c2bf81)


### Sales transactions in each region
```
Select Region, COUNT (*) AS [Sales Transaction]
		FROM [dbo].[LITA Capstone]
		GROUP BY Region
```
![NUMBER OF SALES TRANSACTION IN EACH REGION](https://github.com/user-attachments/assets/b5b954ac-52b7-4848-9546-b01b4d72287f)

### Highest Selling Product by Total Sales Value
```
Select Top 1(Product), SUM(Quantity*UnitPrice) AS [Total_Sales]   
		FROM [dbo].[LITA Capstone]
		GROUP BY Product
		ORDER BY Total_Sales DESC
```
![HIGHEST SELLING PRODUCT BYTOTAL SALES](https://github.com/user-attachments/assets/fa4c2789-43a4-482f-be92-ba4ca7b27ae6)

### Total Revenue Per Product
```
Select Product, SUM(Quantity*UnitPrice) AS Revenue
		FROM [dbo].[LITA Capstone]
		GROUP BY Product
```
![TOTAL REVENUE BY PRODUCT](https://github.com/user-attachments/assets/f71c68cd-58ab-4577-a9b6-9e95b5ae7ab8)

### Monthly sales totals for the current year
```
Select Month (OrderDate) AS Sale_Month,
		SUM (TotalSales) AS Monthly_Sales
		FROM [dbo].[LITA Capstone]
		WHERE Year(OrderDate) = 2024
		GROUP BY Month(OrderDate)
		ORDER BY Sale_Month
```
![CURRENT YEAR MONTHLY SALES TOTAL](https://github.com/user-attachments/assets/187bfd80-85fc-4c3c-a4ed-7d8dcdefc768)

### Top 5 customers by total purchase amount
```
Select Top 5 Customer_Id,
SUM(TotalSales) AS Total_Purchase
FROM [dbo].[LITA Capstone]
GROUP BY Customer_Id
ORDER BY Total_Purchase DESC
```
![TOP 5 CUSTOMERS BY TOTAL PURCHASE](https://github.com/user-attachments/assets/76318693-0bc7-4976-ab0b-862f90b5edc3)

### Percentage of total sales contributed by each region
```
Select Region,
SUM(TotalSales) AS Region_Sales,
(SUM(TotalSales) * 100.0 / (Select SUM(TotalSales) 
FROM [dbo].[LITA Capstone])) AS Percentage_of_Total_Sales
FROM [dbo].[LITA Capstone]
GROUP BY Region
```
![% TOTAL SALES OF EACH REGION](https://github.com/user-attachments/assets/58be1bfc-70ce-4b7a-a21a-a4f711486b8d)

### Products with no sales in the last quarter
```
Select Distinct p.Product
FROM [dbo].[LITA Capstone] p
LEFT JOIN [dbo].[LITA Capstone] s ON p.Product = s.Product
AND DATEDIFF(DAY, s.OrderDate,GETDATE()) <=90 
Where s.OrderID is NULL
```
![PRODUCT WITH NO SALES IN LAST QT](https://github.com/user-attachments/assets/3c8a57c7-21af-4682-86df-2a37b6b0c54c)

# Power BI
Powwr BI is a data visualization and business intelligence that converts data from different sources to interactive dashboards and business intelligence reports. The sales data was analyzed using power BI to generate key insights.

### Sales Analysis Dashboard 

![Sales Data Analysis](https://github.com/user-attachments/assets/ba38019f-3398-432b-ad38-84674143a8ce)

![SALES DATA](https://github.com/user-attachments/assets/37da086c-7f76-4c91-86e3-3b3ba51d1250)

## Sales Analysis Summary
- Region by Total Sales: The analysis of region total sales shows a sum total of 2,101,090 in the North, South, East and West.

- Top 5 selling products: The top 5 selling product was achieved using filter. The result showed that Shoes has the highest sales with a total of 613,380 followed by Shirt (485,600), Hat (316195), Gloves (296900) and Jacket (208230) respectively.

- Average Total Sales: The average total sales was achieved using calculated measures. The result showed an average total sales of product to be 212.

- Sum of Total sales by product: This was visualized using a pie chart. The slicer was tracked on the pie chart and result found include the following:
1. Shoes: The highest product sales in the four regions is shoe with a total of 613380 (29%). However, Shoe was sold in the South, East and West, South reported the highest sales among the three regions with average total sales of 309.

2. Shirt: Shirt was sold in North and East with the North sales ranking as the highest-248000 compared to East sales- 237,600. The overall average total sales of the shirt was reported to be 327.
3. Hat: Hat was sold in the West, East and North. West has the highest sales of Hat- 174,300. The overall average total sales of Hat was 159.
4. Gloves: Gloves was sold in South and West region. However, South has the highest sale with a total of 247,600 compared to sales of Gloves in the West (49300). The overall average total sales was 200.
5. Jacket: Jacket was sold in the North and East. The North has the highest sales of jacket-104,280 compared to East sales- 103,950. The overall average total sales was 140
6. Socks: Socks reported sales in South and West region, with South ranking the highest sales- 133,920 compared to West- 46,865. The overall average total sales was reported to be 122.  




