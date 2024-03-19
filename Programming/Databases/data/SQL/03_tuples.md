---
Author: AAM
Date: 2024-03-18
tags:
  - "#programming"
  - SQL
  - DB
---

---
# 03 Tuples Management

[Back to index](../../DATABASES.md)

---
## Inserting tuples

- Syntax: `insert into [table] values( [values] )`
```sql
-- table1 is a table with 3 properties.
-- value1, value2 and value3 must have the proper datatypes.
insert into table1 values(value1, value2, value3);
```

## Delete tuples
- Syntax: `delete from [table] where [condition]`
```sql
-- Delete from table1 the second tuple
delete from table1 where table1_id = 2;

-- Delete all tuples of table1 
delete from table1;
```

## Display tuples

- Syntax: `select [properties] from [table] where [condition]`
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

## Update tuples

- Syntax: `update [table] set [propertie = new value] where [condition]`
```sql
-- Set property name of all tuples of table1 to "A"
update table1 set table1_name = "A";

-- Set property name of second tuple of table1 to "B"
update table1 set table1_name = "B" where table1_name = 2;
```
