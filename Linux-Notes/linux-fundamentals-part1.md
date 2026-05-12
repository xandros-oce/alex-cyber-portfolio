# Linux Fundamentals Part 1

# Terminal

The Linux terminal is a text-based interface that allows users to interact directly with the operating system using commands.

The terminal is heavily used in:
- Linux administration
- cybersecurity
- cloud computing
- server management

---

# Common Linux Commands

## echo

```bash
echo Hello
```

Outputs text provided by the user.

---

## whoami

```bash
whoami
```

Displays the current logged-in user.

---

## ls

```bash
ls
```

Lists files and directories inside the current directory.

---

## cd

```bash
cd
```

Changes directories.

Example:

```bash
cd Documents
```

Moves into the Documents directory.

---

## cat

```bash
cat file.txt
```

Displays the contents of a file.

`cat` stands for:
Concatenate.

---

## pwd

```bash
pwd
```

Displays the current working directory.

`pwd` stands for:
Print Working Directory.

---

## find

```bash
find ~/alex-training -name "*.txt"
```

Searches for files and directories.

Example:
Searches recursively for all `.txt` files inside the `alex-training` directory.

---

## grep

```bash
grep "text" file.txt
```

Searches the contents of files for specific text or values.

---

# Recursive Searching with grep

Sometimes the information being searched for exists across multiple files and directories.

The `-R` option allows grep to search recursively through all files and subdirectories.

Example:

```bash
grep -R "password" .
```

Searches recursively inside the current directory.

---

# Shell Operators

Shell operators allow commands to be combined, redirected, or executed differently inside the terminal.

---

## &

```bash
command &
```

Runs a command in the background.

---

## &&

```bash
command1 && command2
```

Combines multiple commands together on one line.

The second command only runs if the first command succeeds.

---

## >

```bash
command > file.txt
```

Redirects output into a file.

If the file already exists, its contents are overwritten.

---

## >>

```bash
command >> file.txt
```

Appends output to a file instead of overwriting existing contents.
