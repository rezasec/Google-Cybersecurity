# Linux Basics  

---

## Table of Contents  
- [At a Glance](#at-a-glance)  
- [Linux Architecture](#linux-architecture)  
- [Linux Distributions](#linux-distributions)  
- [Package Managers](#package-managers)  
- [The Linux Shell](#the-linux-shell)  
- [Communicating with the Shell](#communicating-with-the-shell)  
- [Key Takeaways](#key-takeaways)  
- [Glossary](#glossary)  

---

## At a Glance  
- **Linux** = open-source OS, cornerstone of cybersecurity
- Built from **GNU** (Richard Stallman) + **Linux Kernel** (Linus Torvalds).  
- Highly customizable → 600+ distributions (“distros”).  
- Analysts use Linux for:  
  - Log analysis  
  - Identity & access management  
  - Pen testing & digital forensics  
- Most work happens in the **shell** (CLI).  

---

## Linux Architecture  
Components that make up Linux
- **User**: person initiating tasks; Linux is multi-user.  
- **Applications**: programs for tasks; installed via **package managers**.  
- **Shell**: CLI interpreter, translates commands for the kernel.  
- **Filesystem Hierarchy Standard (FHS)**: organizes data (like a filing cabinet).  
- **Kernel**: manages processes, memory, and hardware drivers.  
- **Hardware**: physical components (CPU, RAM, hard drives, peripherals).  

**Hardware breakdown:**  
- **Peripheral devices** – not required to run the system (keyboard, mouse, printer).  
- **Internal hardware** – motherboard, CPU, RAM, hard drives.  
  - **CPU** – executes program instructions.  
  - **RAM** – short-term memory (data erased at shutdown).  
  - **Hard drive** – long-term storage.  

---

## Linux Distributions  
Different “flavors” of Linux, each serving a purpose
- **Kali Linux™** (Debian-based):  
  - Built for **penetration testing** & **digital forensics** 
  - Tools: **Metasploit** (exploits), **Burp Suite** (web app testing), **John the Ripper** (password cracking), **tcpdump** & **Wireshark** (traffic analysis), **Autopsy** (forensics).  
  - Best run in a **VM** for safety and rollback.  

- **Ubuntu** (Debian-based):  
  - User-friendly; includes GUI & CLI.  
  - Large community support.  
  - Common in **cloud computing**.  

- **Parrot** (Debian-based):  
  - Security-focused, pre-installed tools like Kali.  
  - Has both GUI & CLI; user-friendly.  

- **Red Hat Enterprise Linux (RHEL)**:  
  - Enterprise-focused; subscription-based with support.  

- **AlmaLinux**:  
  - Community-driven replacement for CentOS.  
  - Maintains compatibility with RHEL-based environments.  

---

## Package Managers  
- **Package** = software bundle; may include dependencies.  
- **Package Manager** = tool to install, update, and remove packages
- **Debian-based distros**:  
  - **dpkg** → `.deb` files  
  - **APT (Advanced Package Tool)** → easier CLI tool for installing/searching  
- **Red Hat-based distros**:  
  - **RPM (Red Hat Package Manager)** → `.rpm` files  
  - **YUM (Yellowdog Updater Modified)** → CLI tool for package management  
- Best practice: always install **latest versions** for security patches.  

---

## The Linux Shell  
- **Shell** = command-line interpreter
- Allows communication between user & OS.  
- Executes tasks, runs applications, enables automation.  
- Different types:  
  - **bash** (default, most popular in cybersecurity)  
  - **csh**, **ksh**, **tcsh**, **zsh** (variations, different prompts like `$` or `%`).  
- Analysts primarily use **bash**.  

---

## Communicating with the Shell  
- **Command** = instruction to the system
- Three possible responses:  
  - **Standard Input (stdin)** – user types command.  
  - **Standard Output (stdout)** – system response (e.g., `echo hello` → outputs `hello`).  
  - **Standard Error (stderr)** – error message (e.g., misspelling `echo` as `eco`).  
- Shell enables combining commands, automating tasks, and linking apps together.  

---

## Key Takeaways  
- Linux is the most widely used OS in cybersecurity.  
- Understand **Linux architecture**: user, apps, shell, FHS, kernel, hardware.  
- Be familiar with **popular distributions** (Kali, Ubuntu, Parrot, RHEL, AlmaLinux).  
- Learn how to use **package managers** and **bash shell**.  
- Master **shell communication**: input, output, errors.  

---

## Glossary  
- **Application** – program performing a task.  
- **Bash** – default, most widely used Linux shell.  
- **CentOS** – discontinued distro, replaced by AlmaLinux.  
- **CPU** – executes program instructions.  
- **Command** – instruction to computer.  
- **Digital forensics** – analyzing data post-attack.  
- **Directory** – file that organizes files.  
- **Distributions (distros)** – versions of Linux.  
- **File path** – location of a file/directory.  
- **FHS** – Filesystem Hierarchy Standard, defines storage structure.  
- **GUI** – graphical user interface.  
- **Hard drive** – long-term storage.  
- **Hardware** – physical components.  
- **Internal hardware** – required to run system (CPU, RAM, motherboard).  
- **Kali Linux™** – Debian-based distro for pen testing & forensics.  
- **Kernel** – manages processes & hardware.  
- **Linux** – open-source OS.  
- **Package** – software unit.  
- **Package Manager** – tool to install/manage packages.  
- **Parrot** – Debian-based distro for security.  
- **Pen test** – simulated attack to find vulnerabilities.  
- **Peripheral devices** – external hardware (keyboard, monitor).  
- **RAM** – short-term memory.  
- **Red Hat Enterprise Linux (RHEL)** – enterprise subscription distro.  
- **Shell** – CLI interpreter.  
- **Standard error** – error returned by

