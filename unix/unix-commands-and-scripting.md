# UNIX: Commands, Permissions, Shell Scripting, and Text Editors

This file documents key UNIX concepts, commands, file permissions, shell scripting, and text editing. It’s based on practical UNIX labs and summaries of theory covered during your studies.

---

## What Is UNIX?

- A multi-user, multitasking, command-line operating system.
- Used in cloud computing, servers, development, and embedded systems.
- Core components:
  - **Kernel**: Core of the OS, always running.
  - **Shell**: Interface between user and kernel, processes commands (e.g., Bash, C Shell).

---

## Basic Commands

| Command     | Description                            |
|-------------|----------------------------------------|
| `who`       | Show who is logged in                  |
| `whoami`    | Show your username                     |
| `date`      | Display current date and time          |
| `cal`       | Display calendar                       |
| `ls`        | List files and directories             |
| `pwd`       | Show current directory path            |
| `cd`        | Change working directory               |
| `mkdir`     | Create directory                       |
| `rmdir`     | Remove directory                       |
| `echo`      | Print message or create file           |
| `top`       | Show running processes                 |

---

## Extended File Commands

- `ls -a` : Show hidden files  
- `ls -R` : Recursive listing  
- `ls -l` : Detailed view (permissions, owner, size)  
- `mkdir dir1/dir2` : Create nested directories  
- `cd ..` : Go up one directory  
- `cd -` : Return to last directory  

---

## File Editing with `vi`

- Enter with: `vi filename`
- **Modes**:
  - Command mode (default)
  - Insert mode (press `i` or `a`)
- **Commands**:
  - `:w` : Save
  - `:q` : Quit
  - `:wq` or `ZZ` : Save and quit
  - `:q!` : Quit without saving
  - `dd` : Delete line
  - `x`  : Delete character

---

## File Viewing Commands

| Command              | Description                                 |
|----------------------|---------------------------------------------|
| `cat file.txt`       | Show contents of a file                     |
| `more file.txt`      | Page through file                          |
| `head -n 5 file.txt` | View first 5 lines                         |
| `tail -n 5 file.txt` | View last 5 lines                          |
| `stat file.txt`      | Show metadata info                         |

---

## Wildcards

| Symbol | Use                          |
|--------|------------------------------|
| `*`    | Any number of characters     |
| `?`    | Single character             |
| `[ ]`  | Match any enclosed characters|

---

## File Permissions & `chmod`

- Permission flags: `r` = read, `w` = write, `x` = execute
- Order: `[owner][group][others]` (e.g., `rw-r--r--`)
- **Absolute format**:  
  - `chmod 755 file.txt` → `rwxr-xr-x`  
  - `chmod 644 file.txt` → `rw-r--r--`
- **Symbolic format**:
  - `chmod u+x file.txt` → Add execute to user  
  - `chmod g-w file.txt` → Remove write from group

---

## Redirection and Piping

- Output:
  - `>`: overwrite → `ls -l > list.txt`
  - `>>`: append → `echo "line" >> list.txt`
- Input:
  - `<`: feed file as input
- Pipe:
  - `|`: connect commands  
    Example: `ls | wc -l`

---

## Command Sequences

- Run multiple commands:  
  `date; pwd; ls`
- Redirect grouped output:  
  `(date; pwd; ls) > info.txt`

---

## Shell Scripting

- Start with:
  ```bash
  #!/bin/sh
  # A simple script
  echo Hello
  exit
  ```
- Save as `.sh`, give permission:  
  `chmod u+x script.sh`, run with `./script.sh`

---

## Variables and Expressions

- Set: `x=10`  
- Print: `echo $x`
- Arithmetic with `expr`:
  ```bash
  result=`expr 3 + 5`
  echo $result
  ```

---

## Control Structures

### `if` Statement

```bash
if [ $x -eq 5 ]
then
  echo "x is 5"
else
  echo "x is not 5"
fi
```

### `case` Statement

```bash
case $var in
1) echo "One" ;;
2) echo "Two" ;;
*) echo "Other" ;;
esac
```

---

## Loops

### `for` Loop

```bash
for i in 1 2 3
do
  echo $i
done
```

### `while` Loop

```bash
x=1
while [ $x -le 3 ]
do
  echo $x
  x=`expr $x + 1`
done
```

### `until` Loop

```bash
x=1
until [ $x -gt 3 ]
do
  echo $x
  x=`expr $x + 1`
done
```

---
