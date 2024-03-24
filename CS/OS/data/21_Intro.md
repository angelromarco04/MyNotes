---
Author: AAM
Date: 2024-03-24
tags:
  - ComputerScience
  - OperatingSystems
---
# Introduction to Operating Systems

[Back to index](../OS.md)

1. [Definition of an operating system (OS)](#definition-of-an-os)

---
## Interrupts
### Definition
- Interruptions always arrive at the CPU to stop current execution.
- Each interruption is identified by an integer number.
- There exists a table: **Interruptions Vector**.
	- Associates each interrupt number with the address of its subroutine.
	- This table is located in the lower addresses of the main memory.
### Execution Steps
1. An interruption is generated.
2. CPU ends execution of current instruction.
3. CPU registers are saved to the stack.
4. CPU switches to supervisor mode.
5. Address stated by the interrupt vector is loaded to the Program Counter (PC).
6. The interruption management subroutine is executed. 

### Interrupt Ending
- Every interruption subroutine ends with the `iret` statement.
	1. CPU switches to user mode.
	2. Information is recovered from the stack and loaded to the CPU registers.
	3. CPU continues running previously stopped process.

---
## OS Process Management



---
## Definition of process



---
## Image of a process



---
## Process execution with interrupts



---