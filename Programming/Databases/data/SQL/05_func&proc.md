
---
# 05 Functions & Procedures

[Back to index](../../index.md)

---

## PL/pgSQL

---
## Functions
### Characteristics
### Return a value
```sql
CREATE FUNCTION func_name (param type, ...) RETURNS type AS
$$
	DECLARE
		var_name type;
		...
	BEGIN
		statement
	END;
$$ languaje plpgsql;
```
### Return a table

---
## Procedures