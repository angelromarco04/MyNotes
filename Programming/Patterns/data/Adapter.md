---
Author: AAM
Date: 2024-03-16
tags:
  - programming
  - other
---

## Description

Allows the use of one or more classes as if they were of another class.

## Characteristics

- We implement an adapter class.
	- It inherits from the objective class.
	- It contains an instance of the adaptable class.
	- We implement each method using the adaptable class.

## UML

```mermaid
classDiagram
direction LR

Objective <|-- Adapter
Adapter --* Adaptable

class Objective {
	<< I >>
	+ operation() void
}

class Adapter {
	<< C >>
	- Adaptable adaptable
	+ operation() void
}

class Adaptable {
	<< I >>
	+ otherOperation() void
}
```
## Code

```java
public class Objective { 
	public void operation() { ... }
}

public class Adapter { 
	public void operation() { ... }
}

```