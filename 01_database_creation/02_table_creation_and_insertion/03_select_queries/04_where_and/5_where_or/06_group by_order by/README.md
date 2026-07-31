# GROUP BY and ORDER BY

## Overview
- `GROUP BY` is used to arrange identical data into groups.  
- `ORDER BY` is used to sort the results in ascending (`ASC`) or descending (`DESC`) order.  
- Together, they help summarize and organize query results.

## Syntax
```sql
SELECT column1, aggregate_function(column2)
FROM table_name
GROUP BY column1
ORDER BY aggregate_function(column2) DESC;


SELECT customer_id, COUNT(order_id) AS total_orders
FROM orders
GROUP BY customer_id;

SELECT customer_id, COUNT(order_id) AS total_orders
FROM orders
GROUP BY customer_id
ORDER BY total_orders DESC;

## Notes
- Every column in the `SELECT` list that is **not aggregated** must appear in the `GROUP BY`.  
- Use aggregate functions like `COUNT()`, `SUM()`, `AVG()`, `MAX()`, and `MIN()` with `GROUP BY` to summarize data.  
- `ORDER BY` can sort by column names or by aliases (like `total_orders`).  
- Default sort is ascending (`ASC`); use `DESC` for descending.  
- You can combine `GROUP BY` and `ORDER BY` to first group data, then sort the grouped results.  
