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

- **CISSP’s Eight Security Domains**: Organize cybersecurity work into 8 categories (risk management, asset security, architecture, networks, IAM, testing, operations, software security).  
- **Key Concepts**: Security posture, InfoSec, least privilege, shared responsibility, defense in depth.  
- **Threats, Risks, Vulnerabilities**: Threat = harmful event, Risk = likelihood/impact, Vulnerability = weakness exploited by threats.  
- **Common Issues**: Insider threats, APTs, outdated systems, misconfigurations, phishing, ransomware.  
- **Risk Management**: Handled using strategies (accept, avoid, transfer, mitigate) and frameworks like **NIST RMF**.  
- **NIST RMF**: 7 steps (Prepare, Categorize, Select, Implement, Assess, Authorize, Monitor).  
- **Takeaway**: Security is continuous, proactive, and shared across teams.  

---

## CISSP’s Eight Security Domains  

### 1. Security and Risk Management  
- Builds an organization’s **security posture**: ability to defend and respond to change.  
- Key elements:  
  - Security goals & objectives  
  - Risk mitigation processes  
  - Compliance with regulations  
  - Business continuity & disaster recovery  
  - Legal and ethical requirements  
- **InfoSec**: processes to secure information (incident response, vulnerability management, app/cloud/infrastructure security).  
- **Example**: Adjusting how PII is treated to comply with GDPR.  

### 2. Asset Security  
- Protects **digital and physical assets**: PII, servers, desktops, office space, etc.  
- Covers storage, maintenance, retention, destruction.  
- Tools: backups, recovery plans, impact analysis.  
- **Example**: Creating backups to restore data after an incident.  

### 3. Security Architecture & Engineering  
- Ensures systems, tools, and processes protect assets effectively.  
- **Principles**: shared responsibility, threat modeling, least privilege, defense in depth, fail securely, separation of duties, simplicity, zero trust, trust but verify.  
- **Example**: Using SIEM tools to flag unusual logins.  

### 4. Communication & Network Security  
- Secures **physical and wireless networks** (on-site, remote, cloud).  
- Remote/hybrid work = higher exposure to insecure connections.  
- Mitigation: VPNs, restricted network access, segmentation.  
- **Example**: Restricting risky public Wi-Fi access for remote workers.  

### 5. Identity & Access Management (IAM)  
- Ensures only authorized users have proper access.  
- Core concept: **principle of least privilege**.  
- Components: Identification → Authentication → Authorization → Accountability.  
- **Example**: Granting temporary access for customer service reps, then revoking it.  

### 6. Security Assessment & Testing  
- Identifies and mitigates risks, threats, vulnerabilities.  
- Methods: penetration testing, control testing, security audits, log analysis.  
- **Example**: Auditing user permissions to ensure proper levels of access.  

### 7. Security Operations  
- Handles **incident response and prevention**.  
- Tools & processes: training, awareness, intrusion detection, SIEM, logging, playbooks, forensics, lessons learned.  
- **Example**: Investigating abnormal after-hours data access.  

### 8. Software Development Security  
- Integrates security into the **software development life cycle (SDLC)**.  
- Secure coding, testing, QA, pen testing.  
- Security must be built into every stage (design → release).  
- **Example**: Ensuring encryption is configured properly in a medical device.  

---

## Threats, Risks, and Vulnerabilities  

### Definitions  
- **Threat**: Event/circumstance that could harm assets.  
- **Risk**: Likelihood + impact of a threat affecting confidentiality, integrity, or availability.  
- **Vulnerability**: Weakness that can be exploited by a threat.  

### Common Threats  
- **Insider threats**: Abusing authorized access.  
- **Advanced persistent threats (APTs)**: Long-term unauthorized access.  
- **Phishing/social engineering**: Trick users into revealing sensitive info.  
- **Ransomware**: Encrypts data and demands payment for decryption.  

### Common Risks  
- **External risks**: Threat actors outside the org.  
- **Internal risks**: Employees, vendors, or trusted partners.  
- **Legacy systems**: Outdated hardware/software still in use.  
- **Multiparty risks**: Third-party vendors with access to data.  
- **Software compliance**: Outdated or noncompliant applications.  

