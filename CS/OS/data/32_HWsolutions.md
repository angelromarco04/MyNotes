---
Author: AAM
Date: 2024-03-28
tags:
  - ComputerScience
  - OperatingSystems
---
---
# Hardware solutions to mutual exclusion

[Back to index](../OS.md)

---
## Disabling Interruptions

- In mono-processor computer processes are interleaved
	- Processes are only disrupted because of interruptions.
	- Disable interruptions during critical sections to solve *Mutual Exclusion*.
- Cons:
	- OS cannot get to the CPU.
	- Processes interleaving rate is degraded. 
	- Useless for multicore architectures.

---
## Special Machine Instructions



---