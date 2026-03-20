# Linux Security Lab — AppArmor (SELinux Alternative)

## Objective
The purpose of this lab is to understand and manage Linux security using AppArmor. This includes checking AppArmor status, identifying active profiles, switching profiles between complain and enforce modes, and troubleshooting real-world permission and configuration issues.

---

## Environment
- Ubuntu Linux (VirtualBox VM)
- Bash Terminal
- Windows Host Machine
- Git Bash
- AppArmor Security Framework

---

## Commands Used
| Command | Description |
|--------|-------------|
| aa-status | Displays AppArmor status and loaded profiles |
| grep | Filters output for specific keywords |
| systemctl status apparmor | Checks AppArmor service status |
| aa-complain | Sets profile to complain mode (logs only) |
| aa-enforce | Sets profile to enforce mode (actively blocks) |
| apt update | Updates package list |
| apt install apparmor-utils -y | Installs AppArmor utilities |
| clear | Clears terminal screen |

---

## Command Definitions (Beginner Friendly)
- sudo → Runs command as administrator (root user)
- aa-status → Shows what AppArmor is protecting
- grep → Searches for specific words in output
- aa-complain → Allows activity but logs it (monitor mode)
- aa-enforce → Blocks unauthorized activity (secure mode)
- apt → Linux package manager
- -y → Automatically says “yes” to prompts

---

## Symbol & Syntax Breakdown
| Symbol | Meaning |
|--------|--------|
| \| | Pipe — sends output from one command to another |
| / | Root directory path separator |
| -y | Automatic yes for installations |
| (PID) | Process ID — identifies running process |

---

## Screenshots & Explanations

### Screenshot 01 — AppArmor Status Check
Command:
sudo aa-status

Explanation:
Displays all loaded AppArmor profiles and enforcement status. Confirms AppArmor is active and protecting system services.

---

### Screenshot 02 — AppArmor Service Status
Command:
systemctl status apparmor

Explanation:
Shows that the AppArmor service is running and enabled at the system level.

---

### Screenshot 03 — Enforced Profiles
Command:
sudo aa-status | grep enforce

Explanation:
Filters output to display only profiles currently in enforce mode. This helps identify which services are actively protected.

---

### Screenshot 04 — Full Profile List
Command:
sudo aa-status

Explanation:
Displays all AppArmor profiles loaded on the system, including snap packages and system services.

---

### Screenshot 05 — Complain Mode (Troubleshooting Included)
Commands:
sudo aa-complain /bin/ping
aa-complain /usr/sbin/cupsd
sudo aa-complain /usr/sbin/cupsd

Explanation:
- First attempt failed because /bin/ping does not have an AppArmor profile
- Second attempt failed due to missing sudo (permission denied)
- Final attempt succeeded with elevated privileges

Professional Explanation:
Initially attempted to run aa-complain on a binary without a profile, resulting in no action. Then encountered a permission error when modifying /usr/sbin/cupsd. Resolved the issue by rerunning the command with sudo, successfully switching the profile into complain mode.

---

### Screenshot 06 — Verification
Command:
sudo aa-status | grep cupsd

Explanation:
Confirms that the cupsd service is running and actively tracked by AppArmor. Shows process ID and associated profile.

Professional Explanation:
Verified AppArmor profile status using filtered output and confirmed that the service is actively monitored.

---

### Screenshot 07 — Enforce Mode
Command:
sudo aa-enforce /usr/sbin/cupsd

Explanation:
Switches the profile back to enforce mode, ensuring that AppArmor actively blocks unauthorized actions instead of only logging them.

Professional Explanation:
Switched the AppArmor profile back to enforce mode, confirming the ability to toggle between monitoring and enforcement states.

---

## Key Concepts
- AppArmor is a Mandatory Access Control (MAC) system
- Profiles define allowed behavior for programs
- Complain mode logs activity without blocking
- Enforce mode actively blocks unauthorized actions
- Not all binaries have profiles
- Root privileges are required for security modifications

---

## Real-World Relevance
This lab demonstrates real-world Linux security administration skills including:
- System hardening
- Security monitoring vs enforcement
- Troubleshooting permission issues
- Managing service-level protection

Used in:
- Cloud Security
- DevOps
- System Administration
- Cybersecurity Operations

---

## What I Learned
- How to verify AppArmor is running
- How to identify active security profiles
- How to switch between complain and enforce modes
- How to troubleshoot missing profiles and permission issues
- How Linux security frameworks protect services

---

## Final Summary
In this lab, I completed a full AppArmor security workflow by verifying system status, identifying enforced profiles, troubleshooting errors, modifying profile modes, and validating changes. This demonstrates hands-on experience with Linux security controls and real-world system administration practices.