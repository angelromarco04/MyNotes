
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
### Definitions

- Processes are identified by an unique integer ID (PID)
- In UNIX there are some special process always running:
	- **Swapper** (PID 0) is responsible of dumping pages to disk.
	- **Init** (PID 1) is responsible of loading other processes on boot.
		- Tree-like hierarchy with `init` as root.
- Every orphan process is set as a children of `init`

- Each process also has other identification:
	- User ID (UID)
		- **Owner user** (User that created the process)
		- **Effective user** (User whose priviledges is using the process)
	- Group ID (GID)
		- **Owner group** (Group that created the process)
		- **Effective group** (Group whose privileges is using the process)
- The superuser (root) has all privileges and always has the UID 0.
### Usage
```cpp
#include <iostream>
#include <sys/types.h>
#include <unistd.h>

// Information we get is relative to the process running this code.

int main() {
	pid_t var_pid; // Datatype to store PIDs.
	var_pid = getpid(); // Get the PID.
	var_pid = getppid(); // Get the parent PID.
	
	uid_t var_uid;  // Datatype to store UIDs.
	var_uid = getuid(); // Get the owner UID
	var_uid = geteuid(); // Get the effective owner UID
	
	gid_t var_gid; // Datatype to store GIDs.
	var_gid = getgid(); // Get the owner GID
	var_gid = getegid(); // Get the effective owner GID
}
```

---
## Process Environment



---
## Process Creation



---
## Process Termination



---