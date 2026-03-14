
# 📊 End-to-End Data Analytics Project: Azure SQL & Power BI

📌 Project Overview

This project demonstrates an end-to-end data analytics workflow using Azure SQL Database and Power BI to transform raw data into actionable business insights.

The workflow involves loading raw data into Azure SQL, performing data cleaning using SQL, connecting the cleaned data to Power BI Desktop, and building an interactive dashboard to answer key business questions.

The goal of this project is to showcase practical data analytics skills including SQL data transformation, cloud database usage, and data visualization using Power BI.


# 🎯 Business Problem

Retail businesses often manage hundreds of brands and products, making it difficult to understand:

* Which brands offer the highest discounts

* Which brands generate the highest profit margins

* Which brands have the largest product variety

* Which brands are underperforming

This project analyzes brand-level data to uncover pricing strategies and profitability patterns using SQL and Power BI.


# 🛠️ Tools & Technologies

| Technology         | Purpose                          |
| ------------------ | -------------------------------- |
| Azure SQL Database | Cloud data storage               |
| SQL (T-SQL)        | Data cleaning and transformation |
| Power BI Desktop   | Data visualization               |
| Power Query        | Data transformation              |
| DAX                | Calculated measures              |
| GitHub             | Documentation & project hosting  |


# 🏗️ Project Architecture
```
Raw Dataset
     ↓
Azure SQL Database
     ↓
SQL Data Cleaning
     ↓
Power BI Connection
     ↓
Power Query Transformation
     ↓
Data Modeling (DAX)
     ↓
Interactive Dashboard
     ↓
Business Insights
```

# 📂 Dataset Description

The dataset contains fashion product and brand-level information-

* Brand Name

* Title

* Marked Price

* Discount Percentage

* Profit Percentage

* Sales Price

* Cost Price

This dataset allows analysis of brand performance, pricing strategies, and profitability.


# 🧹 Data Cleaning Using SQL (Azure SQL Database)


* Data preprocessing was performed in Azure SQL Database to prepare the dataset for analysis-

Key cleaning steps included:

* Identifying Unwanted Characters and removing them
* Handling Missing/Invalid Data
* Whitespace & Character Removal
* Type Casting
* Standardizing product data

  Example SQL query-

```sql
SELECT TOP (1000) * FROM [dbo].[Men+Tshirt]

update [dbo].[Men+Tshirt]
set original_price=trim(replace(cast(original_price as varchar (max)),'?',''))
where original_price like '%?%'

update [dbo].[Men+Tshirt]
set sale_price=trim(replace(cast(sale_price as varchar (max)),'?',''))
where sale_price like '%?%'

```


# 🔗 Connecting Azure SQL Database to Power BI

After cleaning the dataset in Azure SQL Database, the database was connected to Power BI Desktop.

Steps performed:

1) Connected Power BI to Azure SQL Database
2) Imported cleaned tables
3) Applied additional transformations using Power Query
4) Created relationships and data model

This enabled real-time analysis from a cloud database environment.


# 📊 Power BI Dashboard Development-

* An interactive Power BI dashboard was created to visualize product pricing and discount trends.

* The Power BI dashboard includes:

1) Brand filtering using slicers
2) Comparative brand analysis
3) Visual insights into pricing and discount patterns
4) Brand profitability analysis
5) Users can dynamically explore brand-level performance metrics.


# 🖥️ Dashboard Preview

Main Dashboard- 








