---
Author: AAM
Date: 2024-03-19
tags:
  - "#programming"
  - SQL
  - DB
---

---
# 04 Queries

[Back to index]()

---

## Simple Queries

- Syntax: `SELECT [properties] FROM [table] WHERE [condition]`
- We can use `*` as `[properties]` to specify all properties in the table.
- Elements can be ordered:
	- Ascending order with `ORDER BY [property] ASC`.
	- Descending order with `ORDER BY [property] DESC`.

```sql
-- Displays a list of names from table1
SELECT table1_name FROM table1;

-- Displays a list of IDs and names from table1
SELECT table1_id, table1_name FROM table1;

-- Displays a all properties of the second tuple in table1
SELECT * FROM table1 WHERE table1_id = 2;

-- Displays a list of names from table1 in ascending order.
SELECT table1_name FROM table1 ORDER BY table1_name ASC;
```

## Intersection, Union and Minus

- Syntax: `SELECT [table]`

![](/Assets/Programming/Databases/SQL_1.png)

```SQL
-- Display all names in erasmus AND student.
-- A x B : erasmus x student
(SELECT name FROM erasmus) INTERSECT (SELECT name FROM student)

-- Display all names in student OR teacher.
-- A + B : teacher + student
(SELECT name FROM teacher) UNION (SELECT name FROM student)

-- Display all names in student NOT IN erasmus.
-- A - B : student - erasmus
(SELECT name FROM student) EXCEPT (SELECT name FROM erasmus)
```

## Joining Queries

![](/Assets/Programming/Databases/SQL_2.png)

```SQL
SELECT name FROM ()
```