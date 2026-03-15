# Linux User Environment & Shell Configuration Lab

## Objective

The purpose of this lab is to understand how Linux manages **user environments**, **shell configuration files**, and **environment variables**.

In this lab I explored:

* Hidden configuration files
* User shell environment variables
* The system PATH variable
* Bash shell configuration files
* Creating command aliases
* Persisting custom shell settings using `.bashrc`

These concepts are extremely important for **Linux administration, DevOps engineering, cloud infrastructure management, and cybersecurity operations**.

---

# Environment

Operating System:
Ubuntu Linux (Virtual Machine)

Virtualization:
Oracle VirtualBox

Host Machine:
Windows 11

Tools Used:

* Bash Terminal
* GNU Nano text editor
* VS Code
* Git Bash
* GitHub

---

# Commands Used

| Command            | Description                            |
| ------------------ | -------------------------------------- |
| `ls -a`            | Lists all files including hidden files |
| `printenv`         | Displays environment variables         |
| `echo $PATH`       | Displays the PATH variable             |
| `nano ~/.bashrc`   | Opens the Bash configuration file      |
| `alias`            | Creates a shortcut command             |
| `source ~/.bashrc` | Reloads the Bash configuration         |
| `ll`               | Custom alias for `ls -lah`             |

---

# Command Definitions

## ls

`ls` means **list**.

It displays files and directories inside the current folder.

Example:

ls

---

## ls -a

The `-a` flag means **all files**.

This shows **hidden files**, which normally start with a dot (`.`).

Example hidden files:

.bashrc
.profile
.config

These files store **user configuration settings**.

Command used:

ls -a

---

## printenv

`printenv` displays **environment variables** currently loaded in the Linux session.

Environment variables store system information such as:

* user name
* home directory
* shell type
* terminal configuration
* system paths

Command used:

printenv

---

## echo

`echo` prints text or variable values to the terminal.

Example:

echo hello

Output:

hello

In this lab we used echo to display the PATH variable.

Command used:

echo $PATH

---

# Important Symbol Explanation

## $

The `$` symbol tells Linux to **retrieve the value of a variable**.

Example:

echo $PATH

Without `$`, Linux would print the word PATH instead of the value.

---

# PATH Variable

The **PATH variable** tells Linux where to search for executable programs.

Example output:

/usr/local/sbin
/usr/local/bin
/usr/sbin
/usr/bin
/sbin
/bin

When you type a command like:

ls

Linux searches these directories to find the program.

This allows commands to run **without typing the full path**.

---

# nano

`nano` is a simple **terminal text editor** used to edit configuration files.

Command used:

nano ~/.bashrc

This opens the `.bashrc` configuration file.

---

# ~ Symbol

The tilde symbol `~` represents the **current user's home directory**.

Example:

~/Documents

Means:

/home/username/Documents

In this lab:

nano ~/.bashrc

Means:

nano /home/username/.bashrc

---

# .bashrc File

`.bashrc` is a **Bash shell configuration file**.

It runs automatically every time a new terminal session starts.

It is used to configure:

* shell behavior
* environment variables
* aliases
* prompt appearance

This allows users to customize their Linux environment.

---

# alias Command

`alias` creates a **shortcut command**.

Example:

alias ll='ls -lah'

This allows the command:

ll

to run:

ls -lah

---

# ls -lah Breakdown

| Option | Meaning                   |
| ------ | ------------------------- |
| `l`    | Long listing format       |
| `a`    | Show hidden files         |
| `h`    | Human readable file sizes |

Example:

ls -lah

This shows:

* file permissions
* file ownership
* file sizes
* hidden files

---

# source Command

The `source` command reloads a configuration file **without restarting the terminal**.

Command used:

source ~/.bashrc

This forces Bash to re-read the configuration file.

Without this command you would need to **close and reopen the terminal**.

---

# Screenshots

## Screenshot 01 — Viewing Hidden Files

File:

01_hidden_files_ls-a.png

Description:

This screenshot shows the `ls -a` command displaying hidden Linux configuration files such as:

.bashrc
.profile
.config

These files control user environment settings.

---

## Screenshot 02 — Environment Variables

File:

02_printenv_output.png

Description:

This screenshot shows the `printenv` command output displaying environment variables including:

SHELL
HOME
USER
PATH
LANG

These variables define how the Linux environment behaves.

---

## Screenshot 03 — PATH Variable

File:

03_echo_path_variable.png

Description:

This screenshot displays the PATH variable using:

echo $PATH

This shows the directories Linux searches when running commands.

---

## Screenshot 04 — Creating Alias

File:

04_create_alias_ll.png

Description:

This screenshot shows the creation of a custom alias:

alias ll='ls -lah'

This allows the user to quickly run a detailed directory listing.

---

## Screenshot 05 — Editing Bash Configuration

File:

05_edit_bashrc.png

Description:

This screenshot shows the `.bashrc` file opened using the nano editor.

The alias command was added to make the shortcut permanent.

---

## Screenshot 06 — Saving Bash Configuration

File:

06_bashrc_saved.png

Description:

This screenshot shows the `.bashrc` configuration file after saving the alias entry.

---

## Screenshot 07 — Reloading Bash Configuration

File:

07_source_bashrc.png

Description:

The command used:

source ~/.bashrc

This reloads the Bash configuration so the new alias becomes active immediately.

---

## Screenshot 08 — Testing Alias

File:

08_alias_ll_test.png

Description:

This screenshot shows the alias command `ll` successfully executing the `ls -lah` command.

The output displays:

* file permissions
* hidden files
* file sizes
* directories

This confirms the alias was successfully loaded from `.bashrc`.

---

# Key Concepts Learned

Hidden files store Linux configuration settings.

Environment variables control system behavior and user sessions.

The PATH variable determines where Linux searches for executable programs.

The `.bashrc` file configures the Bash shell environment.

Aliases allow users to create shortcuts for frequently used commands.

The `source` command reloads configuration files without restarting the terminal.

---

# Why This Matters

Understanding shell configuration and environment variables is essential for:

* Linux System Administration
* DevOps Engineering
* Cloud Infrastructure Management
* Cybersecurity Operations

Professionals frequently customize `.bashrc` to improve productivity and automate workflows.

---

# Lab Summary

In this lab I explored the Linux user environment, examined shell configuration files, inspected environment variables, and created a permanent Bash alias using the `.bashrc` configuration file.

This lab demonstrates foundational Linux administration skills used in real-world cloud and DevOps environments.

