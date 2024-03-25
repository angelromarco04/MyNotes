---
Author: AAM
Date: 2024-03-25
tags:
  - ComputerScience
  - OperatingSystems
---
---
# STS Scheduling Algorithms

[Back to index](../OS.md)

---
## Understanding metrics

- `P` is the **Process ID**.
- `Ta` is the **Time of Arrival** to the scheduler.
- `CPU-(E/S)` is the sequence of **CPU and IO usage**.
- `Ts` is the **Time of Service** (CPU time + IO time).
- `Te` is the **Time of Ending** of the process.
- `Tnrd` is the Turnaround Time (Total time from arrival to completion)
- `Tnnrd` is the Normalized Turnaround Time (`Tnrd` divided by `Ts`)
- `Tw` is the Time Waiting (Total time waiting at the `ready` queue)

---
## First Come First Served

- The `ready` queue is a FIFO queue.
	- It is ordered by arrival time to this step.
- The head of the queue is selected for the `running` state.
- The `running` process cannot be interrupted nor removed (non-preemptive).

---
## Non-Preemptive Static Priority



---
## Preemptive Static Priority



---
## Round-Robin + FCFS



---
## Multiple level queues without feedback



---
## Multiple level queues with feedback