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

### Basic

- Get help: `\?`
- Salir del intérprete: `\q`
- Connect to a database: `\c dbname username`
- Command history: `\s`
### Databases
- List all databases: `\l`
- List available functions in the current database: `\df`
- Execute PSQL commands from a file: `\i filename`
- Remove a database: `drop database database_name`

> [!WARNING]
> Is not possible to delete the currently active database.
### Tables
- List all tables: `\dt`
- Describe a table: `\d table_name`
- List available views: `\dv`

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

---
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
	exampleTable_id int primary key not null,
	exampleTable_name varchar(50) unique not null,
	exampleTable_prop smallint
);
```

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

---
## Managing tuples

### Inserting tuples

- Syntax: `insert into [table] values( [values] )`
```sql
-- table1 is a table with 3 properties.
-- value1, value2 and value3 must have the proper datatypes.
insert into table1 values(value1, value2, value3);
```

### Delete tuples
- Syntax: `delete from [table] where [condition]`
```sql
-- Delete from table1 the second tuple
delete from table1 where table1_id = 2;

-- Delete all tuples of table1 
delete from table1;
```

### Display tuples

- Syntax: `select [properties] from [table] where [condition]`
- We can use `*` as properties to specify all properties in the table.
```sql
-- Displays a list of names from table1
select table1_name from table1;

-- Displays a list of IDs and names from table1
select table1_id, table1_name from table1;

-- Displays a all properties of the second tuple in table1
select * from table1 where table1_id = 2;
```

### Update tuples

- Syntax: `update [table] set [propertie = new value] where [condition]`
```sql
-- Set property name of all tuples of table1 to "A"
update table1 set table1_name = "A";

-- Set property name of second tuple of table1 to "B"
update table1 set table1_name = "B" where table1_name = 2;
```

---
## Managing columns

### Add new columns

- Syntax: `alter table [table] add column [new property] [datatype]`
```sql
-- Add property extra to table1.
alter table table1 add column table1_extra varchar(30);

-- Usually we set a value to all collumn.
update table1 set table1_extra = "text";
```

### Delete columns

- Syntax: `alter table [table] drop[property]`
```sql
-- Delete property extra from table1.
alter table table1 drop table1_extra;
```

---
