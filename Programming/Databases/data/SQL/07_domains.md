
---
# 07 Domains

[Back to index](../../index.md)

---
## Definition
- Is a data type with some optional restrictions.

```postgresql
CREATE DOMAIN domain_name AS data_type
[COLLATE collation] [DEFAULT expression] [constraint […]]
```

- The collation is a function that defines the comparation for ordering rows.
- The constraint can be:
	- `NULL`
	- `NOT NULL`
	- `CHECK(...)`

## Checking text patterns
```postgresql
CHECK( value ~ 'pattern')
```

- `%` is used to represent any sequence of 0 or more characters.
- `_` is used to represent any character (only one).
- `\w` is used to represent a 