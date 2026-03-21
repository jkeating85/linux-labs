# Lab 39 - Git for Linux Administrators

---

## 📌 Objective

The purpose of this lab was to learn how Linux administrators use Git for version control.

In this lab, I:
- Initialized a Git repository
- Configured Git identity
- Created and tracked files
- Staged changes
- Committed updates
- Modified files
- Reviewed commit history

This lab demonstrates a complete Git workflow used in real-world DevOps, cloud, and system administration environments.

---

## 🖥️ Environment

- Ubuntu Linux (Virtual Machine)
- Oracle VirtualBox
- Bash Terminal
- Windows Host Machine
- GitHub Repository
- Git version 2.43.0

---

<<<<<<< HEAD
## ⚙️ Commands Used (With Definitions)

```bash
mkdir -p ~/IT_Labs/02_Linux+/39_Git_for_Linux_Administrators/Screenshots
```
Creates the full directory structure, including parent folders if they do not exist.

```bash
cd ~/IT_Labs/02_Linux+/39_Git_for_Linux_Administrators
```
Changes into the lab directory.

```bash
pwd
```
Prints the current working directory to confirm correct path.

```bash
git --version
```
Displays installed Git version to confirm availability.

```bash
git config --global user.name "John Keating"
```
Sets global Git username.

```bash
git config --global user.email "your_email@example.com"
```
Sets global Git email address.

```bash
git config --list
```
Displays current Git configuration settings.

```bash
git init
```
Initializes a new Git repository in the current directory.

```bash
touch README.md
```
Creates an empty README.md file.

```bash
git status
```
Shows repository status including untracked, staged, and modified files.

```bash
git add README.md
```
Stages README.md for commit.

```bash
git commit -m "Initial commit - added README"
```
Creates the first commit with a message.

```bash
git log --oneline
```
Displays commit history in compact format.

```bash
echo "Git Lab File" > file1.txt
```
Creates file1.txt and writes content (overwrites if exists).

```bash
git add file1.txt
```
Stages file1.txt.

```bash
git commit -m "Added file1.txt"
```
Commits new file to repository.

```bash
echo "Adding more content" >> file1.txt
```
Appends new content to file1.txt.

```bash
git diff
```
Shows line-by-line differences between working directory and last commit.

```bash
git commit -m "Updated file1.txt with more content"
```
Commits updated file changes.

```bash
clear
```
Clears terminal screen for readability.

---

=======
## 🧰 Commands Used (With Definitions)

---

### 📁 Directory Setup
```bash
mkdir -p ~/IT_Labs/02_Linux+/39_Git_for_Linux_Administrators/Screenshots
cd ~/IT_Labs/02_Linux+/39_Git_for_Linux_Administrators
pwd
```
- Creates full directory structure (including parent folders if needed)  
- Navigates into lab directory  
- Confirms current working path  

---

### ⚙️ Git Installation & Configuration
```bash
git --version
git config --global user.name "John Keating"
git config --global user.email "your_email@example.com"
git config --list
```
- Verifies Git is installed  
- Sets global username for commit authorship  
- Sets global email for tracking commits  
- Displays current Git configuration  

---

### 🗂️ Repository Initialization
```bash
git init
touch README.md
```
- Initializes a new Git repository and creates `.git` directory  
- Creates an empty README.md file  

---

### 📊 File Tracking & Commits
```bash
git status
git add README.md
git commit -m "Initial commit - added README"
git log --oneline
```
- Displays file tracking status (untracked, staged, modified)  
- Stages README.md for commit  
- Creates first commit snapshot  
- Shows commit history in compact format  

---

### 📄 File Creation & Versioning
```bash
echo "Git Lab File" > file1.txt
git add file1.txt
git commit -m "Added file1.txt"
```
- Creates new file and writes content (overwrites if exists)  
- Stages new file  
- Commits file to repository  

---

### ✏️ File Modification & Change Tracking
```bash
echo "Adding more content" >> file1.txt
git diff
git add file1.txt
git commit -m "Updated file1.txt with more content"
```
- Appends new content without overwriting  
- Displays exact changes before committing  
- Stages modified file  
- Commits updated version  

---

### 🧹 Terminal Management
```bash
clear
```
- Clears terminal output for better readability  

---

>>>>>>> b2cdd9f8f340799f35adc25805200ce30ff6a4c4
## 🔍 Command Breakdown Examples

### git init

```bash
git init
```

- `git` → Calls Git program  
- `init` → Initializes a repository  

Creates a hidden `.git` directory and enables version control.

---

### git add file1.txt

```bash
git add file1.txt
```

- `git` → Calls Git  
- `add` → Stages file  
- `file1.txt` → Target file  

Moves file from working directory to staging area.

---

### git commit -m "message"

```bash
git commit -m "Added file1.txt"
```

- `git` → Calls Git  
- `commit` → Saves snapshot  
- `-m` → Message flag  
- `"message"` → Commit description  

Creates a permanent snapshot with metadata and history tracking.

