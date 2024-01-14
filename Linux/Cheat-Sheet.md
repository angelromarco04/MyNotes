# Basic
## Managing Directories
- `pwd` → Print Working Directory.
- `ls` → List (show files inside a directory)
- `cd` → Change Directory.
- `mkdir` → Make Directory.
- `rmdir` → Remove Directory.

## Managing files
(Note that everything is considered a file, including directories)

- `file <x>` → Displays the type of file of `x`.
- `rm <x>` → Remove the file `x`.
- `touch <x>` → Create an empty file called `x`.
- `cp <x> <y>` → Copy file `x` to a new one called `y`.
- `mv <x> <y>` → Move or/and rename file `x` to `y`.

## Read/Write files
- `head <x>` → Displays the first lines of the file `x`.
- `tail <x>` → Displays the last lines of the file `x`.
- `cat <x>` → Displays contents of file `x` in the terminal.
- `nano <x>` → Opens a in-terminal editor for `x`.

## Managing users

- `whoami`

## Permissions

- `sudo` → Super User do (privileged level)

## System Info

- `uptime` → Shows how much time the system has been running.
- `ifconfig` → Info about network interfaces.
- `lscpu` → Info about processor.
- `cat /proc/cpuinfo` → Info about processor.
- `cat /proc/meminfo` → info about RAM
- `free` → Current RAM usage (static).
- `top` → Dynamic RAM usage per task.

## Help & others

(Usually the inline argument `--help` is provided)

- `man <x>` → Obtain help about `x` command.
- `man 3 <x>` → Obtain help about `x` function in c.
- `reboot` → Reboot the system.
- `shutdown` → Shut down the system.
- `poweroff` → Power off the system.
- `echo <x>` → Displays x in the terminal.
- `<x> > <y>` → Stores output of command `x` to file `y`.
- `clear` → Cleans the terminal.
