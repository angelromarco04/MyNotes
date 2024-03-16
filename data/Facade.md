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

Provides a unified interface to facilitate the use of one or more subsystems.

## UML

```mermaid
classDiagram
direction TB

Facade

class Facade {
	<< I >>
	+ Subsystem_A 
	+ Subsystem_B
}

class Subsystem_A {
	<< I >>
}

class Subsystem_B {
	<< I >>
}
```
## Code

```java
public class Class { 

}
```