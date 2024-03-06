---
Author: AAM
Date: 2024-03-06
tags:
  - linux
---
---

# Variables
- There are no datatypes.
- Accessing a non-existing v
# Parameters
```bash
$promt> <filename> <arg1> <arg2> ...
```

- Params. can be accessed with `$i` being `i` the param number (`$1`, `$2).
- `$0` is always the filename.
- `$#` is the number of arguments specified.
- `shift` command removes the first arg and re-enumerates.
- `$*` is a string containing all specified args (`"arg1 arg2 arg3"`)
	- Unexpected behaviour if special characters or spaces.
	- `$@` must be instead.



- `$?` exit status of last command
- `$$` process number of current shell