---

### git diff

```bash
git diff
```

Compares current file changes with last committed version.

Shows exactly what changed before committing.

---

## 🧩 Symbols and Syntax Explained

| Symbol | Meaning |
|------|--------|
| `~` | Home directory |
| `/` | Directory separator |
| `+` | Literal character in folder name |
| `.` | Current directory |
| `.git` | Hidden Git repository data |
| `README.md` | Markdown file |
| `-p` | Create parent directories |
| `--global` | Apply setting globally |
| `--list` | Show settings |
| `--version` | Show program version |
| `--oneline` | Compact log view |
| `-m` | Commit message flag |
| `>` | Overwrite file output |
| `>>` | Append to file |
| `" "` | Wrap text with spaces |
| `HEAD` | Current commit pointer |
| `master/main` | Current branch |
| `100644` | Standard file permission in Git |

---

## 🔄 Git Workflow Demonstrated

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

## 📸 Screenshots and Explanations

<<<<<<< HEAD
### Screenshot 01 — Directory Setup  
Created the lab directory and verified the working path using `pwd`. This confirms correct navigation within the Linux filesystem.

### Screenshot 02 — Git Version  
Verified Git is installed and accessible. This ensures the environment is properly prepared for version control operations.

### Screenshot 03 — Git Config  
Configured global username and email. These values are embedded in commits for tracking authorship.

### Screenshot 04 — Git Init  
Initialized a new Git repository. This created the hidden `.git` directory that enables version tracking.

### Screenshot 05 — Create README  
Created the README.md file. This file serves as documentation for the repository.

### Screenshot 06 — Git Status (Untracked)  
Verified that README.md appears as untracked. Git recognizes the file but is not yet tracking it.

### Screenshot 07 — Git Add README  
Staged README.md. This moves the file into the staging area.

### Screenshot 08 — Git Status (Staged)  
Confirmed README.md is staged and ready to be committed.

### Screenshot 09 — First Commit  
Created the initial commit. This establishes the first snapshot in version history.

### Screenshot 10 — Git Log  
Displayed commit history using `git log --oneline`. Shows commit hash and message.

### Screenshot 11 — Create file1.txt  
Created a new file and added initial content using `echo`.

### Screenshot 12 — Git Status New File  
Verified file1.txt appears as untracked.

### Screenshot 13 — Git Add file1.txt  
Staged file1.txt for commit.

### Screenshot 14 — Git Status Staged File  
Confirmed file1.txt is staged and ready for commit.

### Screenshot 15 — Commit file1.txt  
Committed file1.txt to the repository, creating a new snapshot.

### Screenshot 16 — Git Log Updated  
Verified the second commit appears in history.

### Screenshot 17 — Modify File  
Appended new content to file1.txt using `>>`.

### Screenshot 18 — Git Status Modified  
Detected that file1.txt is modified after changes.

### Screenshot 19 — Git Diff  
Displayed exact line-by-line changes before committing.

### Screenshot 20 — Git Add Modified File  
Staged updated file after modifications.

### Screenshot 21 — Commit Updated File  
Committed updated version of file1.txt.

### Screenshot 22 — Final Git Log  
Verified full commit history, confirming all changes were successfully tracked.

---

## 📊 Results

Successfully completed a full Git workflow including:
- Repository initialization
- File tracking
- Staging changes
- Committing updates
- Modifying files
- Reviewing commit history

---

## 🧠 Key Concepts

- Repository → Git-managed directory  
- Working Directory → Active files  
- Staging Area → Prepared changes  
- Commit → Snapshot of changes  
- Tracked File → File under Git control  
- Untracked File → New file not yet staged  
- Modified File → Changed after commit  
- Diff → Change comparison  
- History → Timeline of commits  

---

## 🎯 What I Learned

I learned how Git tracks changes through staging and commits, how to manage file versions, and how to inspect changes before committing.

I also learned the importance of separating:
- Working directory changes  
- Staged changes  
- Committed history  

---

=======
### Screenshot 01 — Directory Setup
![Screenshot 01](Screenshots/01_lab_directory_setup.png)

Created the lab directory and verified the working path using `pwd`. This confirms correct navigation within the Linux filesystem and ensures all commands are executed in the intended directory.

---

### Screenshot 02 — Git Version
![Screenshot 02](Screenshots/02_git_version_check.png)

Verified Git is installed and accessible. This confirms the system is ready for version control operations and avoids issues later in the workflow.

---

### Screenshot 03 — Git Config
![Screenshot 03](Screenshots/03_git_configuration.png)

Configured global username and email. These values are embedded into commits and are critical for tracking authorship in collaborative environments.

---

### Screenshot 04 — Git Init
![Screenshot 04](Screenshots/04_git_init.png)

Initialized a new Git repository. This created the hidden `.git` directory, which stores all version control metadata and enables Git tracking.

---

### Screenshot 05 — Create README
![Screenshot 05](Screenshots/05_create_readme.png)

