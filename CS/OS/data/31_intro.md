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
	- *Mutual Exclusion* problem.
1. Sharing cooperation among processes
	- Processes cooperate to share resources without knowing each others.
	- Programmer is responsible of controlling cooperation.
		- OS provides system calls.
	- *Mutual Exclusion* problem.
1. Communication cooperation among processes
	- Processes send messages (synchronize) between them.
	- Programmer is responsible of communication.
		- OS provides services for sending and receiving.
	- No *Mutual Exclusion* problem.

---
## The problem of mutual exclusion



---