# Linux Log Analysis with grep and awk

## Lab Overview

This lab demonstrates how Linux administrators and security engineers analyze system log files using command-line tools.

Linux systems record important activity in log files. These logs contain information about:

* login attempts
* service activity
* authentication events
* system errors
* background processes

By learning how to search and extract information from logs, administrators can troubleshoot system problems and identify suspicious activity.

In this lab we used two important Linux tools:

* **grep** – used to search for specific patterns in text
* **awk** – used to extract structured data from files

These tools are commonly used in:

* Linux system administration
* DevOps engineering
* site reliability engineering (SRE)
* cybersecurity and incident response

---

# Lab Environment

Operating System: Ubuntu Linux (Virtual Machine)
Virtualization Platform: Oracle VirtualBox
Shell: Bash Terminal

Log files used in this lab:

/var/log/auth.log
/var/log/syslog

These log files store authentication events and system activity.

---

# Screenshot Evidence

## 1 — Lab Folder Creation

Screenshot:

Screenshots/01_lab19_folder_created.png

Command used:

mkdir 19_Log_Analysis_with_grep_awk

### Command Definition

**mkdir**

Make Directory — creates a new folder in the filesystem.

### Command Breakdown

mkdir → command used to create directories
19_Log_Analysis_with_grep_awk → name of the folder created for the lab

---

# 2 — Entering the Lab Directory

Screenshot:

Screenshots/02_inside_lab19_directory.png

Command used:

cd 19_Log_Analysis_with_grep_awk

### Command Definition

**cd**

Change Directory — moves the terminal into another folder.

### Command Breakdown

cd → change directory command
19_Log_Analysis_with_grep_awk → destination directory

---

# 3 — Searching Authentication Logs for SSH Activity

Screenshot:

Screenshots/03_ssh_log_search.png

Command used:

grep ssh /var/log/auth.log

### Command Definition

**grep**

Global Regular Expression Print — searches files for matching text patterns.

### Command Breakdown

grep → search tool
ssh → keyword being searched
/var/log/auth.log → authentication log file

### What This Command Shows

This command searches the authentication log file for entries related to SSH activity.

Examples of events that may appear:

* SSH service starting
* SSH login attempts
* SSH daemon activity

---

# 4 — Counting SSH Log Entries

Screenshot:

Screenshots/04_ssh_log_count.png

Command used:

grep ssh /var/log/auth.log | wc -l

### Command Breakdown

grep ssh → finds SSH-related log entries

| → pipe operator that sends output to another command

wc → word count utility

-l → counts lines of text

### Symbol Explanation

**| (pipe)**

The pipe operator sends the output of one command to another command.

Example:

Command A | Command B

Output from Command A becomes input for Command B.

### What This Command Does

1. Searches authentication logs for SSH entries
2. Sends those results to the wc command
3. Counts how many lines exist

This shows the number of SSH events recorded in the log.

---

# 5 — Extracting Timestamp Fields with awk

Screenshot:

Screenshots/05_log_timestamp_fields.png

Command used:

awk '{print $1,$2,$3}' /var/log/syslog | head

### Command Definition

**awk**

A powerful Linux text-processing tool used to extract and manipulate columns of data from structured text files.

### Command Breakdown

awk → text processing program

{print $1,$2,$3} → print the first three columns of each line

/var/log/syslog → system activity log file

| → pipe output to the next command

head → display the first 10 lines of output

### Symbol Explanation

**$ (field indicator)**

In awk, the dollar symbol represents a column in the text.

$1 → first column
$2 → second column
$3 → third column

### What This Command Does

Extracts the timestamp columns from the system log file.

Example output:

Mar 10 20:30
Mar 10 20:31
Mar 10 20:32

Security engineers often examine timestamps to understand when system events occurred.

---

# 6 — Searching Logs for Password Events

Screenshot:

Screenshots/06_failed_login_attempts.png

Command used:

grep -i password /var/log/auth.log | head

### Command Breakdown

grep → search command

-i → ignore case sensitivity

password → keyword being searched

/var/log/auth.log → authentication log file

| → send results to another command

head → show first 10 results

### Flag Explanation

**-i**

The -i flag tells grep to ignore case sensitivity.

Examples that would match:

password
Password
PASSWORD

### What This Command Shows

Authentication events related to password activity including:

* login sessions
* authentication checks
* credential events

Security engineers analyze these logs to detect:

* failed login attempts
* brute-force attacks
* suspicious access attempts

---

# Key Linux Concepts Learned

## grep

grep is used to search files for specific text patterns.

Common uses include:

* searching system logs
* filtering command output
* troubleshooting services

---

## awk

awk is a text processing language used to extract columns from structured text.

Common uses include:

* parsing log files
* formatting output
* analyzing structured data

---

# Linux Log Analysis

Linux systems store logs that record:

* authentication events
* service activity
* system processes
* security alerts

Log analysis helps administrators:

* troubleshoot system issues
* monitor system behavior
* investigate suspicious activity
* detect security incidents

---

# Lab Summary

In this lab I practiced analyzing Linux system log files using commonly used command-line tools.

Skills demonstrated:

* searching logs with grep
* counting log entries with wc
* extracting data fields with awk
* investigating authentication events

These skills are important for roles in:

* Linux System Administration
* DevOps Engineering
* Site Reliability Engineering
* Cybersecurity
* Cloud Infrastructure Operations
