
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
- To access them in order there are several implementation.
### Linked List Assignation
- FDB contains only the block number (address) of the file's first block.
- Each block contains the block number of that file's next block.
- Problems:
	- Inefficient direct access, only sequential.
	- Space waste in each block.
### Linked List Assignation using a Table
- There is a table that contains:
	- One entry per block (index = block number)
	- For each entry the block number of the block of a file.
- Advantages:
	- Easier direct access.
	- Whole block used for data.
	- Faster if all table is loaded to MM.
### Indexed assignation


---
## Folder implementation

- 

---
## Free space management



---
## File system consistency



---