# Linux Lab 33 — SSH, DNS, and Network Services

---

## Objective

The purpose of this lab is to configure, verify, and test core Linux network services including SSH, DNS resolution, and network connectivity.

This lab demonstrates real-world system administration and networking skills used in cloud engineering, DevOps, and cybersecurity roles.

---

## Environment

- Ubuntu Linux (VirtualBox VM)
- Bash Terminal
- OpenSSH Server
- DNS Utilities (nslookup, dig)
- Networking Tools (ping, ss, ip)

---

## Commands Used and Definitions

### Package Management

- `sudo apt update`
  - Updates package lists from repositories
  - `sudo` = run command as root (superuser)
  - `apt` = Advanced Package Tool
  - `update` = refresh available packages

- `sudo apt install openssh-server dnsutils net-tools -y`
  - Installs required networking tools
  - `-y` = automatically answer yes to prompts

---

### SSH (Secure Shell)

- `systemctl status ssh`
  - Checks SSH service status
  - `systemctl` = system service manager

- `ssh localhost`
  - Connects to the same machine using SSH
  - `localhost` = 127.0.0.1 (loopback address)

- `exit`
  - Closes SSH session

---

### Networking Commands

- `ip a`
  - Displays network interfaces and IP addresses

- `hostname`
  - Displays system hostname

- `hostname -I`
  - Displays all assigned IP addresses

---

### DNS Tools

- `nslookup google.com`
  - Queries DNS server for IP address

- `dig google.com`
  - Advanced DNS query tool (used by engineers)

---

### Connectivity Testing

- `ping -c 4 google.com`
  - Sends 4 ICMP packets
  - Tests network connectivity

---

### Port and Service Inspection

- `ss -tulnp`
  - Displays listening ports and services
  - `-t` = TCP
  - `-u` = UDP
  - `-l` = listening sockets
  - `-n` = numeric output
  - `-p` = show process

---

## Symbols and Flags Explained

- `-c` → count (number of packets)
- `-t` → TCP protocol
- `-u` → UDP protocol
- `-l` → listening ports only
- `-n` → numeric output (no DNS resolution)
- `-p` → process information
- `:` → separates IP and port
- `127.0.0.1` → loopback address (local machine)
- `0.0.0.0` → all network interfaces
- `[::]` → IPv6 equivalent of all interfaces

---

## Screenshots and Explanations

### Screenshot 01 — System Update
Shows successful package list update from Ubuntu repositories.

---

### Screenshot 02 — Package Installation
Confirms installation of:
- OpenSSH Server
- DNS utilities
- Networking tools

---

### Screenshot 03 — SSH Service Status
SSH service is:
- Active (running)
- Enabled at startup
- Listening on port 22

---

### Screenshot 04 — IP Address Configuration
Shows multiple interfaces:
- `10.0.2.15` → NAT (VirtualBox)
- `172.17.0.1` → Docker network
- `192.168.122.1` → libvirt network

This demonstrates a layered virtual networking environment.

---

### Screenshot 05 — SSH Local Connection
Successful SSH login to localhost.

This proves:
- Authentication works
- SSH service is functional

---

### Screenshot 06 — Exit SSH Session
Shows clean exit from SSH session.

---

### Screenshot 07 — DNS Lookup (nslookup)
DNS query successfully resolved google.com.

Key observations:
- DNS server: 127.0.0.53 (systemd-resolved)
- Multiple IPs returned (load balancing)

---

### Screenshot 08 — Advanced DNS Query (dig)
Detailed DNS response including:
- ANSWER SECTION
- Query time
- Server information

This confirms proper DNS functionality.

---

### Screenshot 09 — Network Connectivity (ping)
Results:
- 0% packet loss
- Stable latency (~46 ms)

This confirms reliable network connectivity.

---

### Screenshot 10 — Open Ports (ss)
Shows active listening ports including:

- Port 22 (SSH)
- DNS service (127.0.0.53:53)
- Virtualization networking interfaces

---

### Screenshot 11 — Hostname and IP
Displays:
- System hostname
- All assigned IP addresses

Confirms system identity and network configuration.

---

## Key Concepts

- SSH enables secure remote access
- DNS translates domain names to IP addresses
- ICMP (ping) tests connectivity
- Ports represent services running on a system
- Virtual networking is used in cloud and virtualization environments

---

## Real-World / Interview Explanations

### SSH Verification
“I verified that the SSH service was running and accessible by connecting locally using SSH, confirming authentication and service availability.”

---

### DNS Analysis
“DNS resolution was successful using both nslookup and dig. Multiple A records were returned, indicating load balancing, and queries were handled by the local systemd-resolved service.”

---

### Network Connectivity
“I validated network connectivity using ping, confirming 0% packet loss and stable latency, indicating a healthy network connection.”

---

### Port Inspection (ss Command)
“I used the ss command to inspect listening ports and verified that SSH was actively listening on port 22 across all interfaces. I also identified local DNS resolution services and virtual networking interfaces, confirming proper system and virtualization network configuration.”

---

## What I Learned

- How to install and configure SSH
- How to verify system services using systemctl
- How DNS resolution works using nslookup and dig
- How to test connectivity using ping
- How to inspect open ports using ss
- How virtualization creates layered networking environments
- How to explain system behavior like a professional engineer

---

## Real-World Relevance

These skills are used in:

- Cloud Engineering (AWS, Azure)
- DevOps and Infrastructure Automation
- Cybersecurity and Network Analysis
- System Administration

This lab simulates real-world troubleshooting and system validation tasks performed by engineers daily.

---