# Filtering Data with WHERE AND

## Overview
The `WHERE` clause filters rows based on conditions.  
Using `AND` allows you to apply multiple conditions at once.

## Syntax
```sql
SELECT column1, column2
FROM table_name
WHERE condition1 AND condition2;

SELECT full_name, email
FROM customers
WHERE date_of_birth > '1990-01-01'
AND email LIKE '%example.com';

WHERE full_name = John Doe; -- ❌ Wrong
WHERE full_name = 'John Doe'; -- ✅ Correct
