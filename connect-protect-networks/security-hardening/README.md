# Network Security Hardening

---

## Table of Contents
- [At a Glance](#at-a-glance)  
- [Brute Force Attacks & OS Hardening](#brute-force-attacks--os-hardening)  
- [Network Security Applications](#network-security-applications)  
  - [Firewalls](#firewalls)  
  - [Intrusion Detection System (IDS)](#intrusion-detection-system-ids)  
  - [Intrusion Prevention System (IPS)](#intrusion-prevention-system-ips)  
  - [Full Packet Capture](#full-packet-capture)  
  - [Security Information & Event Management (SIEM)](#security-information--event-management-siem)  
- [Secure the Cloud](#secure-the-cloud)  
- [Cryptography & Cloud Security](#cryptography--cloud-security)  
- [Glossary](#glossary)

---

## At a Glance
- **Goal:** Reduce attack surface and strengthen systems, networks, and cloud through **hardening**.  
- **Focus Areas:**  
  - OS hardening (patches, password policies, authentication)  
  - Network hardening (firewalls, IDS/IPS, SIEM, layered defense)  
  - Cloud hardening (IAM, baselines, cryptography, shared responsibility)  
- **Why:** To block common attacks like brute force, DoS/DDoS, and IP spoofing, while limiting impact if attackers succeed.

---

## Brute Force Attacks & OS Hardening
- **Definition:** Trial-and-error attempts to guess login credentials.  
- **Types:**  
  - *Simple brute force* → manual guessing of usernames/passwords.  
  - *Dictionary attacks* → use lists of common/stolen passwords.  
- **Tools used by attackers:** Automated scripts and software for speed.  

### Assessing vulnerabilities
- **Virtual Machines (VMs):**  
  - Isolated environments for testing malware or suspicious apps.  
  - Can snapshot/restore previous states.  
  - Small risk of VM escape, but useful for safe analysis.  
- **Sandboxes:**  
  - Execute software safely away from production.  
  - Test patches, detect bugs, simulate attacks.  
  - Some malware hides behavior if it detects a VM/sandbox.

### Prevention Measures
- **Hashing + Salting:** Protects passwords in storage.  
- **MFA/2FA:** Extra authentication factors.  
- **CAPTCHA / reCAPTCHA:** Blocks bots from brute forcing.  
- **Password policies:** Define complexity, rotation, reuse limits, login attempt limits.

---

## Network Security Applications

### Firewalls
- Allow/deny traffic using rules (IP/port).  
- **NGFWs:** Inspect packet payloads, block based on applications.  
- Every host should also have its own firewall.

### Intrusion Detection System (IDS)
- Monitors traffic for **signatures or anomalies**.  
- **Alerts only**, doesn’t block.  
- Placed **behind the firewall** to reduce false positives.

### Intrusion Prevention System (IPS)
- Detects and **blocks malicious traffic inline**.  
- Drops suspect packets or blocks sender.  
- Risks: false positives and inline failures could disrupt connectivity.

### Full Packet Capture
- Records all network traffic.  
- Helps analyze alerts, detect patterns, and investigate intrusions.

### Security Information & Event Management (SIEM)
- Collects and aggregates logs from multiple sources (firewalls, IDS, IPS, VPNs, DNS).  
- Provides **real-time dashboards** for monitoring.  
- Example tools: Chronicle (Google Cloud), Splunk Enterprise/Cloud.  
- SIEMs **don’t stop threats directly**, but centralize detection for analysts.

---

## Secure the Cloud

### Key Challenges
- **IAM:** Misconfigured user roles = major risk.  
- **Configuration drift:** More services → higher misconfiguration risk.  
- **Attack surface:** More apps/services → more entry points.  
- **Zero-days:** CSPs can patch hypervisors faster than most on-prem setups.  
- **Visibility:** Logs and packet mirroring replace full traffic inspection.  
- **Rapid change:** CSP updates require adapting configs quickly.

### Shared Responsibility Model
- **CSP responsibility:** Infrastructure (data centers, hypervisors, host OS).  
- **Customer responsibility:** Configurations, applications, and data.  
- **Risk:** Customers sometimes assume CSP handles more than they actually do.

---

## Cryptography & Cloud Security

### Cloud Hardening Tools
- **IAM:** Secure identity management and least-privilege access.  
- **Hypervisors:** Managed by CSP, but vulnerabilities can allow VM escapes.  
- **Baselining:** Reference configurations for security (e.g., encrypted files, threat detection enabled).  

### Cryptography
- **Encryption:** Protects data in transit and at rest. Relies on secure keys.  
- **Cryptographic erasure (crypto-shredding):** Destroying keys = data permanently unreadable.  
- **Key management:**  
  - *TPM:* Hardware chip to store keys/certs locally.  
  - *CloudHSM:* Dedicated hardware module for managing keys in cloud.  
  - Customers may supply their own keys; CSPs protect infra but not customer keys.

---

## Glossary
- **Baseline configuration:** Reference build used to compare changes.  
- **Brute force attack:** Trial-and-error method to guess passwords.  
- **CAPTCHA:** Test to block automated bots.  
- **Firewall:** Device/ruleset filtering traffic.  
- **IDS/IPS:** IDS = detect; IPS = detect + block.  
- **MFA/2FA:** Multiple factors to verify user identity.  
- **Patch update:** Fix for vulnerabilities in OS/apps.  
- **Sandbox:** Isolated environment for testing code.  
- **Security hardening:** Strengthening systems against attacks.  
- **SIEM:** Centralized log/event analysis tool.  
- **VM escape:** Exploit where malicious code breaks out of a VM to access the host.  
- **World-writable file:** File editable by anyone, a major risk.