Created the `README.md` file. This file serves as documentation for the repository and is typically the first file tracked in any project.

---

### Screenshot 06 — Git Status (Untracked)
![Screenshot 06](Screenshots/06_git_status_untracked.png)

Verified that `README.md` appears as untracked. Git recognizes the file exists but is not yet tracking it.

---

### Screenshot 07 — Git Add README
![Screenshot 07](Screenshots/07_git_add_readme.png)

Staged `README.md`. This moves the file from the working directory into the staging area, preparing it for commit.

---

### Screenshot 08 — Git Status (Staged)
![Screenshot 08](Screenshots/08_git_status_staged.png)

Confirmed that `README.md` is staged and ready to be committed.

---

### Screenshot 09 — First Commit
![Screenshot 09](Screenshots/09_git_commit.png)

Created the initial commit. This establishes the first snapshot in the repository’s history.

---

### Screenshot 10 — Git Log
![Screenshot 10](Screenshots/10_git_log.png)

Displayed commit history using `git log --oneline`, showing commit hashes and messages in a compact format.

---

### Screenshot 11 — Create file1.txt
![Screenshot 11](Screenshots/11_create_file1.png)

Created a new file (`file1.txt`) and added initial content using the `echo` command.

---

### Screenshot 12 — Git Status New File
![Screenshot 12](Screenshots/12_git_status_new_file.png)

Verified that `file1.txt` appears as an untracked file.

---

### Screenshot 13 — Git Add file1.txt
![Screenshot 13](Screenshots/13_git_add_file1.png)

Staged `file1.txt`, preparing it to be committed.

---

### Screenshot 14 — Git Status After Add
![Screenshot 14](Screenshots/14_git_status_after_add.png)

Confirmed that `file1.txt` is staged and ready for commit.

---

### Screenshot 15 — Commit file1.txt
![Screenshot 15](Screenshots/15_git_commit_file1.png)

Committed `file1.txt`, creating a new snapshot in the repository.

---

### Screenshot 16 — Git Log (Two Commits)
![Screenshot 16](Screenshots/16_git_log_two_commits.png)

Verified that the repository now contains multiple commits, showing version history progression.

---

### Screenshot 17 — Modify File
![Screenshot 17](Screenshots/17_modify_file1.png)

Modified `file1.txt` by appending new content using `>>`, demonstrating file updates.

---

### Screenshot 18 — Git Status Modified File
![Screenshot 18](Screenshots/18_git_status_modified_file.png)

Detected that `file1.txt` is modified but not yet staged.

---

### Screenshot 19 — Git Diff Output
![Screenshot 19](Screenshots/19_git_diff_output.png)

Displayed exact line-by-line changes using `git diff`. This is critical for reviewing changes before committing.

---

### Screenshot 20 — Git Add Modified File
![Screenshot 20](Screenshots/20_git_add_modified_file.png)

Staged the modified version of `file1.txt`.

---

### Screenshot 21 — Commit Updated File
![Screenshot 21](Screenshots/21_git_commit_updated_file.png)

Committed the updated file, adding another version snapshot to history.

---

### Screenshot 22 — Final Git Log
![Screenshot 22](Screenshots/22_git_log_final.png)

Verified the complete commit history, confirming all changes were successfully tracked and recorded.

---

## 📊 Results

Successfully completed a full Git workflow including:
- Repository initialization
- File tracking
- Staging changes
- Committing updates
- Modifying files
- Reviewing commit history

---

## 🧠 Key Concepts

- Repository → Git-managed directory  
- Working Directory → Active files  
- Staging Area → Prepared changes  
- Commit → Snapshot of changes  
- Tracked File → File under Git control  
- Untracked File → New file not yet staged  
- Modified File → Changed after commit  
- Diff → Change comparison  
- History → Timeline of commits  

---

## 🎯 What I Learned

I learned how Git tracks changes through staging and commits, how to manage file versions, and how to inspect changes before committing.

I also learned the importance of separating:
- Working directory changes  
- Staged changes  
- Committed history  

---

>>>>>>> b2cdd9f8f340799f35adc25805200ce30ff6a4c4
## 🌍 Real-World Relevance

Git is used in:
- DevOps
- Cloud Engineering
- System Administration
- Automation
- Security Operations

It enables:
- Version tracking
- Auditing
- Rollbacks
- Team collaboration

---

## 🧑‍💼 Interview-Level Explanation

“This lab demonstrates version control using Git, including repository initialization, staging changes, committing updates, tracking file modifications, and reviewing commit history. The workflow reflects real-world DevOps and system administration practices.”

---

## 🧾 Interview Notes

**Why create directories in Linux VM:**  
The Linux VM has its own filesystem separate from Windows, so directories must be created inside the Linux environment.

**Why use git status:**  
Provides real-time visibility into file states and prevents committing unintended changes.

**Why use git diff:**  
Allows reviewing exact changes before committing, ensuring accuracy and preventing errors.

---

## ✅ Final Status

Lab Completed Successfully
