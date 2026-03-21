# Lab 39 - Git for Linux Administrators

## Objective

The purpose of this lab was to learn how Linux administrators use Git for version control. In this lab, I initialized a Git repository, configured Git identity, created and tracked files, staged changes, committed updates, modified files, and reviewed commit history.

This lab demonstrates a complete Git workflow used in real-world DevOps, cloud, and system administration environments.

---

## Environment

- Ubuntu Linux (Virtual Machine)
- Oracle VirtualBox
- Bash Terminal
- Windows Host Machine
- GitHub Repository
- Git version 2.43.0

---

## Commands Used (With Definitions)

mkdir -p ~/IT_Labs/02_Linux+/39_Git_for_Linux_Administrators/Screenshots  
Creates the full directory structure including parent folders if they do not exist.

cd ~/IT_Labs/02_Linux+/39_Git_for_Linux_Administrators  
Changes into the lab directory.

pwd  
Prints the current working directory to confirm correct path.

git --version  
Displays installed Git version to confirm availability.

git config --global user.name "John Keating"  
Sets global Git username.

git config --global user.email "your_email@example.com"  
Sets global Git email address.

git config --list  
Displays current Git configuration settings.

git init  
Initializes a new Git repository in the current directory.

touch README.md  
Creates an empty README.md file.

git status  
Shows repository status including untracked, staged, and modified files.

git add README.md  
Stages README.md for commit.

git commit -m "Initial commit - added README"  
Creates the first commit with a message.

git log --oneline  
Displays commit history in compact format.

echo "Git Lab File" > file1.txt  
Creates file1.txt and writes content (overwrites if exists).

git add file1.txt  
Stages file1.txt.

git commit -m "Added file1.txt"  
Commits new file to repository.

echo "Adding more content" >> file1.txt  
Appends new content to file1.txt.

git diff  
Shows line-by-line differences between working directory and last commit.

git commit -m "Updated file1.txt with more content"  
Commits updated file changes.

clear  
Clears terminal screen for readability.

---

## Command Breakdown Examples

### git init

git init

- git → Calls Git program  
- init → Initializes a repository  

Creates a hidden .git directory and enables version control.

---

### git add file1.txt

git add file1.txt

- git → Calls Git  
- add → Stages file  
- file1.txt → Target file  

Moves file from working directory to staging area.

---

### git commit -m "message"

git commit -m "Added file1.txt"

- git → Calls Git  
- commit → Saves snapshot  
- -m → Message flag  
- "message" → Commit description  

Creates a permanent snapshot with metadata and history tracking.

---

### git diff

git diff

Compares current file changes with last committed version.

Shows exactly what changed before committing.

---

## Symbols and Syntax Explained

~ → Home directory  
/ → Directory separator  
+ → Literal character in folder name  
. → Current directory  
.git → Hidden Git repository data  
README.md → Markdown file  
-p → Create parent directories  
--global → Apply setting globally  
--list → Show settings  
--version → Show program version  
--oneline → Compact log view  
-m → Commit message flag  
> → Overwrite file output  
>> → Append to file  
" " → Wrap text with spaces  
HEAD → Current commit pointer  
master → Current branch name  
100644 → Standard file permission in Git  

---

## Git Workflow Demonstrated

1. Create directory  
2. Initialize repository  
3. Configure Git identity  
4. Create README file  
5. Check status  
6. Stage file  
7. Commit changes  
8. View history  
9. Create new file  
10. Stage new file  
11. Commit new file  
12. Modify file  
13. View changes  
14. Stage modifications  
15. Commit updates  
16. Review final history  

---

## Screenshots and Explanations

Screenshot 01 - Directory Setup  
Created lab directory and confirmed location with pwd.

Screenshot 02 - Git Version  
Verified Git installation.

Screenshot 03 - Git Config  
Set and verified username and email.

Screenshot 04 - Git Init  
Initialized repository and created .git directory.

Screenshot 05 - Create README  
Created README.md file.

Screenshot 06 - Git Status (Untracked)  
Verified README.md is untracked.

Screenshot 07 - Git Add README  
Staged README.md.

Screenshot 08 - Git Status (Staged)  
Confirmed README is staged.

Screenshot 09 - First Commit  
Created initial commit.

Screenshot 10 - Git Log  
Verified commit history.

Screenshot 11 - Create file1.txt  
Created file with echo command.

Screenshot 12 - Git Status New File  
Verified file1.txt is untracked.

Screenshot 13 - Git Add file1.txt  
Staged file1.txt.

Screenshot 14 - Git Status Staged File  
Confirmed file1.txt is staged.

Screenshot 15 - Commit file1.txt  
Committed new file.

Screenshot 16 - Git Log Updated  
Verified second commit.

Screenshot 17 - Modify file  
Appended new content to file1.txt.

Screenshot 18 - Git Status Modified  
Detected modified file.

Screenshot 19 - Git Diff  
Viewed exact changes.

Screenshot 20 - Git Add Modified File  
Staged updated file.

Screenshot 21 - Commit Updated File  
Committed updated version.

Screenshot 22 - Final Git Log  
Verified full commit history.

---

## Results

Successfully completed full Git workflow including repository initialization, file tracking, staging, committing, modifying files, and reviewing commit history.

---

## Key Concepts

Repository → Git-managed directory  
Working Directory → Active files  
Staging Area → Prepared changes  
Commit → Snapshot of changes  
Tracked File → File under Git control  
Untracked File → New file not yet staged  
Modified File → Changed after commit  
Diff → Change comparison  
History → Timeline of commits  

---

## What I Learned

I learned how Git tracks changes through staging and commits, how to manage file versions, and how to inspect changes before committing. I also learned the importance of separating working changes, staged changes, and committed history.

---

## Real-World Relevance

Git is used in:

- DevOps
- Cloud Engineering
- System Administration
- Automation
- Security Operations

It allows version tracking, auditing, rollback, and team collaboration.

---

## Interview-Level Explanation

“This lab demonstrates version control using Git, including repository initialization, staging changes, committing updates, tracking file modifications, and reviewing commit history. The workflow reflects real-world DevOps and system administration practices.”

---

## Interview Notes

Why create directories in Linux VM:
The Linux VM has its own filesystem separate from Windows, so directories must exist inside the VM.

Why use git status:
It provides real-time visibility into file states and prevents mistakes.

Why use git diff:
It allows reviewing exact changes before committing to ensure accuracy.

---

## Final Status

Lab Completed Successfully