### Common Vulnerabilities  
- **ProxyLogon**: Exploits Microsoft Exchange.  
- **ZeroLogon**: Exploits Microsoft Netlogon protocol.  
- **Log4Shell**: Runs malicious Java code remotely.  
- **PetitPotam**: Exploits Windows NTLM.  
- **Security logging failures**: Inadequate monitoring lets attacks go unnoticed.  
- **Server-side request forgery**: Manipulates server apps to access backend resources.  

---

## Ransomware & the Web Layers  

- **Ransomware**: Encrypts data, locks systems, demands payment for decryption key.  
- Delivered via phishing, malicious downloads, or exploited vulnerabilities.  
- Negotiations and leaked data often occur on the **dark web**.  

### Web Layers  
1. **Surface web**: Publicly accessible (search engines, websites).  
2. **Deep web**: Requires authorization (intranets, private databases).  
3. **Dark web**: Requires special tools (e.g., Tor); often used for illicit activity.  

### Impacts of Threats  
- **Financial**: Downtime, fixes, fines.  
- **Identity theft**: Stolen PII sold/leaked.  
- **Reputation damage**: Loss of trust, bad press, customer loss.  

---

## Risk Management  

### Strategies  
- **Acceptance**: Live with the risk if cost of mitigation > impact.  
- **Avoidance**: Eliminate the risk source.  
- **Transference**: Shift risk to a third party (e.g., insurance, outsourcing).  
- **Mitigation**: Reduce likelihood or impact.  

### Frameworks  
- **NIST RMF** (Risk Management Framework).  
- **HITRUST** (healthcare-focused).  
- **OWASP** (publishes Top 10 critical web risks).  

---

## NIST Risk Management Framework (RMF)  

1. **Prepare**: Plan ahead, identify risks and controls.  
2. **Categorize**: Define risk management processes/tasks based on CIA (confidentiality, integrity, availability).  
3. **Select**: Choose and document controls (e.g., playbooks).  
4. **Implement**: Put security/privacy plans into action.  
5. **Assess**: Verify controls are effective.  
6. **Authorize**: Take accountability, generate reports, plan of action.  
7. **Monitor**: Continuously track system performance and risks.  

---

## Key Takeaways  

- Security work is organized into **domains** for clarity and structure.  
- **Threats, risks, vulnerabilities** are distinct but interconnected.  
- **Risk management** is proactive and strategic, using frameworks like NIST RMF.  
- Security must be **continuous and embedded** in systems, operations, and software development.  
- Cybersecurity is a **shared responsibility** across teams, not just analysts.  

---

## Glossary  

- **Assess**: Determine if controls are implemented correctly (Step 5, NIST RMF).  
- **Authorize**: Being accountable for risks that may exist (Step 6, NIST RMF).  
- **Business continuity**: Organization’s ability to keep running after disruptions.  
- **Categorize**: Define processes/tasks for risk management (Step 2, NIST RMF).  
- **External threat**: Harm from outside actors.  
- **Implement**: Apply security/privacy plans (Step 4, NIST RMF).  
- **Internal threat**: Harm from employees, vendors, or trusted partners.  
- **Monitor**: Track systems to ensure risks are minimized (Step 7, NIST RMF).  
- **Prepare**: Plan actions to manage risks before a breach (Step 1, NIST RMF).  
- **Ransomware**: Attack that encrypts data and demands payment.  
- **Risk**: Anything impacting confidentiality, integrity, or availability of an asset.  
- **Risk mitigation**: Procedures/rules to reduce risk impact.  
- **Security posture**: Organization’s ability to defend assets and respond to change.  
- **Select**: Choose and document controls (Step 3, NIST RMF).  
- **Shared responsibility**: Everyone plays a role in reducing risk.  
- **Social engineering**: Manipulating humans to gain unauthorized access.  
- **Vulnerability**: Weakness that can be exploited by a threat.  

---

