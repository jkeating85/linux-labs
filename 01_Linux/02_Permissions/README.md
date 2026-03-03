# Linux Fundamentals — File & Directory Permissions

## Objective
Demonstrate understanding of Linux file and directory permissions using `chmod`, and verify real access behavior with a separate test user.

## Environment
- Ubuntu (Virtual Machine)
- Git Bash (Windows)
- Local Linux lab environment

## Commands Used
- `ls -l` — View file permissions, owner, and group
- `ls -ld <directory>` — View directory permissions
- `chmod` — Modify file or directory permissions
- `su - <user>` — Switch users to test access
- `whoami` — Confirm current user identity

## What Was Tested

### File Permissions
- Set file permissions to `600` (owner only)
- Updated permissions to `644`
- Verified read/write access behavior

### Directory Permissions
- Set directory permissions to `700`
- Confirmed restricted access for non-owners

### Access Validation
- Tested access using a secondary user
- Confirmed permission denial
- Verified owner retains full access

## Key Takeaways
- `600` is appropriate for sensitive files (private keys, secrets)
- `644` is common for readable configuration files
- Directory permissions control the ability to enter and list contents
- Testing permissions with a separate user validates real-world behavior

## Screenshots
See the `Screenshots/` folder for visual evidence of permission changes and access validation.
