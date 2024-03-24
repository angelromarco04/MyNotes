---
Author: AAM
Date: 2024-03-24
tags:
  - ComputerScience
  - OperatingSystems
---
---
# Processes description

[Back to index](../OS.md)

---
## Processes Basics
### Definition

- A process is an instance of a program.
- Its different parts are stored in the main memory.
	- **Context** (Some information needed by the OS)
	- **Data**
	- **Program Code**
	- **Stack**
### Creation

- It should be created in the main memory.
- Two ways:
	- Loading program from the secondary memory.
	- Through clonation of another pre-existing process.

---
##  Control Structures of the OS

### Process Control Block (PCB)
- PCB is a OS data structure with all the critical information about a process.
- Every existing process have a PCB.
- Each OS implements the PCB differently.
- PCBs are organized in the Processes Table.
### Processes Table
- OS must keep up-to-date information about processes status.
- The processes table is an indexed vector with the processes IDs (PID).
- Contains pointers to the PCBs o the PCBs themselves.
- Always resides in the main memory.

## The process control block

