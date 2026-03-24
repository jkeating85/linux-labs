# Linux+ Lab 45 — System Performance and Storage Troubleshooting

---

# Objective

The purpose of this lab was to learn how Linux administrators troubleshoot system performance issues and analyze storage utilization using professional Linux monitoring tools.

In this lab, I performed:

- System performance monitoring
- CPU usage analysis
- Memory monitoring
- Disk usage troubleshooting
- System load monitoring
- Process monitoring
- Storage performance analysis

These skills are critical for:

- Linux System Administration
- Cloud Engineering
- DevOps Engineering
- Site Reliability Engineering (SRE)
- Cybersecurity Operations

---

# Environment

- Ubuntu Linux Virtual Machine (VirtualBox)
- Windows 11 Host Machine
- Git Bash
- GitHub Repository
- Linux Terminal (Bash)

---

# Commands Used

| Command | Description |
|--------|-------------|
| top | Live system process monitor |
| htop | Advanced interactive system monitor |
| df -h | Disk filesystem usage |
| du -sh | Directory disk usage |
| iostat | Disk performance statistics |
| vmstat | Virtual memory statistics |
| mpstat | CPU performance statistics |
| uptime | System load information |
| free -h | Memory usage |
| uname -a | System information |

---

# Command Breakdown

## top

Displays real-time system processes.

Breakdown:

- CPU usage
- Memory usage
- Running processes
- System load

---

## htop

Enhanced version of top with:

- Better UI
- Interactive process management
- CPU graphs
- Memory graphs

---

## df -h

Disk filesystem usage

Breakdown:

- df = disk filesystem
- -h = human readable format (GB, MB)

---

## du -sh

Directory disk usage

Breakdown:

- du = disk usage
- -s = summary
- -h = human readable

---

## iostat

Disk performance monitoring

Shows:

- Disk read/write activity
- IO performance
- CPU usage

---

## vmstat

Virtual memory statistics

Displays:

- Memory usage
- CPU activity
- IO statistics

---

## mpstat

CPU statistics

Displays:

- CPU usage per core
- CPU idle time
- CPU load

---

## uptime

System load

Displays:

- System uptime
- Number of users
- Load averages

---

## free -h

Memory usage

Displays:

- RAM usage
- Swap usage
- Available memory

---

## uname -a

System information

Displays:

- Kernel version
- Architecture
- Hostname

---

# Workflow / Steps

1. Created Lab Folder
2. Checked System Health
3. Used top command
4. Installed htop
5. Used htop monitor
6. Used iostat
7. Used df
8. Used vmstat
9. Used mpstat
10. Used uptime
11. Used free
12. Used uname

---

# Screenshots

---

## Screenshot 01

![01_lab_45_folder_structure](screenshots/01_lab_45_folder_structure.png)

This screenshot shows the folder structure created for Linux+ Lab 45. This demonstrates proper lab organization and professional documentation practices used in enterprise environments.

---

## Screenshot 02

![02_initial_system_health_check](screenshots/02_initial_system_health_check.png)

This screenshot shows the initial system health check using Linux monitoring commands. This allows administrators to quickly identify performance issues.

---

## Screenshot 03

![03_top_live_process_monitor](screenshots/03_top_live_process_monitor.png)

This screenshot shows the top command running. The top command provides a real-time view of CPU usage, memory usage, and running processes.

---

## Screenshot 04

![04_install_htop](screenshots/04_install_htop.png)

This screenshot shows the installation of htop using apt package manager. This demonstrates installing troubleshooting tools.

---

## Screenshot 05

![05_htop_system_monitor](screenshots/05_htop_system_monitor.png)

This screenshot shows htop running. It provides advanced system monitoring with CPU graphs and memory usage.

---

## Screenshot 06

![06_iostat_disk_usage](screenshots/06_iostat_disk_usage.png)

This screenshot shows disk performance using iostat. This helps diagnose storage bottlenecks.

---

## Screenshot 07

![07_df_disk_filesystem_usage](screenshots/07_df_disk_filesystem_usage.png)

This screenshot shows filesystem disk usage using df -h.

---

## Screenshot 08

![08_memory_and_vmstat_usage](screenshots/08_memory_and_vmstat_usage.png)

This screenshot shows virtual memory usage using vmstat.

---

## Screenshot 09

![09_mpstat_cpu_statistics](screenshots/09_mpstat_cpu_statistics.png)

This screenshot shows CPU statistics using mpstat.

---

## Screenshot 10

![10_vmstat_live_performance](screenshots/10_vmstat_live_performance.png)

This screenshot shows live system performance monitoring.

---

## Screenshot 11

![11_top_cpu_processes](screenshots/11_top_cpu_processes.png)

This screenshot shows CPU intensive processes.

---

## Screenshot 12

![12_top_memory_processes](screenshots/12_top_memory_processes.png)

This screenshot shows memory intensive processes.

---

## Screenshot 13

![13_disk_usage_df](screenshots/13_disk_usage_df.png)

This screenshot shows disk usage information.

---

## Screenshot 14

![14_directory_disk_usage](screenshots/14_directory_disk_usage.png)

This screenshot shows directory disk usage using du.

---

## Screenshot 15

![15_iostat_disk_performance](screenshots/15_iostat_disk_performance.png)

This screenshot shows disk IO performance.

---

## Screenshot 16

![16_system_load_uptime](screenshots/16_system_load_uptime.png)

This screenshot shows system load using uptime.

---

## Screenshot 17

![17_top_interactive_monitor](screenshots/17_top_interactive_monitor.png)

This screenshot shows interactive top monitoring.

---

## Screenshot 18

![18_memory_usage_free](screenshots/18_memory_usage_free.png)

This screenshot shows memory usage using free -h.

---

## Screenshot 19

![19_system_information_uname](screenshots/19_system_information_uname.png)

This screenshot shows system information using uname -a.

---

# Key Concepts

- System Performance Monitoring
- Disk Performance
- CPU Monitoring
- Memory Monitoring
- Storage Troubleshooting

---

# Real-World Relevance

These commands are used by:

- Linux Administrators
- DevOps Engineers
- Cloud Engineers
- Site Reliability Engineers
- Cybersecurity Analysts

These tools help diagnose:

- High CPU usage
- Memory leaks
- Disk bottlenecks
- System crashes

---

# What I Learned

In this lab, I learned:

- How to monitor system performance
- How to analyze disk performance
- How to troubleshoot CPU usage
- How to monitor memory usage
- How to use professional Linux troubleshooting tools

This lab provided real-world Linux troubleshooting experience.

---