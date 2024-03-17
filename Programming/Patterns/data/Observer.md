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

- Subject notifies Observers when there is a change.
- Notified Observers change accordingly to its associated Subject

## UML

```mermaid
classDiagram
direction TB

Main .. Subject
Main .. Observer

Subject <|-- ConcreteSubject
Observer <|-- ConcreteObserver

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

class ConcreteSubject {
		<< C >>
		- subjectState
	}

class ConcreteObserver {
	<< C >>
	- observerState
}

```
## Code

```java
public class ConcreteSubject { 

}
```