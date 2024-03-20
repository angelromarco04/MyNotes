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

## 1:1 Relations

```mermaid
flowchart LR
	id2 --> id1
	id2 --> id3

	id1["`**Student**`"]
	id2{"`**have**`"}
	id3["`**Account**`"]
```

```Relational
Student = (@idStudent, name)
Account = (@idAccount, info)

# Option 1
Have = (@idStudent (FK to Student), idAccount(FK to Account)(Unique))

# Option 2
Have = (@idAccount(FK to Account), idStudent (FK to Student)(Unique))
```

## 1:N Relations

```mermaid
flowchart LR
	id2 -- ( 1 .. N ) --- id1
	id2 -- ( 0 .. 1 ) --> id3

	id1["`**Student**`"]
	id2{"`**enroll**`"}
	id3["`**Bachellor**`"]
```

```Relational
Student = (@idStudent, name)
Bachellor = (@idBachellor, description)

# Option 1
Enroll = (@idStudent (FK to Student), idBachellor(FK to Bachellor))
```

## N:N Relations

```mermaid
flowchart LR
	id2 -- ( 1 .. N ) --- id1
	id2 -- ( 1 .. N ) --- id3

	id1["`**Student**`"]
	id2{"`**takes**`"}
	id3["`**Course**`"]
```

```Relational
Student = (@idStudent, name)
Bachellor = (@idBachellor, description)

Enroll = (@ [ idStudent (FK to Student), idBachellor(FK to Bachellor) ] )
```