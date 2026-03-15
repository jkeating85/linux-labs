Lab 01 – Linux Navigation

Objective
Practice and demonstrate core Linux navigation commands to understand how the Linux file system is structured and how to efficiently move through directories using the command line.

Environment
- Ubuntu (Virtual Machine)
- Git Bash (Windows)
- Local Linux lab environment

Commands Used & What They Do

pwd
Print Working Directory – Displays your current directory path

ls
List – Shows files and directories in the current location

ls -la
List All – Shows all files (including hidden files) with detailed permissions, ownership, and timestamps

cd
Change Directory – Move into a specified directory

cd ..
Move Up – Navigate to the parent directory

cd ~
Home – Return to the user’s home directory

mkdir
Make Directory – Create a new folder

rmdir
Remove Directory – Delete an empty folder


Key Concepts Demonstrated
- Understanding the Linux hierarchical file system
- Difference between absolute and relative paths
- Directory traversal using cd
- Viewing hidden files with ls -la
- Creating and removing directories
- Using tab completion for efficiency
- Basic command-line workflow


Example Workflow

mkdir linux_lab
cd linux_lab
mkdir level_one
cd level_one
pwd
ls -la
cd ..
rmdir level_one


What I Learned
This lab strengthened my understanding of how Linux organizes files and directories within a hierarchical structure. I learned how to efficiently navigate the file system using relative and absolute paths, inspect directory contents, and manage folders directly from the command line.

Mastering these foundational navigation skills is essential for system administration, DevOps workflows, cloud engineering, and security operations.
