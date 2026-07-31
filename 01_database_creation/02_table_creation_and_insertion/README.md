# Table Creation and Data Insertion

## Overview
Tables are the core structures in a database that store data in rows and columns. Each table represents a specific entity, such as customers, products, or orders.

## Learning Objectives
- Understand how to define table structure
- Learn SQL data types and constraints
- Create tables using SQL
- Insert data into tables

## SQL Syntax

### Creating a Table
```sql
CREATE TABLE customers (
    customer_id INT PRIMARY KEY,
    full_name VARCHAR(100),
    email VARCHAR(100),
    date_of_birth DATE
);

INSERT INTO customers (customer_id, full_name, email, date_of_birth)
VALUES (1, 'Jane Doe', 'jane.doe@example.com', '1990-05-15');


## Notes
- Always define a **primary key** for uniqueness.  
- Choose the right **data type** for each column.  
- Use `NOT NULL` when a column must always have a value.  
- Insert multiple rows with one `INSERT` statement for efficiency.  

### Common Errors
- Forgetting quotes around text values:  
  ```sql
  INSERT INTO customers (full_name) VALUES (Jane Doe); -- ❌ Wrong
  INSERT INTO customers (full_name) VALUES ('Jane Doe'); -- ✅ Correct

