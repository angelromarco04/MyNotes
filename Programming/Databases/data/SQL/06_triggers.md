
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
- `ROW`. Trigger is called 
- `STATEMENT`