
---
# 05 Functions & Procedures

[Back to index](../../index.md)

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
---
## Procedures