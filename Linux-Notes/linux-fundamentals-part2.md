# Linux Fundamentals Part 2

# General Observations

- Practiced Linux commands directly inside the terminal
- Encountered and corrected command mistakes during practice
- Improved confidence navigating directories and managing files
- Became more comfortable using the Linux terminal without relying on the GUI

---

# File and Directory Navigation

## ls

```bash
ls
```

Lists files and directories.

---

## ls -l

```bash
ls -l
```

Displays detailed file information and permissions.

---

## ls -a

```bash
ls -a
```

Displays hidden files and directories.

---

## pwd

```bash
pwd
```

Displays the current working directory.

---

## cd

```bash
cd
```

Changes directories.

Examples:

```bash
cd ..
```

Moves up one directory level.

```bash
cd ~
```

Returns to the home directory.

---

# Creating Files and Directories

## mkdir

```bash
mkdir directory
```

Creates a new directory.

---

## touch

```bash
touch file.txt
```

Creates a new file or updates a file timestamp.

---

# Viewing and Editing Files

## cat

```bash
cat file.txt
```

Displays file contents.

---

## nano

```bash
nano file.txt
```

Opens a file in the Nano text editor.

---

## vim

```bash
vim file.txt
```

Opens a file in the Vim text editor.

---

# File Management

## cp

```bash
cp file.txt destination
```

Copies files.

---

## mv

```bash
mv file.txt destination
```

Moves or renames files.

---

## rm

```bash
rm file.txt
```

Removes files.

---

## rm -r

```bash
rm -r directory
```

Removes directories recursively.

---

## ln -s

```bash
ln -s file link
```

Creates a symbolic link.

---

## shred

```bash
shred file.txt
```

Securely overwrites a file before deletion.

---

# User and Permission Management

## whoami

```bash
whoami
```

Displays the current logged-in user.

---

## sudo

```bash
sudo command
```

Runs a command with superuser privileges.

---

## adduser

```bash
sudo adduser username
```

Creates a new user.

---

## passwd

```bash
sudo passwd username
```

Changes a user password.

---

## chmod

```bash
chmod +x file
```

Changes file permissions.

---

# Networking Commands

## ip a

```bash
ip a
```

Displays network interface and IP address information.

---

## ping

```bash
ping google.com
```

Tests network connectivity and DNS resolution.

---

## traceroute

```bash
traceroute google.com
```

Displays the path packets take across networks.

---

# Terminal Practice Summary

Practiced:
- file creation
- file editing
- directory navigation
- file movement
- permissions
- networking commands
- user management
- troubleshooting terminal errors

This practice improved overall confidence using the Linux terminal and understanding Linux system navigation.
