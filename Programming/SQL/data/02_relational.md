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

- Done in two ways:
	- With the keyword `inner join ... on`:
		`select [properties] from [table1] inner join [table2] on [relation]`
	- With the keyword `where`:
		`select [properties] from [table1], [table2] where [relation]`

```SQL
select u.module, t.name from university u, teacher t where u.code = t.code; 2

select u.module, t.name from university u inner join teacher t on u.code = t.code;
```

## Union (∪)

- Done with the keyword `[query1] union [query2]`.
```SQL
-- All people in the campus. Both students and professors.
(select * from students) union (select * from professors)
```

## Difference (-)

- Done with keyword `[query1] except [query2]`.
```SQL
-- Modules which are not teach by any teacher.
(select module from university) except (select module from professors)
```
## Natural Join (⋈)


p18 - renaming