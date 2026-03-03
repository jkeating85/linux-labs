# Linux Fundamentals — Users & Groups

## Objective
Demonstrate practical understanding of Linux user and group management, ownership, and access control using core administrative commands.

---

## Environment
- Ubuntu (Virtual Machine)
- Git Bash (Windows)
- Local Linux lab environment

---

## Commands Used & What They Do

- `whoami` — Displays the currently logged-in user.

- `id` — Shows user ID (UID), primary group ID (GID), and all group memberships.

- `cat /etc/passwd` — Displays system user account information.

- `cat /etc/group` — Displays system group information.

- `groupadd <group>` — Creates a new group.

- `useradd <user>` — Creates a new user account.

- `usermod -aG <group> <user>` — Adds an existing user to a secondary group without removing existing memberships.

- `groups <user>` — Displays all groups a user belongs to.

- `chown <user>:<group> <file>` — Changes file ownership (user and/or group).

- `ls -l` — Displays file permissions, owner, and group.

---

## What Was Tested

### User Creation
- Created a new test user
- Verified user existence in `/etc/passwd`

### Group Management
- Created a new group
- Added user to secondary group
- Verified group membership

### Ownership Changes
- Changed file ownership using `chown`
- Verified updated ownership with `ls -l`

---

## Key Concepts

- Every file has an owner (user) and an associated group.
- Each user has a primary group and may belong to multiple secondary groups.
- Group membership directly affects file and directory access.
- Ownership and permissions work together to enforce access control.

---

## Visual Evidence

See the `Screenshots/` folder for command execution and validation output.

---

## What I Learned

This lab strengthened my understanding of how Linux manages identity and access control through users and groups. I learned how ownership impacts permissions and how to validate access using system files and user inspection commands.
