# Task 7: Basic Sales Summary using SQLite and Python

## Overview
This project demonstrates how to connect a Python script to an SQLite database, execute SQL queries to retrieve basic sales data, and visualize the output using a bar chart. The main goal is to generate a summary of total quantity sold and total revenue per product.

## Tools Used
- Python
- SQLite (sqlite3)
- pandas
- matplotlib

## Files Included
- `sales_data.db`: SQLite database containing sample sales records
- `sales_chart.png`: Bar chart representing revenue by product
- `task7_sales_summary.ipynb`: Jupyter/Colab notebook with all code and outputs

## Key Concepts
- Connecting SQLite database using Python
- Running SQL queries from Python
- Using GROUP BY to summarize data
- Importing SQL results into pandas
- Plotting data using matplotlib

## SQL Query Used
```sql
SELECT product, 
       SUM(quantity) AS total_qty, 
       SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
