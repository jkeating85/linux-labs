# Linux Scripting Lab

## Objective
Create and execute a basic Bash script that collects system information including user details, system uptime, disk usage, memory usage, logged-in users, and open network ports.

---

## Environment
- Ubuntu Linux (VirtualBox VM)
- Bash Shell
- VS Code for documentation
- Git & GitHub for version control

---

## Script Created
system_audit.sh

This script performs a basic system audit by displaying:

- Current logged in user
- System uptime
- Disk usage
- Memory usage
- Logged in users
- Open network ports

---

## Commands Used

| Command | Description |
|------|------|
| nano | Create and edit the script |
| chmod +x | Make the script executable |
| ./scriptname | Execute the script |
| df -h | Show disk usage |
| free -h | Show memory usage |
| whoami | Display current user |
| who | Show logged-in users |
| uptime | Display system uptime |
| ss -tuln | Show open network ports |

---

## Screenshots

### Script Directory
![Script Directory](Screenshots/01-script-directory.png)

### Writing the Script
![Script Writing](Screenshots/02-script-writing.png)

### Script Permissions
![Script Permissions](Screenshots/03-script-permissions.png)

### Script Output
![Script Output](Screenshots/04-script-output.png)

---

## What I Learned

- How to create Bash scripts
- How to make scripts executable using chmod
- How to run scripts from the terminal
- How to gather system information using Linux commands
- How to document technical work for GitHub

## Script Breakdown

The Bash script created in this lab gathers basic system information by executing several Linux commands automatically.

Explanation of key parts of the script:

#!/bin/bash  
Tells Linux to run the script using the Bash shell interpreter.

echo  
Prints text messages to the terminal to organize the report output.

whoami  
Displays the username of the currently logged-in user.

uptime  
Shows how long the system has been running along with the current load average.

df -h  
Displays disk usage in a human-readable format (GB/MB instead of blocks).

free -h  
Shows memory usage including total, used, and available RAM.

who  
Lists users currently logged into the system.

ss -tuln  
Displays open network ports and listening services on the system.
