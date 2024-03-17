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

Client .. Receiver :use
Client .. ICommand :use
subdiagram
ICommand <|-- Order1
ICommand <|-- Order2
end

class Receiver {
	<< C >>
	+ operation1()
	+ operation2() 
}

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

```
## Code

```java
public class Client { 
	public void main(String[] args) {
		Receiver receiver = new Receiver();
	}
}
```