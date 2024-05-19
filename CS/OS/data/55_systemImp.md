
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
- FDB contains a fixed number of block numbers.
- Some of this blocks contain other block numbers (indirect access).
- Problems:
	- Limited file size. by the index.
	- Access time depends on indirection level.

---
## Folder implementation

- FDB must be reachable by its name.
### MS-DOS Implementation:
- File name (8B)
- Extension (3B)
- Attributes (1B)
- Reserved (10B)
- Time (2B) & Date (2B)
- First block number (2B)
- Size (4B)
### UNIX folder implementation:
	- FDB resides in a specific area and is called i-node.
	- Each i-node is identified by a integer (file ID).
	- i-node example:
		- i-node number (2B)
		- File name (14B)
---
## Free space management



---
## File system consistency



---