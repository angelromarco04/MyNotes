---
Author: AAM
Date: 2024-02-09
tags:
  - "#programming"
  - SQL
---

---
# 01 Basic notions

[Back to index](Programming/SQL/SQL.md)

---

## PSQL shell commands

- Get help: `\?`
- Salir del intérprete: `\q` 
- List all databases: `\l`
- Remove a database: `drop database database_name`
- List all tables: `\dt`
- Describe a table: `\d table_name`
- List available functions in the current database: `\df`
- List available views: `\dv`
- Command history: `\s`
- Execute psql commands from a file: `\i filename`
- Switch connection to a new database: `\c dbname username`


## Datatypes

- Boolean (`true`, `false`, `null`)
- Character (strings):
	- `char(n)`: Fixed length of n characters.
	- `varchar(n)`: Variable length up to n characters.
	- `text`: Unlimited length of characters
- Numeric:
	- Integer:
		- `smallint`: 2B signed integer.
		- `int`: 4B signed integer.
		- `serial`: Auto resizable integer.
	- Floating point:
		- `float(n)`: Variable length up to 8B with at least n precision.
		- `real` or `float8`: 4B floating point number.
		- `numeric` or `numeric(p, s)`: real number with p digits and s after decimal point.
- Temporal
	- `date`
	- `time`
	- `timestamp` (date + time)
	- `timestamptz` (date + time + timezone)
	- `interval` (periods of time)

## Creating tables

- Repeated table names are not allowed.
- By convention properties are named: `tableName_propertie`
- Properties are specified as: `name datatype constraints`
- Types of constraints:
	- `not null`
	- `unique`
	- `primary key`
	- `check`
	- `foreign key`
	
- Each table should have a primary key.

```sql
CREATE TABLE exampleTable (
	exampleTable_id serial primary key,
	exampleTable_name varchar(50) unique not null,
	exampleTable_prop smallint
);
```

- We can make relations by specifying  