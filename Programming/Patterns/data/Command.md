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
- The Client creates a list of Commands and then executes them one by one.

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

		// Create a receiver object
		Receiver receiver = new Receiver();
		
		// Create a sequence of actions for the receiver
		List<ICommand> commands = new ArrayList<ICommand>();
		commands.add(new Order1(receiver));
		commands.add(new Order2(receiver));

		// Execute all the actions
		executeAll(commands);
	}

	public static void executeAll(List<ICommand> commands) {
		for(ICommand command : commands)
			command.execute();
	}
}
```