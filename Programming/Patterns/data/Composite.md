---
Author: AAM
Date: 2024-03-16
tags:
  - programming
  - other
---
---
# Title

[Back to index](../PATTERNS.md)

---

## Description

Allows to treat groups of objects as if they were a single object.
Similar to a tree data structure.

## Characteristics

- 

## UML

```mermaid
classDiagram
direction TB
Component <|-- Leaf
Component <|-- Composite

class Component {
	<< I >>
	+ operation void
}

class Leaf {
	<< C >>
	+ operation void
}

class Composite {
	<< C >>
	+ operation void
}
```
## Code

```java
public class Class { 

}
```