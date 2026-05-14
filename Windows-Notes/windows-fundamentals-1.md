# Windows Fundamentals 1

# Task Manager

Opened Task Manager using:

```bash
Ctrl + Shift + Esc
```

Task Manager is used to monitor:

* running processes
* CPU usage
* memory usage
* system performance
* background applications

---

## Process Investigation

### Highest Memory Usage

* VirtualBox Virtual Machine

### Highest CPU Usage

* Wallpaper32

### Unfamiliar Windows Processes

* crashhelper
* Runtime Broker
* WMI Provider Host

---

# Services

Opened the Windows Services section to investigate running and stopped services.

---

## Service Investigation

### Running Service

* Appinfo

### Stopped Service

* bthserv

### Unrecognised Service

* ALG

---

# Cybersecurity Relevance of Services

Attackers may:

* abuse Windows services
* create malicious services
* hide persistence within services
* disable security-related services

SOC analysts frequently investigate:

* strange service names
* stopped security services
* newly created services

---

# Resource Monitor

Opened:

* Resource Monitor
* Network tab

Used to monitor:

* active network activity
* processes using the network
* remote connections
* network usage

---

## Network Investigation

### Highest Network Usage

* Battle.net.exe

### Remote Address Observed

* 192.168.0.73

### Recognised Port

* Port 445

Port 445 is commonly associated with:

* SMB (Server Message Block)
* Windows file sharing

---

# TCP vs UDP

## My Original Answer

> TCP is connection with safety and checks
> UDP is fast connections like streaming

---

# Teacher Feedback

Strong beginner understanding.

Correctly identified:

* TCP focuses on reliability and checking
* UDP focuses on speed and low overhead

These are the most important differences between the two protocols.

---

# TCP

TCP (Transmission Control Protocol) is a connection-oriented protocol that ensures data is delivered reliably and in the correct order.

TCP:

* checks if packets arrive
* retransmits missing data
* establishes connections before communication begins

Common uses:

* websites
* logins
* downloads
* email
* SSH

TCP prioritises:

* reliability
* accuracy
* ordered delivery

---

# UDP

UDP (User Datagram Protocol) is a lightweight, connectionless protocol designed for speed and efficiency.

UDP:

* does not guarantee delivery
* does not retransmit lost packets
* sends data with minimal overhead

Common uses:

* streaming
* gaming
* voice/video calls
* DNS

UDP prioritises:

* speed
* low latency
* efficiency

---

# Simple Analogy

TCP:

* like sending a registered package with tracking and confirmation

UDP:

* like shouting information across a room without checking every word was heard

---

# Windows Networking

Opened Command Prompt (`cmd`) to practice Windows networking commands.

---

# ipconfig

```bash
ipconfig
```

Displays:

* IP configuration
* IPv4 address
* default gateway
* network adapter information

Linux equivalent:

```bash
ip a
```

---

## Network Information

### IPv4 Address

* 192.168.0.x

### Default Gateway

* 192.168.0.1

### Address Type

* Private IP address

---

# NAT (Network Address Translation)

Home routers commonly perform NAT.

NAT allows:

* multiple private devices
* to share one public IP address

This allows multiple devices in a home network to access the internet simultaneously.

---

# netstat -ano

```bash
netstat -ano
```

Flags:

* `-a` = all connections
* `-n` = numeric addresses
* `-o` = show PID

Displays:

* active connections
* listening ports
* TCP/UDP activity
* process IDs (PIDs)

---

## Observations

Recognised:

* TCP
* UDP
* LISTENING connections
* Ports 445 and 135

---

# Windows vs Linux Command Comparison

| Linux             | Windows               |
| ----------------- | --------------------- |
| ss                | netstat               |
| top               | Task Manager          |
| services/daemons  | services              |
| listening sockets | listening connections |

---

# Process and PID Investigation

Example observed:

```bash
TCP 0.0.0.0:7680 0.0.0.0:0 LISTENING 7612
```

Associated process:

* svchost.exe

`svchost.exe` is a Windows host process used to run Windows services.

---

# File System

Windows commonly uses:

* NTFS (New Technology File System)

Older Windows file systems included:

* FAT16
* FAT32
* HPFS

NTFS supports:

* permissions
* access control
* file/folder security

---

# NTFS Permissions

Permissions determine what users can do with files and folders.

Common permissions:

* Read
* Write
* Read & Execute
* Modify
* Full Control

This is similar to Linux permissions using:

* read (`r`)
* write (`w`)
* execute (`x`)

---

# Local Users and Groups

Opened:

```bash
lusrmgr.msc
```

Used to:

* view local users
* view groups
* inspect account permissions
* investigate user properties

Observed:

* user group memberships
* account descriptions
* user property tabs

---

# Cybersecurity Relevance

User and group enumeration is important because attackers and defenders both investigate:

* local accounts
* administrator privileges
* group memberships
* access permissions

This is also important for:

* troubleshooting
* account auditing
* privilege management

---

# Room Completed

Completed:

* TryHackMe: Windows Fundamentals 1

