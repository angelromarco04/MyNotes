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

- Syntax: `INSERT INTO [table] VALUES( [values ...] )`
```sql
-- table1 is a table with 3 properties.
-- value1, value2 and value3 must have the proper datatypes.
INSERT INTO table1 VALUES(value1, value2, value3);
```

## Delete tuples
- Syntax: `DELETE FROM [table] WHERE [condition]`
```sql
-- Delete from table1 the second tuple
DELETE FROM table1 WHERE table1_id = 2;

-- Delete all tuples of table1 
DELETE FROM table1;
```

## Update tuples

- Syntax: `update [table] set [propertie = new value] where [condition]`
```sql
-- Set property name of all tuples of table1 to "A"
update table1 set table1_name = "A";

-- Set property name of second tuple of table1 to "B"
update table1 set table1_name = "B" where table1_name = 2;
```
