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

1. **Primary Key** (Identifies a row in the table. Usually one).
```sql
CREATE TABLE student (
	student_id SERIAL PRIMARY KEY,
	-- More...
);

CREATE TABLE book (
	book_ISBN int,
	book_version int,
	-- More...

	PRIMARY KEY (book_ISBN, book_version)
);
```

2. **Unique** (Column values are unique).
```sql
CREATE TABLE student (
	student_id SERIAL PRIMARY KEY,
	student_email VARCHAR(100) UNIQUE,
	-- More...
);
```

3. **Not Null** (Column cannot  be empty)
```sql
CREATE TABLE student (
	student_id SERIAL PRIMARY KEY,
	student_name VARCHAR(100) NOT NULL,
	-- Other columns...
);
```

4. **Check** (Validates data based on a condition)
```sql
CREATE TABLE book (
	book_id SERIAL PRIMARY KEY,
	book_price int CHECK (book_price > 0),
	book_discount int,
	-- Other columns...
	
	CHECK (book_price > book_discount),
	-- Other way
	CONSTRAINT valid_discount CHECK (book_price > book_discount)
);
```

5. **Default** (Sets a default value)
```sql
CREATE TABLE student (
	student_id SERIAL PRIMARY KEY,
	student_erasmus bool DEFAULT 'no',
	-- Other columns...
);
```

6. ***Foreign Key** (Establishes a relationship between two tables)
```sql
CREATE TABLE classroom (
    id_classroom int PRIMARY KEY not null,
    id_location int not null,
    -- Other columns...
    
    FOREIGN KEY (id_location) REFERENCES location(id_location),
);
```

7. **On update cascade** (Tuples are updated when modified in the relation)
```sql
CREATE TABLE student (
    id_student int PRIMARY KEY not null,
    lecture_name int,
    -- Other columns...
    
    FOREIGN KEY (lecture_name)
	    REFERENCES lecture(lecture_name) ON UPDATE CASCADE,
);
```

8. **On delete cascade** (Tuples are removed when deleted in the relation)
```sql
CREATE TABLE student (
    id_student int PRIMARY KEY not null,
    lecture_name int,
    -- Other columns...
    
    FOREIGN KEY (lecture_name)
	    REFERENCES lecture(lecture_name) ON DELETE CASCADE,
);
```

## Relations

1. **One to many**
```sql
CREATE TABLE classroom (

    id_classroom int PRIMARY KEY not null,
    id_location int not null,
    
    FOREIGN KEY (id_location) REFERENCES location(id_location),
);
```
2. **Many to many**
```sql
CREATE TABLE teach (

    id_bachelor int not null,
    id_teacher int not null,

    FOREIGN KEY (idbachelor) REFERENCES bachelor(id_bachelor),
	FOREIGN KEY (id_teacher) REFERENCES teacher(id_teacher),

    PRIMARY KEY (id_academic_bachelor, id_teacher)

);
```
3. **Aggregation**
```sql
CREATE TABLE practice (
    id_bachelor int not null,
    id_teacher int not null,
    id_enterprise int,
    
    FOREIGN KEY (id_bachelor, id_teacher)
	    REFERENCES teach(id_academic_bachelor, id_teacher),
	    
    FOREIGN KEY (id_enterprise) REFERENCES enterprise(id_enterprise),

    PRIMARY KEY (id_academic_bachelor, id_teacher, id_enterprise)

);
```

## Specification

```SQL
CREATE TABLE student (
    id_student int PRIMARY KEY not null,
    FOREIGN KEY (id_student) references university(id_member),
);
```