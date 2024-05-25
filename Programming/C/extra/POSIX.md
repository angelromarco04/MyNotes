
---
# POSIX standard

[Back to index](../CS/OS/README.md)

---
## Introduction
- To perform a system call we require assembly.
- Parameters passed by:
	- Each parameter to a CPU register.
	- Parameters in memory block and address to CPU register.
	- Using the stack (usually this one).
- To simplify this an API (library) was created:
	- POSIX = Portable Operating System Interface
- To use this API:
```Cpp
#include <iostream>
#include <sys/types.h>
#include <unistd.h>
```
---
## Process identification
### Obtaining process' PID
- Processes are identified by an unique integer ID (PID)
```cpp
pid_t var_pid; // Datatype to store PIDs.
var_pid = getpid(); // Get the PID.
var_pid = getppid(); // Get the parent PID.
```
- In UNIX there are some special process always running:
	- **Swapper** (PID 0) is responsible of dumping pages to disk.
	- **Init** (PID 1) is responsible of loading other processes on boot.
		- Tree-like hierarchy with `init` as root.
- Every orphan process is set as a children of `init`
### Obtaining process UID
- User ID (UID)
	- **Owner user** (User that created the process)
	- **Effective user** (User whose priviledges is using the process)
```cpp
uid_t var_uid;  // Datatype to store UIDs.
var_uid = getuid(); // Get the owner UID
var_uid = geteuid(); // Get the effective owner UID
```
- The superuser (root) has all privileges and always has the UID 0.
### Obtaining process GID
- Group ID (GID)
	- **Owner group** (Group that created the process)
	- **Effective group** (Group whose privileges is using the process)
```cpp
gid_t var_gid; // Datatype to store GIDs.
	var_gid = getgid(); // Get the owner GID
	var_gid = getegid(); // Get the effective owner GID
```
### Changing Process Identification
- All of this functions:
	- Throw an error if the provided UID/GID is not valid.
	- Return `0` if the operation is correctly performed and `-1` otherwise.
- When superuser invokes `setuid()` or `setgid()` it changes both fields.
	- When a process loose superuser privileges it cannot get them back.
```cpp
int setuid (uid_t uid); // Change owner UID
int setgid (gid_t gid); // Change owner GID

int seteuid (uid_t euid); // Change effective owner UID
int setegid (gid_t egid); // Change effective owner GID
```
---
## Process Environment
## Environment Variables
- When a process starts some variables are created.
	- `HOME`: Initial working directory of the user.
	- `LOGNAME`: User name in the login.
	- `PATH`: Folders with executable files.
	- `SHELL`: Default command interpreter.
### Usage
```cpp
#invlude <stdlib.h>

char *getenv (const char *name);
int putenv (const char *string);
```
---
## Process Creation



---
## Process Termination



---