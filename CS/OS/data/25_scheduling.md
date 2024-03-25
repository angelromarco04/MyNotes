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
- `Tnrd` is the Turnaround Time (Total time from `Ta` to `Te`)
- `Tnnrd` is the Normalized Turnaround Time (`Tnrd` divided by `Ts`)
- `Tw` is the Time Waiting (`Te` minus `Ts`)

---
## First Come First Served

- The `ready` queue is a FIFO queue.
	- It is ordered by arrival time to this step.
- The head of the queue is selected for the `running` state.
- The `running` process cannot be interrupted nor removed (non-preemptive).

### Example

| P   | Ta  | CPU-(E/S)          |
| --- | --- | ------------------ |
| 1   | 0   | 4, (1), 8, (1), 1  |
| 2   | 2   | 1, (5), 3, (10), 1 |
| 3   | 4   | 2, (2), 5, (3), 1  |
| 4   | 6   | 10, (1), 8         |
```mermaid
---
displayMode: compact
---
gantt
    dateFormat X
    axisFormat %s
    
    section P1
        X       : crit, a, 0, 4
        IO      : a, 4, 5
		W       : active, a, 5, 7
		X       : crit, a, 7, 15
		IO      : a, 15, 16
		W       : active, a, 16, 33
		X       : crit, a, 33, 34
    section P2
	    W       : active, b, 2, 4
	    X       : crit, b, 4, 5
	    IO      : b, 5, 10
	    W       : active, b, 10, 30
	    X       : crit, b, 30, 33
	    IO      : b, 33, 43
	    X       : crit, b, 43, 44
	section P3
		W       : active, c, 4, 5
		X       : crit, c, 5, 7
	    IO      : c, 7, 9
	    W       : active, c, 9, 25
	    X       : crit, c, 25, 30
	    IO      : c, 30, 33
	    X       : crit, c, 42, 41
	section P4
		W       : active, d, 6, 15
		X       : crit, d, 15, 25
		IO      : d, 25, 26
		W       : active, d, 26, 34
		X       : crit, d, 34, 42

```

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