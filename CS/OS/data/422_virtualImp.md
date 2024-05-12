
---
# Virtual Memory Implementation
[Back to index](../index.md)

---
## Introduction
There are several ways of implementing Virtual Memory:
- **Paging** (Only one explained here)
- **Segmentation**
- **Paged Segmentation**

---
## Paging
### Organization of the Memory
- Process is divided into fixed-size blocks called pages.
- MM is divided into fixed-size blocks called frames.
- Pages and frames are of the same size.
### Data Structures
- **Pages table**
	- One per process
	- Contains:
		- Page number.
		- Protection bits.
		- Modified bit (1 if modified).
		- Present bit (1 if in MM).
		- Reference bit  (1 if referenced recently).
- File map table
	- Address of the processes in secondary storage.
- Frames table (as in simple paging)
	- Only one for whole system.
	- Has an entry for each frame (assigned/free, page number, PID)
### Address translation
1. Divide the virtual address into page number and offset.
2. Access the page table of the process.
	- Try to translate the page number to a frame number.
	- If present bit is set to 0 throw a Page Fault Exception.
		1. OS takes control to locate page in secondary memory.
		2. Loads to MM the 
1. Access the MM with the physical address.
	- physical address = frame number +offset.
	- Locate the frame number and the offset inside it.