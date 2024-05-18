
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
	- Copy of the FDB (actual copy or pointer to the FDB table)
	- Reading/writing pointer (pointer to a R/W memory position)
	-  # processes sharing (-1 if no sharing)
- New entry is always created if:
	- Different file (FDB)
	- Same file but R/W pointers are not shared.
	- Same file but different mode.
- Opening modes: read (R), write (R) or read/write (R/W)

---
## FDB table in the M.M.

- One for the whole system.
- Contains a copy in MM of the opened files FDB.
	- Also contains the number of references to it.
	- If this number reaches 0 the entry is freed.
- Avoids storing several copies of the same FDB in MM.
- Not every OS implements it.


---
## Process’ open file table

- Stores information about about files opened by each process.
- Stored in MM.
- Contains:
	- pointer to system open file table
	- Can also store R/W pointer.

---
## System calls for files management

- **Create file**
	1. Create a new FDB.
	2. Set initial values in the FDB.
- **Delete file**
	- File and its FDB are removed.
- **Open file**
	1. 

---
## System calls for directories management



---