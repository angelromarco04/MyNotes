---
Author: AAM
Date: 2024-03-16
tags:
  - programming
  - other
---
---
# Observer

[Back to index](../PATTERNS.md)

---

## Description

Allows to modify several objects (Observers) based on changes in other object (subject).

## Characteristics

- 

## UML

```mermaid
classDiagram


Subject <|-- ConcreteSubject
Observer <|-- ConcreteObserver
Subject ..> Observer : notify
ConcreteObserver ..> ConcreteSubject

namespace Interfaces {

	class Subject {
		<< I >>
		+ add(Observer)
		+ remove(Observer)
		+ notify()
	}

	class Observer {
		<< I >>
		+ setSubject(Subject)
		+ update()
	}
}

```
## Code

```java
public class Class { 

}
```