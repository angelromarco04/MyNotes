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

	id1["Entity"]
	id2(("Attribute1"))
	id3(("Attribute2"))
	id4(("Attribute3"))
```
## Types of Attributes

- Simple or Composite.
- Single-valued or Multi-valued.
- Derived or not.
- Null or not.