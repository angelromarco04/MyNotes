---
Author: AAM
Date: 2024-02-20
tags:
  - "#programming"
  - SQL
---

---
# 02 Relational Algebra

[Back to index](Programming/SQL/SQL.md)

---

## Selection (σ)

- Selection allows to filter tuples by conditions.
- Done with the keyword `where [condition]`.

```SQL
select * from university where year = 1;
select * from university where year = 1 and students >= 30;
```
## Projection (π)

- Projection allows to specify properties to be shown.
- Done with the keyword `select [properties]`.

```SQL
select module from university;
select module, degree from university;
```

- Composition between selection and projection is possible.
```SQL
select module, degree from university where year = 1;
```
## Cartesian Product (x)



## Union (∪)
## Difference (-)
## Natural Join (⋈)