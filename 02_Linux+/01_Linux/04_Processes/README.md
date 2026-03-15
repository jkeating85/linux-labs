# Linux Processes Lab

## Objective

Demonstrate how Linux processes can be monitored, run in the background, and terminated.

## Environment

* Ubuntu Linux (Virtual Machine)
* Oracle VirtualBox
* Windows 11 Host Machine
* Linux Terminal

## Commands Used

### top

Displays running processes and system resource usage in real time.

### sleep

Creates a temporary process used for testing.

### &

Runs a command in the background.

### jobs

Displays background jobs in the current shell session.

### kill

Terminates a running process using its Process ID (PID).

## What Was Tested

### Process Monitoring

Used `top` to observe running system processes.

### Background Processes

Created a background process using:

sleep 120 &

### Job Verification

Confirmed the process was running using:

jobs

### Process Termination

Stopped the process using:

kill PID

## Key Concepts Learned

* Linux processes run in either foreground or background.
* Every process has a unique PID.
* System administrators can monitor and terminate processes.

## Visual Evidence

### Basic Process List
![Basic Process List](Screenshots/01-basic-process-list.png)

### All Processes
![All Processes](Screenshots/02-all-processes.png)

### Process Monitoring with top
![top command](Screenshots/03-top-monitor.png)

### Background Process
![Background Process](Screenshots/04-background-process.png)

### Jobs Command
![Jobs Command](Screenshots/05-jobs-command.png)

### Killing a Process
![Kill Process](Screenshots/06-kill-process.png)

## What I Learned

This lab demonstrates how Linux manages processes and how administrators monitor and control running tasks.
