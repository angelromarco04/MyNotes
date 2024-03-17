---
Author: AAM
Date: 2024-03-16
tags:
  - programming
  - other
---
---
# State

[Back to index](../PATTERNS.md)

---

## Description

Allows to modify the behaviour of an object depending on a internal state.

## Characteristics

- 

## UML

```mermaid
classDiagram
Context --o State
State <|-- State1
State <|-- State2

class Context {
	<< C >>
	- State state
	+ goNext() void
	+ setState(State) void
}

class State {
	<< I >>
	+ goNext() void
}
```
## Code

```java
public class Class { 

}
```