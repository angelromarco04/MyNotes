
---
# Virtual Memory Management Policies

[Back to index](../index.md)

---
## Introduction
- Software required to manage virtual memory (part of the OS).
### Reading policies
- When do we need to load a page to MM?
- **On Demand Paging**
	- Pages are loaded to MM when referenced by the CPU
	- Principle of locality reduces page faults.
	- On Pure Demanding Paging processes start with no page at MM.
- **Previous Paging**
	- More than one page loaded in a single page fault.
	- This was never proven.
### Location Policies
- Where do we need to load a page to MM?
- For paging location is not important.

---
## Resident Set Management
### Definition
- Set of pages of a process loaded to the MM.
- OS determines this set size
- Small size $\implies$ More processes in MM but higher page fault rate per process.
### Assignment Policies
- Assign the maximum number of used frames per process.
- Low # frames $\implies$ hyper-paging (# pages $>>$ # frames) $\implies$ High page fault rate
---