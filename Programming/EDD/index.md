
---
# Event Driven Design

[HOME](/README.md)

---
## Event Driven Programming (EDP)
### Definition
The execution flow of the program varies depending on some events.
### Program State
- The program state is difficult to determine.
- There are usually concurrent (parallel) programs.
- There are several modules:
	- Can run a different speeds.
	- Can run simultaneously.
	- Some can not necessarily run.
	- Can have several instances running.
### Events
- Events are an observable occurrence.
- Events can happen at any instant.
- Events can be external or internal.
### Event Response
- There is an observer that responds (handles) an event.
- The observer is frequently called event handler or controller.
### Event Sources
- Some events are launched by an agent.
- The agent is called event source.
---
## Event Based Systems (EBS)
