
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
## Event Based Systems (EBS) Interactions
### Definition
- A system is a set of agents that:
	- Change their behaviour depending on its state.
	- Interact between them in several ways (events).
- The system state is the state of all the agents at a specific time.
- A EBS is discrete if:
	- It has a finite set of states and changes.
	- Every state has a next state.
### Request-Response Interaction
- Involves only two agents.
- Response is mandatory.
```mermaid
sequenceDiagram
    participant A
    participant B
    A->>B: Request (+details)
    B->>A: Response
```
### Message passing Interaction
- Involves only two agents.
- Response is optional.
```mermaid
sequenceDiagram
    participant A
    participant B
    A->>B: Request (+details)
    B-->>A: Response (optional)
```
### Publication-Subscription Interaction
- Involves multiple agents.
- Several B agents subscribe to A.
- Several A agents publish several types of messages.
- B agents receive messages from A agents if they are subscribed.
---
## The EDP Paradigm
### Event Model
- EDP is a paradigm whose core are the events.
- Objects linked to events:
	- Event Source. Generates the event.
	- Event Objects. Encapsulates event data.
	- Event Handler. Responses to the event.
### Events vs method calls
1. Event source and handler have a weaker coupling (independence).
2. Event handlers can be connected to several events at different times.
3. Events can have 0 or more handlers.
4. Event handlers does not return any value.
5. Same handler can control events from different sources.
6. Event sources (usually) do not need to wait for the handler to finish.
7. Events can be handled with delay.
---
## EDP Design
### Event response
- Event handlers can have:
	- A unique response algorithm.
	- Different responses depending on the system state.
- Some events can be an Action Not Allowed (ANA) for specific states.
### EBS representation
- **State graph** represents the states, the events and the allowed changes.
```mermaid
graph LR
A((State 0)) -- event A --> B((State 1))
B((State 1)) -- event B --> A((State 0))
B((State 1)) -- event A --> C((State 2))
C((State 2)) -- event B --> B((State 1))
C((State 2)) -- event C --> D((State 3))
A((State 0)) -- event C --> D((State 3))
```
- **State table** is the table representation of the state graph.

| State | event A | event B | event C |
| :---: | :-----: | :-----: | :-----: |
|   0   |    1    |   ANA   |    3    |
|   1   |    2    |    0    |   ANA   |
|   2   |   ANA   |   ANA   |    3    |
|   3   |   ANA   |   ANA   |   ANA   |

- Actions table provides a description of what each event does in each state.
---
## Events Infrastructure
pg 34