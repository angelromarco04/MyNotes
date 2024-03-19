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
- We can use `*` as properties to specify all properties in the table.
- Elements can be ordered:
	- Ascending order with `order by [property] asc`.
	- Descending order with `order by [property] desc`.

```sql
-- Displays a list of names from table1
select table1_name from table1;

-- Displays a list of IDs and names from table1
select table1_id, table1_name from table1;

-- Displays a all properties of the second tuple in table1
select * from table1 where table1_id = 2;

-- Displays a list of names from table1 in ascending order.
select table1_name from table1 order by table1_name asc;
```
