---
Author: AAM
Date: 2024-03-17
tags:
  - "#programming"
  - DB
---

---
# Entity/Relationship Model

[Back to index](../../DATABASES.md)

---

## Entity vs Attribute

- Entries are defined by a set of attributes.

```mermaid
flowchart TD
	id1---id2
	id1---id3
	id1---id4

	id1["`**Car** *(Entity)*`"]
	id2(["`**ID** *(Attribute)*`"])
	id3(["`**Brand** *(Attribute)*`"])
	id4(["`**Model** *(Attribute)*`"])
```
## Types of Attributes

- Simple or Composite (Formed by several simple ones).
- Single-valued (Simple circle) or Multi-valued (Double circle).
- Derived (Dotted circle) or not.
- Null or not.

## Relations

- Represented with a diamond shape.
- Degree:
	- Binary (Two entities. Common one)
	- Reflexive (Entity associated with itself)
	- N-ary ()