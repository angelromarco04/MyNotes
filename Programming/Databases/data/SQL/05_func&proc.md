
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
CREATE FUNCTION func_name (param type, ...)
RETURNS type AS
$$
	DECLARE
		var_name type;
		...
	BEGIN
		SELECT prop_name INTO var_name FROM ...
	END;
$$ languaje plpgsql;
```
### Return a table
```sql
CREATE FUNCTION func_name (param type, ...)
RETURNS TABLE(var_name type, ...) AS
$$
	BEGIN
		RETURN QUERY SELECT ...
		IF NOT FOUND
			THEN RAISE EXCEPTION '... % ...', $1;
	END;
$$ languaje plpgsql;
```
### PL/pgSQL param & exceptions
- Inside the PL/pgSQL code of a function/procedure.
- Replace Use `$1` to refer to the first param.
```sql
IF NOT FOUND
	THEN RAISE EXCEPTION '... % ...', $1;
```
---
## Procedures