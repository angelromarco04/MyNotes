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

```mermaid
```

## UML

```mermaid
classDiagram
direction TB
Component <|-- Leaf
Component <|-- Composite
Composite *--> Component : 1..n

class Component {
	<< I >>
	+ operation() void
}

class Leaf {
	<< C >>
	+ operation() void
}

class Composite {
	<< C >>
	- List~Component~ children
	+ add() void
	+ remove(int pos) void
	+ operation() void
}
```
## Code

```java
public class Class { 

}
```