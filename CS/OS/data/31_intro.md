---
Author: AAM
Date: 2024-03-28
tags:
  - ComputerScience
  - OperatingSystems
---

---
# Introduction to Processes Coordination

[Back to index](../OS.md)

---
## Principles of concurrency

- **Concurrent processes**: interleave or overlap its execution.
- **Parallel processes**: overlap its execution.
- **Concurrency and parallelism**
	- Multi-programming (mono-processor)
		- No real parallelism. Processes interleave.
	- Multi-processing and distributed (several CPUs)
		- Real parallelism. Processes interleave and overlap.
- **Concurrency Problems**
	- Shared global resources.
	- Processes synchronization.
	- Inefficient resource assignment.
	- Difficult programming error identification (not repeatable scenarios)

---
## Classification of processes interaction

1. Contest among processes
	- Independent processes trying to access same resource.
	- OS is responsible of resources assignment.
2. Sharing cooperation among processes
	- Processes cooperate without knowing each others.
	- Programmer is responsible of controlling cooperation (use sys. calls).
3. Communication cooperation among processes
	- Processes send messages between them.

---
## The problem of mutual exclusion



---