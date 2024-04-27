
---
# 05 Functions & Procedures

[Back to index](../../index.md)

---
## Function vs Procedure
- Functions perform an calculation and return a result.
- Procedures perform an operation and return no value.
---
## Functions
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
	END;
$$ languaje plpgsql;
```
### Using a function
```SQL
SELECT my_function(params);
```

---
## Procedures
```SQL
CREATE PROCEDURE proc_name (param type, ..., INOUT out_name type)
RETURNS type AS
$$
	BEGIN
		SELECT prop_name INTO out_name FROM ...
	END;
$$ languaje plpgsql;
```
---
## PL/pgSQL code
### Param & exceptions
- Inside the PL/pgSQL code of a function/procedure.
- Replace `%` with the `$1` which refers to the first param.
- An alias can also be specified
```sql
$$
BEGIN
	...
	IF NOT FOUND THEN
		RAISE EXCEPTION '... % ...', $1;
END;
$$
```

```sql
$$
DECLARE alias_name ALIAS FOR $1;
BEGIN
	...
	IF NOT FOUND THEN
		RAISE EXCEPTION '... % ...', alias_name;
END;
$$
```
### For loops
- Used to iterate over the values of a query.
```sql
$$
BEGIN
	FOR var_name IN query
	LOOP
		...
	END LOOP;
END;
$$
```

```sql
$$
BEGIN
	FOR var_name IN value..value
	LOOP
		...
	END LOOP;
END;
$$
```
### Notices
```sql
$$
BEGIN
	...
	RAISE NOTICE '... % ...', var_name;
END;
$$
```