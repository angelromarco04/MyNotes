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
```sh
var1= "abc"
```

# Comments
```sh
# This is a comment
# This is also a comment
echo Hello World # This is a another comment
```

# Expressions

- Expressions return `0` as `true` or any other value as `false`.

```sh
# Alternative 1
test $var -eq 0

# Alternative 2
[$var -eq 0]
```

### Numerical values
- `N -eq M` → $N = M$`
- `N -ne M` →  $N \ne M$
- `N -gt M` → $N > M$`
- `N -lt M` → $N < M$`
- `N -ge M` → $N \ge M$`
- `N -le M` → $N \le M$`

### File types
- `-s file` → Check if file exists and if it is non-empty.
- `-f file` → Check if file exists and if it is normal.
- `-d file` → Check if file is a directory.
- `-w file` → Check if file is writable.
- `-r file` → Check if file is readable.
- `-x file` → Check if file is executable.
### String values
- `S = R` → Check if S is equal to R.
- `S != R` → Check if S is not equal to R.
- `-z S` → Check if length of S is `0`.
- `-n S` → Check if length of S is not `0`.
# If-else

```sh
if text $var -eq 3
then ...
elif ...
else ...
fi

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