---
Author: AAM
Date: 2024-03-18
tags:
  - "#programming"
  - SQL
---

---
# 02 Tables Creation

[Back to index](../../DATABASES.md)

---

## Datatypes

- **Boolean** (`true`, `false`, `null`)
- **Character** (strings):
	- `char(n)`: Fixed length of n characters.
	- `varchar(n)`: Variable length up to n characters.
	- `text`: Unlimited length of characters
- **Numeric**:
	- Integer:
		- `smallint`: 2B signed integer.
		- `int`: 4B signed integer.
		- `serial`: Auto resizable integer.
	- Floating point:
		- `float(n)`: Variable length up to 8B with at least n precision.
		- `real` or `float8`: 4B floating point number.
		- `numeric` or `numeric(p, s)`: real number with p digits and s after decimal point.
- **Temporal**
	- `date`
	- `time`
	- `timestamp` (date + time)
	- `timestamptz` (date + time + timezone)
	- `interval` (periods of time)

## Creating Simple Tables

- Repeated table names are not allowed.
- By convention properties are named: `tableName_propertie`

```sql
CREATE TABLE [IF NOT EXISTS] table_name (
    column1 datatype(length) column_constraint,
    column2 datatype(length) column_constraint,
    ...,
    table_constraints
);
```

## Constraints

1. **Primary Key** (Identifies a row in the table).
```sql
CREATE TABLE employees (
employee_id SERIAL PRIMARY KEY,
-- Other columns...
);
```

2. **Unique** (Column values are unique).
```sql
CREATE TABLE students (
	student_id SERIAL PRIMARY KEY,
	email VARCHAR(100) UNIQUE,
	-- Other columns...
);
```

3. **Not Null** (Column cannot  be empty)
```sql
CREATE TABLE orders (
	order_id SERIAL PRIMARY KEY,
	customer_id INT NOT NULL,
	-- Other columns...
);
```

4. **Check** (Validates data based on a condition)
```sql
CREATE TABLE products (
	product_id SERIAL PRIMARY KEY,
	price DECIMAL CHECK (price > 0),
	-- Other columns...
);
```
        
5. **Foreign Key** (Establishes a relationship between two tables)
```sql
CREATE TABLE orders (
order_id SERIAL PRIMARY KEY,
customer_id INT,
FOREIGN KEY (customer_id) REFERENCES customers(customer_id)
-- Other columns...
);
```
        

Remember to adjust these constraints based on your specific use case. Each constraint ensures data consistency and helps maintain the integrity of your database. 🛡️🔍






- We can make relations by specifying foreign keys.
```sql
CREATE TABLE otherTable (
	otherTable_id int primary key not null,
	otherTable_name varchar(50) unique not null,

	primary key(exampleTable_id),
	foreign key(exampleTable_id) references exampleTable(exampleTable_id)
);
```

- Relations many to many intermediate tables are created as: `table1_table2`.
- There is no need to specify a primary key for the table.
```sql
CREATE TABLE table1_table2 (
	primary key(table1_id, table2_id),
	foreign key(table1_id) references table1(table1_id),
	foreign key(table2_id) references table2(table2_id),
);
```