
---
# 06 Triggers

[Back to index](../../index.md)

---
## Creation
```sql
CREATE TRIGGER trigger_name 
{ BEFORE | AFTER } { INSERT | UPDATE | DELETE [OR …] }
ON table_name [ FOR [ EACH ] {ROW | STATEMENT} ]
[ WHEN ( condition ) ]
EXECUTE PROCEDURE func_name (args)
```

## Levels
- `ROW`. Trigger is called for every row the operation modifies.
- `STATEMENT`. Executed once per operation
	(No matter the number of rows modified)
## Variables
- `NEW` contains the new row (insert/update).
- `OLD` contains the old row (delete/update).
- TG_WHEN returns `BEFORE` or `AFTER`.
- TG_LEVEL returns `ROW` or `STATEMENT`.
- TG_OP returns `INSERT`, `UPDATE` OR `DELETE`.
- TG_TABLE_NAME returns the table