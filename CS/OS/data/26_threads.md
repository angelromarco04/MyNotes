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
	- Are stored at main memory.
	- Formed by:
		- Code
		- Data
		- At least one running thread (main thread)
	- Do never execute code.
		- PCB without some parts (running state, context, etc).
- Threads
	- Formed by:
		- Thread Control Block (TCB) is a *mini PCB*. 
			- Contains the thread state and context.
		- Stack is unique to each thread.
	- Accesses memory and resources that belong to their process.
	- Resources are shared between threads of the same process.

---
## Process and Thread Creation

- Processes are created by the OS Long-Term Scheduler (LTS)
	- Loads runnable file from secondary memory to the main memory
	- Creates a process and its main thread.
		- Process (code, data and PCB)
		- Thread (TCB and stack)
- Extra threads must be created by the programmer.
	- Requires a system call to the OS.
	- Fast and efficient creation.
	- Threads share code and global data of the process.
	- Usually, each thread uses one par

---
## Process and Thread Management



---
## Process and Thread Ending



---
## Benefits of Threads



---
## Use Examples