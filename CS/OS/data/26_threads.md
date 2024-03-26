---
Author: AAM
Date: 2024-03-26
tags:
---
---
# Threads

[Back to index](../OS.md)

---

## Introduction

- OS manages differently:
	- Process (Resource owner unit, do not run)
	- Thread (minimal scheduling running unit)
- Processes  are composed of one or more threads.
- Multithread OS allows processes to use several threads.

---
## Composition in Main Memory

- Processes
	- Have the PCB loaded to main memory.
	- Have at least one running thread (main thread)
	- Do never execute code.
	- PCB without some parts.
- Threads
	- Have a *mini PCB* called Thread Control Block (TCB)
		- Thread state and context.
	- Access to memory and resources that belong to their process
	- Resoruces are shared 

---
## Process and Thread Creation



---
## Process and Thread Management



---
## Process and Thread Ending



---
## Benefits of Threads



---
## Use Examples