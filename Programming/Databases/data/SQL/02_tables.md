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
		- `serial`: Auto incrementable integer.
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

- Column constraints can only reference the value of that column.
- Table constraints can reference any column.
## Types of Constraints

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


## Relations

1. **One to many**
```sql

```
2. **Many to many**
```sql
CREATE TABLE Enrollments (
    student_id INT not null,
    course_id INT not null,
    FOREIGN KEY (student_id) REFERENCES Students(student_id),
    FOREIGN KEY (course_id) REFERENCES Courses(course_id),
    PRIMARY KEY (student_id, course_id)
);
```
3. **Aggregation**
```sql
CREATE TABLE practice (
    id_bachelor int not null,
    id_teacher int not null,
    id_enterprise int,
    
    foreign key (id_bachelor, id_teacher) references teach(id_academic_bachelor, id_teacher),

    foreign key (id_enterprise) references enterprise(id_enterprise),

    primary key (id_academic_bachelor, id_teacher, id_enterprise)

);
```
