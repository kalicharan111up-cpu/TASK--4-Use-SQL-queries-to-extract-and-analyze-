# TASK--4-Use-SQL-queries-to-extract-and-analyze-
This repository is about the SQL queries extraction and analysis.


Here’s a concise summary of common SQL queries used to explore and analyze an eCommerce dataset:
🛒 Key SQL Query Types for eCommerce
1. Customer Insights
- SELECT COUNT(*) FROM customers; → Total number of customers
- SELECT country, COUNT(*) FROM customers GROUP BY country; → Customer distribution by country
- SELECT * FROM customers WHERE signup_date > '2025-01-01'; → Recent signups
  
2. Order Analysis
- SELECT COUNT(*) FROM orders; → Total orders
- SELECT customer_id, COUNT(*) FROM orders GROUP BY customer_id; → Orders per customer
- SELECT * FROM orders WHERE order_status = 'Returned'; → Returned orders
  
3. Sales & Revenue
- SELECT SUM(total_amount) FROM orders; → Total revenue
- SELECT product_id, SUM(quantity) FROM order_items GROUP BY product_id; → Best-selling products
- SELECT DATE(order_date), SUM(total_amount) FROM orders GROUP BY DATE(order_date); → Daily sales trend
  
4. Product Performance
- SELECT * FROM products WHERE stock_quantity < 10; → Low-stock products
- SELECT category, COUNT(*) FROM products GROUP BY category; → Product count by category
  
5. Customer Behavior
- SELECT customer_id, AVG(total_amount) FROM orders GROUP BY customer_id; → Average spend per customer
- SELECT customer_id FROM orders GROUP BY customer_id HAVING COUNT(*) > 5; → Repeat customers
