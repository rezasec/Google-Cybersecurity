# Security Frameworks & Controls  

---

## Table of Contents  
- [At a Glance](#at-a-glance)  
- [Frameworks vs Controls](#frameworks-vs-controls)  
- [Cybersecurity Frameworks](#cybersecurity-frameworks)  
  - [Cyber Threat Framework (CTF)](#cyber-threat-framework-ctf)  
  - [ISO/IEC 27001](#isoiec-27001)  
- [Security Controls](#security-controls)  
- [CIA Triad](#cia-triad)  
  - [Confidentiality](#confidentiality)  
  - [Integrity](#integrity)  
  - [Availability](#availability)  
- [OWASP Security Principles](#owasp-security-principles)  
- [Security Audits](#security-audits)  
- [Key Takeaways](#key-takeaways)  
- [Glossary](#glossary)  

---

## At a Glance  

- **Frameworks** = guidelines for managing risk + compliance.  
- **Controls** = safeguards to reduce threats (physical, technical, admin).  
- **CIA Triad** = confidentiality, integrity, availability → core of security posture.  
- **OWASP Principles** = best practices for reducing risks in daily security work.  
- **Audits** = independent reviews of controls/policies to ensure compliance + remediation.  

---

## Frameworks vs Controls  

- **Frameworks** = high-level guidelines to align with laws/standards (e.g., NIST CSF, ISO/IEC 27001).  
- **Controls** = specific safeguards to reduce threats (e.g., MFA, firewalls, CCTV).  
- Example: HIPAA (framework for healthcare) → MFA (control) ensures compliance.  

---

## Cybersecurity Frameworks  

### Cyber Threat Framework (CTF)  
- Developed by U.S. government.  
- Provides **common language** for describing/sharing cyber threat activity.  
- Helps analysts communicate, compare, and respond to evolving threats.  

### ISO/IEC 27001  
- Internationally recognized standard for **information security management systems (ISMS)**.  
- Covers protecting assets like financial info, IP, employee data, 3rd-party data.  
- Outlines requirements + best practices. Provides a catalog of controls but doesn’t mandate specific ones.  

---

## Security Controls  

Controls reduce risk by **preventing, detecting, or correcting** issues.  

- **Physical**: gates, locks, guards, CCTV, access badges.  
- **Technical**: firewalls, MFA, antivirus, encryption.  
- **Administrative**: separation of duties, authorization, asset classification, policies.  

---

## CIA Triad  

Framework for evaluating security posture.  

### Confidentiality  
- Only authorized users can access data.  
- Enforced via **least privilege** + access restrictions.  

### Integrity  
- Data must be correct, authentic, and reliable.  
- Achieved through **cryptography** and **encryption**.  

### Availability  
- Data must be accessible to authorized users when needed.  
- Example: remote workers accessing internal networks with proper controls.  

---

## OWASP Security Principles  

Key security practices used daily by analysts:  
- **Minimize attack surface** → fewer entry points = fewer risks.  
- **Least privilege** → only necessary access.  
- **Defense in depth** → multiple layers of security.  
- **Separation of duties** → critical actions split across people.  
- **Keep it simple** → avoid unnecessary complexity.  
- **Fix correctly** → remediate root causes, not just symptoms.  

Additional OWASP principles:  
- **Secure defaults** → systems/apps should default to safest settings.  
- **Fail securely** → if a control fails, it should fail in the most secure state.  
- **Don’t trust services** → verify 3rd-party systems, don’t assume safety.  
- **Avoid security by obscurity** → don’t rely on secrecy (e.g., hidden code) for security.  

---

## Security Audits  

**Definition**: Independent reviews of controls, policies, and procedures against internal standards + external regulations.  

### Goals  
- Ensure IT/security practices meet standards.  
- Identify gaps + remediation needs.  
- Avoid penalties for noncompliance.  

### Factors Affecting Audits  
- Industry type  
- Org size  
- Government regulations  
- Geographic location  
- Business decisions (voluntary compliance)  

### Audit Process  
1. **Scope** → list assets, policies, controls to review.  
2. **Risk assessment** → evaluate risks tied to budget, processes, regulations.  
3. **Conduct audit** → test security of assets/controls.  
4. **Mitigation plan** → reduce risks and outline fixes.  
5. **Communicate results** → detailed report with findings + compliance gaps.  

### Role of Frameworks in Audits  
- Frameworks (e.g., NIST CSF, ISO 27000) prepare organizations for audits.  
- Controls support compliance with frameworks and regulations.  

---

## Key Takeaways  

- Frameworks give the **structure**, controls provide the **actions**.  
- CIA triad is central to designing secure systems.  
- OWASP principles = practical rules for daily security tasks.  
- Audits keep organizations accountable and aligned with compliance standards.  

---

## Glossary  

- **Asset** → item of value to an org (data, hardware, IP).  
- **Authentication** → verifying identity.  
- **Authorization** → granting access to resources.  
- **Availability** → data accessible to authorized users.  
- **Biometrics** → physical traits for authentication.  
- **Confidentiality** → only authorized users can access data.  
- **Integrity** → data correctness + reliability.  
- **CIA Triad** → confidentiality, integrity, availability.  
- **Encryption** → encoding data to block unauthorized access.  
- **NIST CSF** → framework of standards/guidelines to manage risk.  
- **NIST SP 800-53** → detailed controls for U.S. gov systems.  
- **OWASP** → nonprofit improving software security.  
- **Security audit** → review of controls/policies vs expectations.  
- **Security controls** → safeguards (physical, technical, admin).  
- **Security frameworks** → guidelines for managing risks/compliance.  
- **Security posture** → org’s ability to defend and respond.  
- **Threat** → event/circumstance that can harm assets.  
- **Risk** → impact to CIA if threat occurs.  

---
