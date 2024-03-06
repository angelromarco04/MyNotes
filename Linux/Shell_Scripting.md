---
Author: AAM
Date: 2024-03-06
tags:
  - linux
---
---

# Variables
- There are no datatypes.
- Accessing a non-existing value returns `null`.
- There are some global variables
	- `$HOME` working directory of the user.
	- `$PATH` path where the shell looks for commands.

# Comments
```sh
# This is a comment
# This is also a comment
echo Hello World # This is a another comment
```

# Expressions

- Expressions return a boolean value

```sh
# Alternative 1
test 
# Alternative 1
```
# Parameters
```sh
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