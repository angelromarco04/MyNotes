# Basic
## Managing Directories
- `pwd` → Print Working Directory.
- `ls` → List (show files inside a directory)
- `cd` → Change Directory.
- `mkdir` → Make Directory.
- `rmdir` → Remove Directory.
- `find <folder>`

## Managing files
(Note that everything is considered a file, including directories)

- `file <file>` → Displays the type of the file.
- `rm <file>` → Remove the file.
- `touch <file>` → Create an empty file.
- `cp <file1> <file2>` → Copy `file1` to a new one called `file2`.
- `mv <file1> <file2>` → Move or/and rename file1 to file2.

## Read/Write files
- `head <file>` → Displays the first lines of the file.
- `tail <file>` → Displays the last lines of the file.
- `cat <file>` → Displays contents of file in the terminal.
- `nano <file>` → Opens a in-terminal editor.
- `cut <file>` → Each line of the file is cut using a delimiter.
- `wc <file>` → Counts lines, bytes, characters... in a file.
## Managing strings
- `echo <string>` → Displays `string` in the terminal.
- `grep <string> <file>` → Searches `string` in the `file`.
## Managing users

- `whoami`

## Managing processes

- `ps` → Shows running processes.
- `kill <pid>` → Kills processes by its Process ID.
## Permissions

- `sudo` → Super User do (privileged level)

## System Info

- `date` → Shows current date.
- `uptime` → Shows how much time the system has been running.
- `lscpu` → Info about processor.
- `cat /proc/cpuinfo` → Info about processor.
- `cat /proc/meminfo` → info about RAM
- `free` → Current RAM usage (static).
- `top` → Dynamic RAM usage per task.
- `htop` → Better representation of `top` command.
- `df` → Shows disk usage.
- `lsblk` → Shows block devices (disk partitions).

## Networking
- `ifconfig` → Info about network interfaces.
- `ip` → Newer version of `ifconfig`.

## Package Manager
- `apt` → Advanced Package Manager (Debian)

## Help & others

(Usually the inline argument `--help` is provided)

- `man <x>` → Obtain help about `x` command.
- `man 3 <x>` → Obtain help about `x` function in c.
- `reboot` → Reboot the system.
- `shutdown` → Shut down the system.
- `poweroff` → Power off the system.
- `<x> > <y>` → Stores output of command `x` to file `y`.
- `clear` → Cleans the terminal.
