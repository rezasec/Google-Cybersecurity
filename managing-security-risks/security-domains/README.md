# Security Domains  

---

## Table of Contents  
- [At a Glance](#at-a-glance)  
- [CISSP’s Eight Security Domains](#cissps-eight-security-domains)  
  - [1. Security and Risk Management](#1-security-and-risk-management)  
  - [2. Asset Security](#2-asset-security)  
  - [3. Security Architecture & Engineering](#3-security-architecture--engineering)  
  - [4. Communication & Network Security](#4-communication--network-security)  
  - [5. Identity & Access Management (IAM)](#5-identity--access-management-iam)  
  - [6. Security Assessment & Testing](#6-security-assessment--testing)  
  - [7. Security Operations](#7-security-operations)  
  - [8. Software Development Security](#8-software-development-security)  
- [Threats, Risks, and Vulnerabilities](#threats-risks-and-vulnerabilities)  
- [Ransomware & the Web Layers](#ransomware--the-web-layers)  
- [Risk Management](#risk-management)  
- [NIST Risk Management Framework (RMF)](#nist-risk-management-framework-rmf)  
- [Key Takeaways](#key-takeaways)  
- [Glossary](#glossary)  

---

## At a Glance  

- Security is split into **8 CISSP domains**.  
- Core ideas: **security posture**, least privilege, shared responsibility, defense in depth.  
- **Threat ≠ Risk ≠ Vulnerability** → keep these separate.  
- Common problems: insider threats, phishing, ransomware, outdated systems.  
- **Risk management**: accept, avoid, transfer, mitigate.  
- **NIST RMF**: 7 key steps.  

---

## CISSP’s Eight Security Domains  

### 1. Security and Risk Management  
- Builds overall **security posture**.  
- Includes risk mitigation, compliance, continuity, and ethics.  
- **Example**: Updating data handling for GDPR.  

### 2. Asset Security  
- Protects digital + physical assets.  
- Backup and recovery = critical.  
- **Example**: Restoring systems from secure backups.  

### 3. Security Architecture & Engineering  
- Focus: secure design of systems.  
- Key principles: **least privilege, defense in depth, zero trust**.  
- **Example**: SIEM alerts on unusual logins.  

### 4. Communication & Network Security  
- Secures on-site, remote, and cloud networks.  
- VPNs + segmentation protect remote workers.  

### 5. Identity & Access Management (IAM)  
- Ensures proper authentication + authorization.  
- Based on **least privilege**.  
- **Example**: Granting temporary access for customer support reps.  

### 6. Security Assessment & Testing  
- Finds weaknesses through testing + audits.  
- Methods: pen testing, control testing, audits.  
- **Example**: Reviewing user permissions.  

### 7. Security Operations  
- Handles **incident response** and daily defense.  
- Tools: SIEM, logging, playbooks, forensics.  
- **Example**: Investigating suspicious after-hours access.  

### 8. Software Development Security  
- Security must be built into the **SDLC**.  
- Secure coding + QA prevent flaws.  
- **Example**: Checking encryption in medical software.  

---

## Threats, Risks, and Vulnerabilities  

### Threats  
- **Insider threats**: abuse of access.  
- **APTs**: long-term hidden access.  
- **Phishing**: tricking users into revealing info.  
- **Ransomware**: encrypts data, demands payment.  

### Risks  
- Chance + impact of a threat on **CIA** (confidentiality, integrity, availability).  
- Examples:  
  - **External** (hackers), **Internal** (employees/vendors).  
  - **Legacy systems**: old, unpatched systems still online.  
  - **Third-party risks**: vendor access to sensitive data.  

### Vulnerabilities  
- Weaknesses attackers exploit.  
- Examples: ProxyLogon, ZeroLogon, Log4Shell, PetitPotam.  
- Poor logging = blind spots.  

---

## Ransomware & the Web Layers  

- **Ransomware**: locks data → ransom for decryption key.  
- Often spreads via phishing or unpatched systems.  

**Web layers:**  
1. **Surface web**: normal public sites.  
2. **Deep web**: private logins (intranets, databases).  
3. **Dark web**: hidden networks, often used for illegal data sales.  

**Impacts:** financial loss, identity theft, reputation damage.  

---

## Risk Management  

### Strategies  
- Accept, Avoid, Transfer, Mitigate.  

### Frameworks  
- **NIST RMF** → main framework.  
- **HITRUST** → healthcare.  
- **OWASP Top 10** → biggest web app risks.  

---

## NIST Risk Management Framework (RMF)  

Steps (memorize order):  
1. Prepare  
2. Categorize  
3. Select  
4. Implement  
5. Assess  
6. Authorize  
7. Monitor  

---

## Key Takeaways  

- **8 CISSP domains** cover all security areas.  
- Always separate **threats, risks, vulnerabilities**.  
- **RMF** gives a step-by-step way to handle risk.  
- Security is ongoing and requires shared responsibility.  

---

## Glossary  

- **Security posture**: overall defense strength.  
- **Least privilege**: minimum access needed.  
- **Zero trust**: never trust, always verify.  
- **SIEM**: tool for monitoring logs/events.  
- **Risk mitigation**: reducing likelihood/impact.  
- **CIA triad**: confidentiality, integrity, availability.  
- **NIST RMF**: 7-step risk management framework.  

---
