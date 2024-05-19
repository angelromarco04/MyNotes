
---
# File system implementation

[Back to index](../README.md)

---
## File system structure

- A file system is a way of organizing files in the secondary memory (SM).
- Disk is divided in:
	- MBR (lower disk positions)
	- Partition table (just after MBR)
	- Several partitions each with a file system (can be de same or not). 
- Each file system has its own format:
	- Boot block, super block, free space management, root directory...
	- Block size may vary (1kB to 4KB normally).

---
## File implementation

- Files are stored in data blocks in SM.
- Data blocks of the same file may not be adjacent.
- To access them seImplementation 

---
## Folder implementation



---
## Free space management



---
## File system consistency



---