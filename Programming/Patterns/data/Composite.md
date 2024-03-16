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
flowchart TD

Composite1[Composite]
Composite2[Composite]
Leaf1(Leaf)
Leaf2(Leaf)
Leaf3(Leaf)
Leaf4(Leaf)
Leaf5(Leaf)

subgraph 1 [ ]
Composite1 --> Leaf1
Composite1 --> Leaf2
Composite1 --> Composite2
Composite1 --> Leaf3

subgraph 2 [ ]
Composite2 --> Leaf4
Composite2 --> Leaf5
end
end
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
public class Component { 
	public void operation()
}
```