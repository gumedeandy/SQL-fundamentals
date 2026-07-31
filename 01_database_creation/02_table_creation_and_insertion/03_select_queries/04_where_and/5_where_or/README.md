# Filtering Data with WHERE OR

## Overview
The `WHERE` clause filters rows based on conditions.  
Using `OR` allows you to include rows that meet **at least one** of the conditions.

## Syntax
```sql
SELECT column1, column2
FROM table_name
WHERE condition1 OR condition2;

SELECT full_name, email
FROM customers
WHERE date_of_birth < '1990-01-01'
OR email LIKE '%gmail.com';

Notes
OR requires at least one condition to be true.

Combine with AND for more complex filtering.

Use parentheses () when mixing AND and OR to control logic order.
