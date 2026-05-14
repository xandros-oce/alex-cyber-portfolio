# Network Monitoring and Ports

# Active Network Monitoring

Practiced monitoring active network connections, ports, protocols, and processes using Linux networking tools.

---

# ss -tulpen

```bash id="l7m3vx"
ss -tulpen
```

Displays:

* listening ports
* active network sockets
* protocols
* processes using the network

Using `sudo` provides additional process information:

```bash id="r5a9qk"
sudo ss -tulpen
```

---

# TCP vs UDP

## TCP

TCP (Transmission Control Protocol) is:

* reliable
* connection-oriented
* checks if data arrives correctly

Used for:

* websites
* SSH
* downloads
* logins

TCP prioritises:

* reliability
* accuracy
* ordered delivery

---

## UDP

UDP (User Datagram Protocol) is:

* faster
* lightweight
* connectionless
* does not confirm delivery

Used for:

* streaming
* gaming
* DNS
* voice/video calls

UDP prioritises:

* speed
* low latency
* efficiency

---

# IP Addresses and Ports

Analogy:

* IP address = house address
* Port = door inside the house

Example:

```bash id="eh8zpf"
192.168.1.15:22
```

Breakdown:

* `192.168.1.15` = device IP address
* `22` = SSH service port

---

# Common Ports

| Port | Service |
| ---- | ------- |
| 22   | SSH     |
| 80   | HTTP    |
| 443  | HTTPS   |
| 53   | DNS     |
| 25   | SMTP    |
| 3389 | RDP     |

---

# Process and Port Visibility

Example observed:

```bash id="1qmybd"
tcp LISTEN 127.0.0.1:631 users:(("cupsd",pid=1446))
```

Breakdown:

| Section   | Meaning                 |
| --------- | ----------------------- |
| tcp       | Protocol                |
| LISTEN    | Waiting for connections |
| 127.0.0.1 | Localhost               |
| 631       | Port                    |
| cupsd     | Process name            |
| pid=1446  | Process ID              |

---

# Cybersecurity Relevance

In cybersecurity, defenders frequently ask:

> What process is using this port?

This is important because malware may:

* open hidden ports
* create listeners
* communicate externally
* bind to suspicious services

Process visibility + port visibility is a critical cybersecurity skill.

---

# ps aux | grep

```bash id="5mg0ju"
ps aux | grep systemd-resolve
```

The `|` symbol pipes output from one command into another.

This command:

* displays all running processes
* filters results for `systemd-resolve`

Observed output:

```bash id="r0pzsu"
systemd+ 393 ... /usr/lib/systemd/systemd-resolved
```

---

# Process Breakdown

| Section                           | Meaning              |
| --------------------------------- | -------------------- |
| systemd+                          | User running process |
| 393                               | PID                  |
| Ss                                | Process state        |
| /usr/lib/systemd/systemd-resolved | Executable path      |

---

# top

```bash id="q9lyxj"
top
```

Linux terminal equivalent of Task Manager.

Displays:

* live running processes
* CPU usage
* memory usage
* real-time system activity

Observed:

* `gnome-shell` using highest CPU usage

`gnome-shell` is the graphical Linux desktop interface.

---

# htop

```bash id="3exm8n"
htop
```

Improved interactive version of `top`.

Observed:

* `gnome-shell` using highest memory usage

---

# lsof -i

```bash id="o8vawz"
lsof -i
```

Displays open files and active network connections.

Initially returned no output because no active network connections were occurring during execution.

---

# curl Network Testing

Used:

```bash id="6rz9hk"
curl google.com
```

Then used a larger file download to maintain an active connection:

```bash id="m3x1pq"
curl http://speed.hetzner.de/100MB.bin -o /dev/null
```

This allowed `lsof -i` to capture active network activity.

---

# Connection Breakdown

| Section                | Meaning               |
| ---------------------- | --------------------- |
| curl                   | Process name          |
| 5078                   | PID                   |
| alex                   | User running process  |
| TCP                    | Protocol              |
| 40592                  | Temporary source port |
| nbg1-speed.hetzner.com | Remote server         |
| http                   | Destination service   |
| ESTABLISHED            | Active connection     |

---

# Networking Concepts

## IP Address

An IP address is a unique address assigned to a device on a network.

Examples:

* laptop
* phone
* router
* server

Analogy:

* IP address = house address

---

## Port

A port is a communication endpoint used by services and applications.

Examples:

* Port 80 = HTTP
* Port 443 = HTTPS
* Port 22 = SSH

Analogy:

* Port = door inside the house

---

## Protocol

A protocol is a set of rules that defines how devices communicate across a network.

Examples:

* TCP
* UDP
* ICMP
* HTTP
* HTTPS

Protocols determine:

* how data is sent
* how devices communicate
* how reliability and speed are handled

---

# Final Example

```bash id="bov5ak"
142.250.207.14:80 using TCP
```

Breakdown:

* IP address = the server/device
* Port 80 = web service
* TCP = communication protocol

