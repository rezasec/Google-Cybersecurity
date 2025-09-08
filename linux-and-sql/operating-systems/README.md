
# Operating Systems

---

## Table of Contents  
- [At a Glance](#at-a-glance)  
- [Common Operating Systems](#common-operating-systems)  
- [OS, Applications & Hardware](#os-applications--hardware)  
- [Boot Process](#boot-process)  
- [Resource Management](#resource-management)  
- [Virtualization & VMs](#virtualization--vms)  
- [User Interfaces: GUI vs CLI](#user-interfaces-gui-vs-cli)  
- [Key Takeaways](#key-takeaways)  
- [Glossary](#glossary)  

---

## At a Glance  
- The **operating system (OS)** is the bridge between hardware and the user.  
- Popular OS: **Windows, macOS, Linux, ChromeOS, Android, iOS**.  
- The OS:  
  - Runs applications and coordinates hardware.  
  - Manages CPU, memory, and I/O resources.  
  - Provides **user interfaces** (GUI & CLI).  
- Security analysts must understand OS design, especially **legacy OS risks**, **virtualization**, and the **Linux CLI**.  

---

## Common Operating Systems  
- **Windows** – closed-source; widely used in enterprise.  
- **macOS** – partly open source (kernel open, other parts closed).  
- **Linux** – fully open source; widely used in security (e.g., Kali Linux).  
- **ChromeOS** – lightweight, partly open source; common in education.  
- **Android** – open-source mobile OS (2008).  
- **iOS** – partially open source mobile OS (2007).  

### Legacy OS  
- Outdated systems still in use due to software/hardware compatibility needs.  
- High risk: **no updates, no patches** → easy targets for attackers.  

---

## OS, Applications & Hardware  
- **User**: initiates a task (e.g., download a file).  
- **Application**: interface the user interacts with (browser, calculator).  
- **OS**: interprets the request, sends it to hardware.  
- **Hardware**: CPU, memory, storage → does the work, sends results back.  

Analogy:  
- **Restaurant** – Application = placing the order, OS = kitchen, Hardware = stove/tools, User = customer.  

---

## Boot Process  
1. **Power on** → BIOS or UEFI chip runs.  
   - **BIOS**: older systems.  
   - **UEFI**: modern replacement (post-2007), adds security.  
2. **Bootloader** runs → loads the OS.  
3. OS is ready for user tasks.  

**Security Note**: BIOS/UEFI can be attacked (antivirus often doesn’t scan firmware).  

---

## Resource Management  
- OS = **conductor of an orchestra**. Balances CPU, memory, storage, and I/O among competing processes.  
- Example: antivirus scan consumes more resources than calculator app.  
- Analysts use tools like **Task Manager** to see processes, CPU %, and memory usage.  
- Malware may consume resources → performance issues.  

---

## Virtualization & VMs  
- **Virtualization** = using software to simulate hardware.  
- **Virtual Machine (VM)** = virtual computer with its own OS, CPU, storage.  
- Benefits:  
  - **Isolation (sandboxing)** – malware in a VM won’t easily infect the host.  
  - **Efficiency** – multiple VMs share one machine’s hardware.  
- **Hypervisor** manages VMs (e.g., KVM in Linux).  
- Other forms: virtual servers, networks, and storage.  

**Risk**: Malicious code can sometimes “escape” the VM.  

---

## User Interfaces: GUI vs CLI  
- **GUI** (Graphical User Interface): icons, windows, menus. Easy for beginners. One request at a time.  
- **CLI** (Command-Line Interface): text-based, powerful, supports multiple requests.  
- CLI Advantages in Security:  
  - **Efficiency**: bulk operations (e.g., move hundreds of files fast).  
  - **History file**: logs all commands for review, auditing, and incident response.  
  - **Preferred** in cybersecurity for flexibility and traceability.  

---

## Glossary  
- **Application** – program performing a specific task.  
- **BIOS** – older firmware chip with boot instructions.  
- **Bootloader** – software that starts the OS.  
- **CLI** – command-line interface; text-based user input.  
- **GUI** – graphical user interface; icons and windows.  
- **Hardware** – physical components of a computer.  
- **Legacy OS** – outdated but still-used operating system.  
- **OS** – operating system; manages hardware, apps, users.  
- **RAM** – Random Access Memory, short-term memory for tasks.  
- **UEFI** – modern replacement for BIOS with added security.  
- **User Interface** – program that lets users control the OS.  
- **Virtual Machine (VM)** – software-based version of a physical computer.  

---
