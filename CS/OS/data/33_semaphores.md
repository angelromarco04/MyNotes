---
Author: AAM
Date: 2024-03-29
tags:
---
---
# Semaphores

[Back to index](../OS.md)

---

## Definition of semaphore

- Processes cooperates through signals.
	- Processes wait until a signal is received
- Special variables called semaphores (`s`) are used.
	- To send a signal `V(s)` or `signal(s)` (releases a process).
	- To receive a signal `P(s)` or `wait(s)` (blocks a process).
- Implementation:
	- Semaphores are integer variables initialized with a non-negative value.
	- Operation `V` increases the value of a semaphore.
	- Operation `P` decreases the value of a semaphore.
- Types:
	- General or counting (any value)
	- 

---
## Solution to the mutual exclusion problem



---
## Solution to synchronization problems



---
## Problems derived from the misuse of semaphores



---
## The producers/consumers problem



---
## The readers/writers problem



---