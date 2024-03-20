---
Author: AAM
Date: 2024-03-20
tags:
  - "#programming"
  - DB
---

---
# Relational Model

[Back to index](../../DATABASES.md)

---

## Basic Notions

- Both attributes and relations are represented by tuples.
- Tuples are represented with parenthesis.
- Values are separated by commas.

## Attributes

- In composite attributes only appears the values that compose the attribute.
- Derived attributes are omitted.

```Relational
# Primary Keys start with @
Student = (@id, name)
Book = (@[ISBN, version], name)

# Foreign Keys must be specified
Student = (@id, idCourse (FK to Course))

#  Multi value attributes are represented apart
Course = (@id)
Places = (@[idDate, idCourse (FK to Course)], name)
```

## Relations

