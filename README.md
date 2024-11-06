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
- Retrieve the total sales for each product category
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
```  SELECT * FROM[dbo].[SalesDATA ProJECT 1]
```

retrieve the total sales for each product category

```SQL
Select Product, SUM(Total_Sales) AS Total_Sales from[dbo].[SalesDATA ProJECT 1]
Group by Product
```

Find the number of sales transactions in each region

```SQL
select region, count(*) AS Number_of_Sales_Transactions from[dbo].[SalesDATA ProJECT 1]
Group by Region
```

find the highest selling product by total sales value

```SQL
select Top 1 Product, sum(Total_Sales) AS Highest_Selling_Product from[dbo].[SalesDATA ProJECT 1]
```

calculate the percentage of total sales contributed by each region

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

products with no sales in the last quarter

```SQL
SELECT Product FROM[dbo].[SalesDATA ProJECT 1]
GROUP BY Product
Having Sum (CASE WHEN OrderDate BETWEEN '2024-06-01' AND '2024-08-31'
THEN 1 ELSE 0 END)=0
```

find Top 5 Customers by total purchase Amount

```SQL
SELECT TOP (5) Customer_ID,
SUM(Total_Sales) AS Total_Purchase_Amount
FROM[dbo].[SalesDATA ProJECT 1]
GROUP BY Customer_ID
ORDER BY Total_Purchase_Amount
DESC
```

Find the number of sales transactions in each region

```SQL
select region, count(*) AS Number_of_Sales_Transactions from[dbo].[SalesDATA ProJECT 1]
Group by Region
```
Data Visualization
---
![Ave Sales per Product    Total Sales per Region](https://github.com/user-attachments/assets/6cbf9142-5697-4ee1-a76a-3f1580baa9b8)

![Pivot Tables](https://github.com/user-attachments/assets/413d45e3-443d-4edf-bd79-8311c932b653)

![Sales Data DashBoard (2)](https://github.com/user-attachments/assets/94f226de-c7e8-41a9-a810-f04cf3214811)

![SQL Sales Data Table 1](https://github.com/user-attachments/assets/5190f5bc-bfe8-49cd-bf07-658cfde351e0)

![SQL Top 5 Customers](https://github.com/user-attachments/assets/261aab7c-4313-4b04-a584-848bc28571b8)

![SQL Total sales per Product](https://github.com/user-attachments/assets/42fa676d-4806-4f2e-b5d7-3ac23f904eb8)

![SQL % of Total Sales per Region](https://github.com/user-attachments/assets/090cfb9e-4f6b-44de-a4ab-82de5d3cce1b)

![SQL Revenue per Product](https://github.com/user-attachments/assets/a4dacf0e-3299-4767-a5c4-9db513dd50c3)

![SQL Total Sales for each Product](https://github.com/user-attachments/assets/233514a3-c8c1-44b0-bac3-2cbae0f86688)

![SQL Monthly Sales](https://github.com/user-attachments/assets/0caecb8c-2868-4d1b-8996-1e2b0277df0a)


