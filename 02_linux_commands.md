# Linux Command Reference Guide

This guide provides an overview of common Linux commands for beginners and intermediate users. It includes basic commands, file manipulation techniques, text processing tools, and more.

## Table of Contents
1. [Basic Commands](#basic-commands)
2. [Intermediate Commands](#intermediate-commands)
3. [File Links: Hard Links and Soft Links](#file-links-hard-links-and-soft-links)
4. [Text Processing Commands](#text-processing-commands)
5. [VI Editor](#vi-editor)
6. [Login and Remote Connection](#login-and-remote-connection)
7. [System and Disk Management](#system-and-disk-management)

---

## Basic Commands

- `date`: Displays the current date and time.
- `ls`: Lists the directories and files in the current directory.
- `mkdir directory_name`: Creates a new directory.
- `ls -l`: Lists directories and files with additional details such as permissions and timestamps.
- `pwd`: Displays the current directory's full path.
- `touch filename`: Creates a new empty file named `filename`.
- `clear`: Clears the terminal screen.
- `cd path/of/directory`: Changes the directory to the specified path.
- `cd ..`: Navigates one level up in the directory structure.
- `rm filename`: Deletes the specified file.
- `rm -r foldername`: Recursively removes the contents of a folder.
- `rmdir foldername`: Removes an empty folder.
- `echo "text to print"`: Prints the specified text to the terminal.
- `cat filename`: Displays the contents of a file.
- `echo "message" > filename`: Redirects the message to the file, creating it if necessary.
- `zcat filename`: Displays the contents of a `.zip` file.
- `head filename.txt`: Shows the first few lines of a file.
- `tail filename.txt`: Shows the last few lines of a file.
- `tail -f filename.txt`: Continuously monitors and displays new lines added to the file (e.g., logs).
- `less filename.txt`: Views the file content in a paginated manner.
- `more filename.txt`: Similar to `less`, but for larger pages.

---

## Intermediate Commands

- `cp filename.txt foldername/`: Copies a file to a folder.
  - Example: `cp devops/devops-file.txt cloud/`
- `cp -r foldername1/ foldername2/`: Recursively copies a folder to another location.
- `mv filename.txt ../foldername/`: Moves a file to another folder.
- `mv devops/ new_folder_name/`: Renames a folder.
- `wc filename.txt`: Displays the number of lines, words, and bytes in a file.
- `ls -ltr`: Lists files with more detailed information (including permissions, ownership, size, and timestamps).
- `rm file/path/filename.txt`: Removes a specific file by its path.

---

## File Links: Hard Links and Soft Links

### Hard Link
- A hard link is a direct reference to a file's inode, meaning the link will continue to exist even if the original file is deleted.
- **Command**: `ln /path/to/original/file hardlink-name`

### Soft Link (Symbolic Link)
- A soft link is a shortcut to a file. If the original file is deleted, the soft link becomes broken.
- **Command**: `ln -s /path/to/original/file softlink-name`

### Examples
- `ln -s /path/to/file/filename.txt softlink-name`: Creates a soft link for the file.
- `ln /path/to/file/filename.txt hardlink-name`: Creates a hard link for the file.

---

## Text Processing Commands

- `cut -b 1-4 filename.txt`: Extracts bytes from a file (in this case, bytes 1 to 4).
- `echo "hello" | tee newfile.txt`: Prints `hello` to the terminal and saves it in `newfile.txt`.
- `sort filename.txt`: Sorts the content of the file alphabetically.
- `diff file1.txt file2.txt`: Displays the differences between two files.

---

## VI Editor

The `vi` editor is a powerful text editor available in most Linux systems.

### Basic Commands for `vi`
- `vi filename.txt`: Opens the specified file in `vi`.
- `i`: Enter insert mode to edit the file.
- `esc`: Exits insert mode and returns to command mode.
- `:wq + enter`: Saves and exits the file, returning to the terminal.

For advanced editing, you can use `vim`, which is an improved version of `vi`.

---

## Login and Remote Connection

- **SSH (Secure Shell)**: Used to securely connect to a remote system.
  - **Public Key**: Should be stored on the remote system.
  - **Private Key**: Should be kept on the local system.
- To connect to a remote system, use the following:
  - `ssh username@hostname_or_ip`

---

## System and Disk Management

- `df`: Displays disk space usage for file systems.
- `df -h`: Shows disk space in a human-readable format.
- `du .`: Displays the disk usage of all folders in the current directory.
- `nohup command-name`: Runs a command and saves its output in a file, even if the session is closed.

---

### Notes:
- Linux commands are case-sensitive.
- Many commands have additional flags (e.g., `-r`, `-l`) that modify their behavior. Use `man <command>` (e.g., `man ls`) to view detailed documentation for any command.

