# Linux Navigation, File Management & Permissions  

---

## Table of Contents  
- [At a Glance](#at-a-glance)  
- [Filesystem Hierarchy Standard (FHS)](#filesystem-hierarchy-standard-fhs)  
- [Navigating the File System](#navigating-the-file-system)  
- [Reading File Content](#reading-file-content)  
- [Filtering Content](#filtering-content)  
- [Managing Directories & Files](#managing-directories--files)  
- [File Permissions](#file-permissions)  
- [Managing Users with sudo](#managing-users-with-sudo)  
- [Linux Help & Resources](#linux-help--resources)  
- [Key Takeaways](#key-takeaways)  
- [Glossary](#glossary)  

---

## At a Glance  
- Linux analysts must navigate, filter, and manage files **entirely via the shell**.  
- Core tasks:  
  - Navigate FHS with **pwd, ls, cd**  
  - Read file content with **cat, head, tail, less**  
  - Filter/search with **grep, pipes (|), find**  
  - Manage files/dirs with **mkdir, rmdir, touch, rm, mv, cp**  
  - Control permissions with **ls -l, chmod**  
  - Manage users with **sudo, useradd, userdel, usermod, chown**  
- Built-in help via **man, apropos, whatis** + online community.  

---

## Filesystem Hierarchy Standard (FHS)  
Defines how Linux directories & storage are organized.  

- **Root directory (/)** – highest level; all directories branch from here.  
- **Standard directories:**  
  - `/home` – user directories (e.g., `/home/analyst`). `~` = shorthand for user’s home.  
  - `/bin` – binary executables.  
  - `/etc` – system configuration files.  
  - `/tmp` – temporary files (often targeted by attackers).  
  - `/mnt` – mounted devices (USB, drives).  
- **File paths:**  
  - **Absolute path** – starts at root (`/home/analyst/projects`).  
  - **Relative path** – from current directory (`../projects`).  
  - `.` = current directory, `..` = parent directory.  

---

## Navigating the File System  

- **pwd** – prints current working directory.  
- **ls** – lists contents of a directory. Can specify another path (`ls projects`).  
- **cd** – changes directory. Accepts absolute or relative paths.  
  - Example: `cd ..` moves one level up.  

Use `whoami` to check current username.  

---

## Reading File Content  

- **cat** – displays full file content.  
- **head** – shows first 10 lines by default (`head -n 5 file.txt`).  
- **tail** – shows last 10 lines by default; useful for logs.  
- **less** – view file one page at a time; controls:  
  - `Space` = forward page  
  - `b` = back page  
  - `↑` / `↓` = line by line  
  - `q` = quit  

---

## Filtering Content  

- **grep** – search for strings inside files.  
  - `grep error server_logs.txt` → all lines containing “error”.  
- **Piping (|)** – send output of one command into another.  
  - Example: `ls /home/analyst/reports | grep users`  
- **find** – search for files/dirs by criteria.  
  - `find /home/analyst/projects -name "*log*"` → case-sensitive.  
  - `-iname` → case-insensitive.  
  - `-mtime` → modified within given days (`-mtime -3` = last 3 days).  
  - Wildcards (`*`) represent zero or more characters.  

---

## Managing Directories & Files  

- **mkdir** – create new directory.  
- **rmdir** – remove empty directory.  
- **touch** – create empty file.  
- **rm** – delete file (use with caution).  
- **mv** – move or rename files.  
- **cp** – copy files.  
- **nano** – beginner-friendly CLI text editor. Save with `Ctrl+O`, exit with `Ctrl+X`.  

**Redirection operators:**  
- `>` – overwrite file with new content.  
- `>>` – append content to file.  

---

## File Permissions  

### Structure  
Permissions = 10-character string, e.g. `drwxrwxrwx`.  

- **1st char** = file type (`d` = directory, `-` = file).  
- **Next 3** = user (owner) permissions.  
- **Next 3** = group permissions.  
- **Last 3** = others (everyone else).  

### Types of permissions  
- **r** = read  
- **w** = write  
- **x** = execute  

### Commands  
- **ls -l** – list files with permissions.  
- **ls -a** – include hidden files (those starting with `.`).  
- **chmod** – change permissions.  
  - `chmod u+rwx,g-r,o-r file.txt`  
  - `u` = user, `g` = group, `o` = others  
  - `+` = add, `-` = remove, `=` = assign exactly  

Apply **principle of least privilege** – only give required access.  

---

## Managing Users with sudo  

- **sudo** – temporarily grants elevated privileges. Safer than logging in as root.  

### Key commands  
- **useradd** – add new user.  
  - `sudo useradd researcher9`  
  - `-g` = primary group, `-G` = supplementary groups  
- **usermod** – modify existing users.  
  - `-g` = change primary group  
  - `-a -G` = append to supplementary groups  
  - `-d` = change home dir, `-l` = change login, `-L` = lock account  
- **userdel** – delete users.  
  - `sudo userdel -r username` → remove user & home directory  
- **chown** – change ownership of files.  
  - `sudo chown user file.txt`  
  - `sudo chown :group file.txt`  

---

## Linux Help & Resources  

### Community  
- **Unix & Linux Stack Exchange** – trusted Q&A forum with community-voted answers.  
- Search engines + community forums = effective troubleshooting.  

### Integrated commands  
- **man** – full manual pages (`man cat`).  
- **apropos** – search man pages for keywords (`apropos -a create new group`).  
- **whatis** – one-line description of a command (`whatis nano`).  

---

## Takeaways  

- **Navigation**: pwd, ls, cd  
- **File content**: cat, head, tail, less  
- **Filtering**: grep, pipes, find  
- **File management**: mkdir, rmdir, touch, rm, mv, cp, nano  
- **Redirection**: > (overwrite), >> (append)  
- **Permissions**: ls -l, chmod; enforce least privilege  
- **Users**: sudo with useradd, usermod, userdel, chown  
- **Help**: man, apropos, whatis + online community  

---

## Glossary  

- **Absolute file path** – full path starting from root.  
- **Argument** – input that modifies a command.  
- **Authentication** – verifying identity.  
- **Authorization** – granting access to resources.  
- **Bash** – default Linux shell.  
- **Command** – instruction to system.  
- **File path** – location of file/directory.  
- **FHS** – Filesystem Hierarchy Standard.  
- **Filtering** – selecting data based on criteria.  
- **nano** – simple command-line text editor.  
- **Options** – modify command behavior.  
- **Permissions** – read/write/execute rights for user, group, others.  
- **Principle of least privilege** – grant only required access.  
- **Relative file path** – starts from current directory.  
- **Root directory** – `/`, top of Linux hierarchy.  
- **Root user (superuser)** – elevated privileges.  
- **Standard input (stdin)** – info received by OS.  
- **Standard output (stdout)** – info returned by OS.  
- **String data** – ordered characters.  

---
