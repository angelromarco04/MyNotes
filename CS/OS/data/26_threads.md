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

- Modern OS manages differently:
	- Process (Resource owner unit, do not run)
	- Thread (minimal scheduling running unit)
- Processes own threads.
- Multithread OS allows processes to have several threads.

---
## Composition in Main Memory

- Processes
	- Have the PCB loaded to main memory.
	- Have at least one running thread (main thread)
	- Do never execute code.
		- PCB without some parts (running state, context, etc).
- Threads
	- Have a *mini PCB* called Thread Control Block (TCB)
		- Contains the thread state, context and a stack.
	- Access to memory and resources that belong to their process
	- Resources are shared between threads of the same process.

---
## Process and Thread Creation

- The LTS loads runnable

---
## Process and Thread Management



---
## Process and Thread Ending



---
## Benefits of Threads



---
## Use Examples