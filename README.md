## Capstone_Project_1

### Project Title: Sales Data Analysis

[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning and Preparations](#data-cleaning-and-preparations)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

[Data Visualization](#data-visualization)

### Project Overview
---
Sales data encompasses various pieces of information related to sales transactions. It is crucial for businesses to understand their sales performance and customer behaviour, identify trends, and make informed decisions. In essence, sales data is a goldmine of insights that can drive straregic decision making and enhance overall business performance.

### Data Sources
---
The primary source of Data used here is sales data from microsoft excel worksheet given by Mr Muhsin Hameed from Ladies in Tech Africa in Conjunction with The Incubator Hub.

### Tools Used
---
- Microsoft Excel 
  1. For Data Cleaning
  2. For Analysis
  3. For Visualization
- SQL- Structured Query Language for Queying Data
- Power BI
  1. For Integration
  2. For Transformation
  3. For Visualization
-  GitHub for portfolio Building

### Data Cleaning and Preparations
---
At the initial phase of the Data cleaning and preparations, we perform the following actions;
   1.  Data loading and inspection
   2.  Handling missing variables
   3.  Data cleaning and formatting

### Exploratory Data Analysis
---
EDA is all about making your data talk to you in such a way that you get a clearer understanding of the data itself. Listed below are the various ways you could exlpore your data to get more insights;
- The average sales per product
- Total revenue by region
- Monthly sales for the current year
- Top 5 customers by total purchase amount
- Percentage of total sales contributed by each region
- Products with no sales in  the last quarter of the year
- Top performing products.

  ### Data Analysis
  ---
  This is where i include some basic lines of code /queries used during the 
  analysis;

  ```SQL
  Create Database Capstone_Project1
  ```
```  SELECT * FROM[dbo].[SalesDATA ProJECT 1]```
```SQL
Select Product, SUM(Total_Sales) AS Total_Sales from[dbo].[SalesDATA ProJECT 1]
Group by Product
```
```SQL
select region, count(*) AS Number_of_Sales_Transactions from[dbo].[SalesDATA ProJECT 1]
Group by Region
```
```SQL
select Top 1 Product, sum(Total_Sales) AS Highest_Selling_Product from[dbo].[SalesDATA ProJECT 1]
```
```SQL
SELECT
    Region,
	SUM(Total_Sales) AS Region_Sales_Total,
	(SUM(Total_Sales)*100) / (SELECT SUM(Total_Sales)FROM[dbo].[SalesDATA ProJECT 1])
	AS Sales_Percentage
From[dbo].[SalesDATA ProJECT 1]
Group By
  Region
```
```SQL

SELECT Product FROM[dbo].[SalesDATA ProJECT 1]
GROUP BY Product
Having Sum (CASE WHEN OrderDate BETWEEN '2024-06-01' AND '2024-08-31'
THEN 1 ELSE 0 END)=0
```
```SQL
SELECT TOP (5) Customer_ID,
SUM(Total_Sales) AS Total_Purchase_Amount
FROM[dbo].[SalesDATA ProJECT 1]
GROUP BY Customer_ID
ORDER BY Total_Purchase_Amount
DESC
```
```SQL
select region, count(*) AS Number_of_Sales_Transactions from[dbo].[SalesDATA ProJECT 1]
Group by Region
```
Data Visualization
---

![Sales Data Dashboard](https://github.com/user-attachments/assets/e4d854bd-dcfc-44bf-82e4-f7908d709adc)

![Pivot Tables for Sales Data](https://github.com/user-attachments/assets/1773eb0a-3e09-41e7-bef4-1b2357b432ad)


![SQL 1](https://github.com/user-attachments/assets/21d33234-1946-48d2-be4d-85ade3617bb5)


![SQL](https://github.com/user-attachments/assets/1f3975b9-7d9d-43a1-a0b8-e826c2ce5760)

![SQL](https://github.com/user-attachments/assets/ec671dfc-fdab-4a29-8c5f-8ef5ed533822)



