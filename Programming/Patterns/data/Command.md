---
Author: AAM
Date: 2024-03-16
tags:
  - programming
  - other
---
---
# Command

[Back to index](../PATTERNS.md)

---

## Description


## Characteristics

- The receiver is the object that contains all the actions.

## UML

```mermaid
classDiagram
direction TB

Client .. Receiver 
Client .. ICommand 


ICommand <|-- Order1
ICommand <|-- Order2

class Receiver {
	<< C >>
	+ operation1()
	+ operation2() 
}

namespace Operations {
	class ICommand {
		<< I >>
		+ execute()
	}
	
	class Order1 {
		<< C >>
		+ Order1(Receiver r)
		+ execute()
	}
	
	class Order2 {
		<< C >>
		+ Order2(Receiver r)
		+ execute()
	}
}
```
## Code

```java
public class Client { 
	public static void main(String[] args) {
		Receiver receiver = new Receiver();
	}

	public static void executeAll(List<Command> commands) {
		for(Command command : comman)
	}
}
```