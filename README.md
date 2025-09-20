# Sales Insight Data Analysis

This repository provides SQL-based analysis of the [Sales Insight Data](https://www.kaggle.com/datasets/gunjanpatidar/sales-insight-data) dataset.  
---
## Project Goals

- Load dataset into a relational database  
- Explore customers, products, markets, and orders  
- Build reusable SQL queries for KPIs and dashboards  
- Validate business rules with “SQL screens” (query + expected output format)  
---
## Data Model

Dimensions and facts:
- `dim_customer`  
- `dim_product`  
- `dim_market`  
- `dim_date`  
- `fact_sales_order`

## Entity Relation Diagram
- <img width="791" height="601" alt="image" src="https://github.com/user-attachments/assets/912a0969-66d0-4a25-9340-0128536ba9d9" />

## Data Analysis Using SQL

**Query 1** - Show all customer records

- SELECT * FROM customers;

**Query 2** - Show transactions where currency is US dollars

- SELECT * from transactions where currency="USD"
<img width="891" height="296" alt="image" src="https://github.com/user-attachments/assets/ff2152c9-856b-4fd2-b523-e003ed60d517" />


**Query 3** - Show distinct product codes that were sold in Chennai

- SELECT distinct product_code FROM transactions where market_code='Mark001';
<img width="807" height="865" alt="image" src="https://github.com/user-attachments/assets/c7c3eea9-4923-46c2-84bb-76529f36f727" />

**Query 4** - Show transactions in 2020 join by date table

- SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;
<img width="1125" height="898" alt="image" src="https://github.com/user-attachments/assets/c7b38422-cffa-4473-96c0-0451c3dea2f2" />

**Query 5** - Show total revenue in year 2020,

- SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";
<img width="781" height="315" alt="image" src="https://github.com/user-attachments/assets/b387e83e-4df3-4bda-911c-cc82c224c251" />

