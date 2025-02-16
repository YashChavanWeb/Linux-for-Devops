# Linux Commands and System Management Cheat Sheet

## System Information Commands

### 1. `who`
- Displays information about who is logged in to the system.
  - Example: `who`
  - Output: Lists users, login times, and terminal information.

### 2. `whoami`
- Shows the current logged-in user's name.
  - Example: `whoami`
  - Output: The username of the current user.

### 3. `which`
- Displays the location of a command or program.
  - Example: `which bash`
  - Output: Shows the path of the command or executable (e.g., `/bin/bash`).

### 4. `id`
- Provides user and group information.
  - Example: `id`
  - Output: Displays the user's ID, group ID, and group memberships.

---

## Superuser and Permissions

### 1. `sudo`
- **Super User Do**: Used to execute commands with superuser (root) privileges.
  - `sudo` allows normal users to perform administrative tasks.
  - Example: `sudo shutdown` (Shutdown the system)
  - Example: `sudo apt install docker.io` (Install software)

---

## Package Management (APT)

- **`apt`**: Package management tool used for installing and removing software.
  
  ### Update Package List:
  ```bash
  sudo apt-get update
  ```

  ### Install Software:
  ```bash
  sudo apt-get install docker.io
  ```

  ### Remove Software:
  ```bash
  sudo apt-get remove docker.io
  ```

---

## User and Group Management

### 1. Add a User
```bash
sudo useradd -m username
```
- `-m` flag creates the user's home directory.

### 2. Set Password for User
```bash
sudo passwd username
```

### 3. Switch to Another User
```bash
su username
```

### 4. Return to Primary User
```bash
exit
```

### 5. List Users
```bash
cat /etc/passwd
```

### 6. Delete a User
```bash
sudo userdel username
```

---

### Groups

#### 1. Create a Group
```bash
sudo groupadd groupname
```

#### 2. View Groups
```bash
cat /etc/group
```

#### 3. Add User to a Group

- For a single user:
  ```bash
  sudo gpasswd -a username groupname
  ```

- For multiple users:
  ```bash
  sudo gpasswd -M user1,user2 groupname
  ```

#### 4. Delete a Group
```bash
sudo groupdel groupname
```

---

## File Permissions

### File Permission Format (e.g., `drwxrwxr-x`)
- **d**: Directory
- **r**: Read
- **w**: Write
- **x**: Execute

| Permission | Value |
|------------|-------|
| ---        | 0     |
| --x        | 1     |
| -w-        | 2     |
| -wx        | 3     |
| r--        | 4     |
| r-x        | 5     |
| rw-        | 6     |
| rwx        | 7     |

### 1. View File Permissions
```bash
ls -l
```

### 2. Modify File Permissions (`chmod`)
- **Example**: Give full permissions to a folder:
  ```bash
  chmod 777 folder_name
  ```

### 3. Umask
- Sets default permissions for new files.
  - Default value: `0002`

### 4. Change Ownership (`chown`)
- Changes file or directory ownership.
  ```bash
  chown user_2 file.txt
  ```

### 5. Change Group Ownership (`chgrp`)
- Changes file or directory group.
  ```bash
  chgrp group_name file.txt
  ```

---

## Compression Commands

### 1. Install `zip` Utility
```bash
sudo apt install zip
```

### 2. Zip a Folder
```bash
zip zip_file_name foldername
```

### 3. Unzip a File
```bash
unzip zip_file_name.zip
```

### 4. Tar Compression

- Compress a folder:
  ```bash
  tar -cvzf folder_name.tar.gz folder_name
  ```

- Extract a tar file:
  ```bash
  tar -xvzf folder_name.tar.gz
  ```

---

## File Transfer Commands

### 1. `scp` (Secure Copy Protocol)
- Used to copy files between local and remote systems securely.
  
  **Syntax**:
  ```bash
  scp -i "path/to/key.pem" filename.txt username@remote_host:/path/to/destination
  ```
  Example:
  ```bash
  scp -i "my_key.pem" file.txt user@192.168.1.1:/home/user/
  ```

### 2. `rsync`
- Sync files and directories between local and remote systems.
  - More efficient than `scp` because it only transfers changed files.
  
  **Example**:
  ```bash
  rsync -avz source/ user@remote_host:/path/to/destination
  ```

---

## Notes on `sudo`

- The **root user** (or superuser) has all system privileges.
- Other users can perform administrative tasks using `sudo`.
- `sudo` is typically used for:
  - Installing and managing software.
  - Modifying system files and configurations.
  - Changing ownership or permissions of protected files.

---

## Additional Notes

- The **`apt`** package manager is used on **Debian-based systems** (e.g., Ubuntu).
- Other package managers include:
  - **Yum**: Used on Red Hat-based systems.
  - **Portage**: Used on Gentoo-based systems.

By mastering these commands, you can manage Linux systems, users, file permissions, and software packages efficiently.
