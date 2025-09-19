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
- Show all customer records
  Show all customer records

SELECT * FROM customers;

