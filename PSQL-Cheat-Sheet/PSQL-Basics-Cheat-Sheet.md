# Complete PostgreSQL Cheat Sheet

-----

## 1. Create a Database


```sql
CREATE DATABASE db_name
   WITH
   OWNER            = owner_name
   ENCODING         = 'UTF-8'
   CONNECTION LIMIT = -1
```

## 2. Create Table

```
CREATE TABLE table_name
{
    column 1 DATA_TYPE primary key,
    column 2 DATA_TYPE REFERENCES foreign_table_name (field_name),
    column 3 DATA_TYPE
}
```

An example:

```sql
CREATE TABLE simple_table
{  
    id SERIAL PRIMARY KEY,  
    name VARCHAR(50) NOT NULL,
    address VARCHAR(400),  
    mobile_number INT,  
    aadhar_number VARCHAR(9) REFERENCES aadhar_details (aadhar_id)  
}
```