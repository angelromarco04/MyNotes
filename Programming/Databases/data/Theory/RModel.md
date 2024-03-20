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
### 1:1 Relations

```mermaid
flowchart LR
	id2 --> id1
	id2 --> id3

	id1["`**Student**`"]
	id2{"`*have*`"}
	id3["`**Account**`"]
```

```Relational
# Option 1
Student = (@idStudent, idAccount (FK to Account) (Unique))
Account = (@idAccount)

# Option 2
Student = (@idStudent)
Account = (@idAccount, idStudent (FK to Student) (Unique))
```

### 1:N Relations

```mermaid
flowchart LR
	id2 -- ( 1 .. N ) --- id1
	id2 -- ( 1 .. 1 ) --> id3

	id1["`**Student**`"]
	id2{"`*enroll*`"}
	id3["`**Bachellor**`"]
```

```Relational
Student = (@idStudent, idBachellor (FK to Bachellor))
Bachellor = (@idBachellor)
```

### N:N Relations

```mermaid
flowchart LR
	id2 -- ( 1 .. N ) --- id1
	id2 -- ( 1 .. N ) --- id3

	id1["`**Student**`"]
	id2{"`*takes*`"}
	id3["`**Course**`"]
```

```Relational
Student = (@idStudent)
Bachellor = (@idBachellor)

Enroll = ( @[
	idStudent (FK to Student),
	idBachellor(FK to Bachellor)
])
```

### Reflexive 1:1 Relations
```mermaid
flowchart LR
	id2 ---> id1
	id2 ---> id1

	id1["`**Category**`"]
	id2{"`*has*`"}
```
```Relational
Category = (@idCategory, idCategory (FK to Category) (Unique) )
```


### Reflexive 1:N Relations
```mermaid
flowchart LR
	id2 -- ( 1 .. N ) --- id1
	id2 -- ( 1 .. 1 ) --> id1

	id1["`**Category**`"]
	id2{"`*has*`"}
```
```Relational
Category = (@idCategory, idCategory (FK to Category) )
```

### Reflexive N:N Relations
```mermaid
flowchart LR
	id2 -- ( 1 .. N ) --- id1
	id2 -- ( 1 .. N ) --- id1

	id1["`**Category**`"]
	id2{"`*has*`"}
```
```Relational
Category = (@idCategory)
Has = ( @[
	idCategory (FK to Category),
	idCategory (FK to Category)
])
```

### Multidirectional N:N:N Relations
```mermaid
flowchart LR
	id2 -- ( 1 .. N ) --- id1
	id2 -- ( 1 .. N ) --- id4
	id2 -- ( 1 .. N ) --- id3


	id1["`**Teacher**`"]
	id2{"`*teaches*`"}
	id3["`**Bachellor**`"]
	id4["`**Classroom**`"]
```
```Relational
Teacher = (@idTeacher)
Bachellor = (@idBachellor)
Classroom = (@idClassroom)

Teaches = (
	@[
		idTeacher (FK to Teacher)
		idClassroom (FK to Classroom)
		idBachellor (FK to Bachellor)
	],
)
```
### Multidirectional N:1:N Relations
- The N related are considered PK.
- The 1 related are considered just FK
```mermaid
flowchart LR
	id2 -- ( 1 .. N ) --- id1
	id2 -- ( 1 .. N ) --- id4
	id2 -- ( 1 .. 1 ) --> id3

	id1["`**Teacher**`"]
	id2{"`*teaches*`"}
	id3["`**Bachellor**`"]
	id4["`**Classroom**`"]
```
```Relational
Teacher = (@idTeacher)
Bachellor = (@idBachellor)
Classroom = (@idClassroom)

Teaches = (
	@[
		idTeacher (FK to Teacher)
		idClassroom (FK to Classroom)
	],
	idBachellor (FK to Bachellor)
)
```

### Multidirectional N:1:1 Relations
```mermaid
flowchart LR
	id2 -- ( 1 .. N ) --- id1
	id2 -- ( 1 .. 1 ) --> id4
	id2 -- ( 1 .. 1 ) --> id3


	id1["`**Teacher**`"]
	id2{"`*teaches*`"}
	id3["`**Bachellor**`"]
	id4["`**Classroom**`"]
```
```Relational
Teacher = (@idTeacher)
Bachellor = (@idBachellor)
Classroom = (@idClassroom)

Teaches = (
	@[
		idTeacher (FK to Teacher)
		idClassroom (FK to Classroom)
	] (Unique),
	idBachellor (FK to Bachellor)
)
```

## Weak entities
