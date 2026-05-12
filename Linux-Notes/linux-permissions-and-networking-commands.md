# Linux Permissions and Networking Commands

# Linux Permissions

## Viewing Permissions

```bash
ls -l
```

Displays files and directories with detailed permissions.

Example permission string:

```bash
-rwxr-xr-x
```

Permission meanings:
- r = read
- w = write
- x = execute

Permission groups:
- First group = owner permissions
- Second group = group permissions
- Third group = everyone else

---

## chmod

```bash
chmod 755 notes.txt
```

Changes file permissions.

755 means:
- Owner = read, write, execute
- Group = read, execute
- Others = read, execute

---

# File Searching

```bash
find ~/alex-training -name "*.txt"
```

Searches recursively for all `.txt` files inside the `alex-training` directory.

---

# Networking Commands

## ip a

```bash
ip a
```

Displays:
- network interfaces
- IP addresses
- network adapter information

---

## ping

```bash
ping 8.8.8.8
```

Tests connectivity between devices.

Used for:
- checking internet connectivity
- testing network communication
- measuring response time

---

## ping google.com

```bash
ping google.com
```

Demonstrates DNS resolution by converting a domain name into an IP address before sending packets.

---

# DNS

DNS (Domain Name System) translates domain names into IP addresses.

Example:
- google.com → IP address

---

## nslookup

```bash
nslookup google.com
```

Queries DNS servers to retrieve IP address information for a domain.

---

## traceroute

```bash
traceroute google.com
```

Displays the route packets take across networks to reach a destination.
