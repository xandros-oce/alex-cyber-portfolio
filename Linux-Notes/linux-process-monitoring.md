# Linux Process Monitoring

# Process Monitoring

Process monitoring is an important Linux and cybersecurity skill used to:

* investigate running applications
* identify suspicious activity
* monitor CPU and memory usage
* troubleshoot system performance

---

# ps aux

```bash id="t2q7vn"
ps aux
```

Displays:

* running processes
* users running processes
* CPU and memory usage
* process IDs (PIDs)

---

# grep

```bash id="9m5xqp"
grep
```

Used to search for specific values or text.

Often combined with other commands using a pipe (`|`).

---

# ps aux | grep

Example:

```bash id="v7x4pk"
ps aux | grep systemd-resolve
```

This command:

* shows all running processes
* filters output for `systemd-resolve`

---

# Pipe Operator

```bash id="0p4kzt"
|
```

The pipe operator takes output from one command and feeds it into another command.

This is heavily used in Linux administration and cybersecurity investigations.

---

# Example Output

```bash id="5w8nrm"
systemd+ 393 ... /usr/lib/systemd/systemd-resolved
```

---

# Process Breakdown

| Section                           | Meaning              |
| --------------------------------- | -------------------- |
| systemd+                          | User running process |
| 393                               | Process ID (PID)     |
| Ss                                | Process state        |
| /usr/lib/systemd/systemd-resolved | Executable path      |

---

# top

```bash id="3k9vpa"
top
```

Linux terminal equivalent of Task Manager.

Displays:

* live running processes
* CPU usage
* memory usage
* real-time system activity

`top` is one of the most commonly used Linux monitoring tools.

---

# Observations

Highest CPU usage observed:

* `gnome-shell`

`gnome-shell` is the graphical Linux desktop interface.

---

# htop

```bash id="7x1qmd"
htop
```

Interactive and improved version of `top`.

Provides:

* easier navigation
* colour-coded process monitoring
* improved readability

---

# Observations

Highest memory usage observed:

* `gnome-shell`

---

# Process IDs (PIDs)

A PID (Process ID) is a unique number assigned to a running process.

PIDs are important for:

* identifying processes
* troubleshooting
* monitoring system activity
* stopping processes
* cybersecurity investigations

---

# Cybersecurity Relevance

Security analysts and defenders often monitor:

* unusual processes
* unexpected CPU usage
* suspicious executables
* unknown running services
* malicious background activity

Attackers and malware may:

* disguise malicious processes
* hide persistence
* consume system resources
* run hidden services

Process monitoring is a core Linux administration and cybersecurity skill.

