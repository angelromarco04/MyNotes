
---
# Data structures for files management

[Back to index](../README.md)

---
## File Descriptor Block (FDB)

- Stores the information needed by the OS to manage a file.
	- Can also be a folder
	- ID, location in secondary memory, size, protection...
- Stores no actual information of the file.
- All FDB are usually stored at the beginning of the filesystem.
- Only opened files are at the MM.

---
## System open file table

- One for the whole system.
- Stores information about the opened files.
	- Copy of the FDB
	- Reading/writing pointer
	-  # processes sharing.
- 

---
## FDB table in the M.M.



---
## Process’ open file table



---
## System calls for files management



---
## System calls for directories management



---