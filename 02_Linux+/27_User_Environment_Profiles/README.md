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

## Screenshots

### Screenshot 01 — Home Directory
File: Screenshots/01_home_directory.png

Explanation:
This screenshot shows the user's Linux home directory. The home directory is the default working directory for a user account and stores personal files, configuration files, and user-specific data.


### Screenshot 02 — Hidden User Files
File: Screenshots/02_hidden_user_files.png

Command Used:
ls -a

Explanation:
This screenshot shows hidden files in the user's home directory. Files that begin with a dot (`.`) are hidden configuration files. Examples include `.bashrc`, `.profile`, and `.config`. These files control user environment settings and shell behavior.


### Screenshot 03 — Top of .bashrc File
File: Screenshots/03_bashrc_top.png

Command Used:
nano ~/.bashrc

Explanation:
This screenshot shows the top portion of the `.bashrc` file opened in the Nano text editor. The `.bashrc` file contains Bash shell configuration settings that run automatically when a new terminal session starts.


### Screenshot 04 — Bottom of .bashrc File
File: Screenshots/04_bashrc_bottom.png

Explanation:
This screenshot shows the bottom section of the `.bashrc` file. This area typically contains user-defined settings such as aliases, environment variables, and custom shell configurations.


### Screenshot 05 — .profile Contents
File: Screenshots/05_profile_contents.png

Command Used:
nano ~/.profile

Explanation:
This screenshot shows the `.profile` file contents. The `.profile` file is another shell configuration file that runs when a user logs into a system. It is commonly used to initialize environment variables and startup programs.


### Screenshot 06 — Environment Variables (Top)
File: Screenshots/06_environment_variables_top.png

Command Used:
printenv

Explanation:
This screenshot displays the top section of environment variables printed by the `printenv` command. Environment variables store system information such as the current user, home directory, shell type, language settings, and terminal configuration.


### Screenshot 07 — Environment Variables (Bottom)
File: Screenshots/07_environment_variables_bottom.png

Command Used:
printenv

Explanation:
This screenshot shows the continuation of environment variables displayed by `printenv`. These variables control how programs and the operating system behave during a user session.


### Screenshot 08 — PATH Variable
File: Screenshots/08_path_variable.png

Command Used:
echo $PATH

Explanation:
This screenshot shows the PATH environment variable. The PATH variable contains directories separated by colons (`:`). When a command is typed in the terminal, Linux searches these directories to locate the executable program.


### Screenshot 09 — Alias Test
File: Screenshots/09_alias_test.png

Command Used:
alias ll='ls -lah'

Explanation:
This screenshot shows the creation and testing of a command alias. An alias creates a shortcut command. In this case, the alias `ll` runs the command `ls -lah`, which displays a detailed directory listing including hidden files.


### Screenshot 10 — Editing .bashrc (Top)
File: Screenshots/10_bashrc_edit_top.png

Command Used:
nano ~/.bashrc

Explanation:
This screenshot shows the `.bashrc` file being edited in the Nano text editor. The alias command was added to this file so it will load automatically whenever a new terminal session starts.


### Screenshot 11 — Editing .bashrc (Bottom)
File: Screenshots/11_bashrc_edit_bottom.png

Explanation:
This screenshot shows the bottom section of the `.bashrc` file where the alias was added. Adding the alias here makes the shortcut permanent for the user.


### Screenshot 12 — Alias Loaded After Reloading Bash
File: Screenshots/12_alias_loaded_after_bashrc.png

Commands Used:
source ~/.bashrc  
ll

Explanation:
This screenshot shows the Bash configuration being reloaded using `source ~/.bashrc`. After reloading the configuration, the `ll` alias works successfully and displays a detailed directory listing. This confirms the alias was correctly saved in `.bashrc`.

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

