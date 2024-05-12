
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
- Pages table
	- One per process
	- Contains:
		- Number of page/frames.
		- Protection bits
		- Modified (1 if modified), present (1 if in MM) and reference b