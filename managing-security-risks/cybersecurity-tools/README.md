# Introduction to Cybersecurity Tools  

---

## Table of Contents  
- [At a Glance](#at-a-glance)  
- [Logs and SIEM](#logs-and-siem)  
  - [Firewall Logs](#firewall-logs)  
  - [Network Logs](#network-logs)  
  - [Server Logs](#server-logs)  
- [SIEM Tools](#siem-tools)  
  - [Splunk Dashboards](#splunk-dashboards)  
  - [Chronicle Dashboards](#chronicle-dashboards)  
- [Future of SIEM](#future-of-siem)  
- [Open-Source vs Proprietary Tools](#open-source-vs-proprietary-tools)  
  - [Linux](#linux)  
  - [Suricata](#suricata)  
- [Key Takeaways](#key-takeaways)  
- [Glossary](#glossary)  

---

## At a Glance  

- **Logs** are records of system/network events → essential for security monitoring.  
- **SIEM tools** (e.g., Splunk, Chronicle) collect + analyze logs, provide dashboards, and support incident response.  
- **Future of SIEM**: cloud-native, AI/ML, automation (SOAR).  
- **Open-source tools** (Linux, Suricata) are free, customizable, widely used.  
- **Proprietary tools** (Splunk, Chronicle) are vendor-owned and paid but polished and scalable.  

---

## Logs and SIEM  

Logs are central to monitoring threats, risks, and vulnerabilities.  

### Firewall Logs  
- Track traffic allowed/denied by rules.  
- Identify unusual activity (e.g., repeated failed login attempts).  

### Network Logs  
- Capture network activity (IP addresses, devices).  
- Useful for spotting abnormal traffic (e.g., spikes in bandwidth use).  

### Server Logs  
- Track activity on apps, databases, OS.  
- Provide visibility into unauthorized access or configuration issues.  

---

## SIEM Tools  

**SIEM (Security Information and Event Management)** = collects and correlates logs across systems, supports real-time monitoring, alerts, dashboards.  

### Splunk Dashboards  
- **Security posture** → last 24h of notable events + trends.  
- **Executive summary** → overall health, high-level metrics for stakeholders.  
- **Incident review** → visual timeline of incident events for investigation.  
- **Risk analysis** → changes in user/computer/IP activity to prioritize risks.  

### Chronicle Dashboards  
- **Enterprise insights** → suspicious domains/IOCs with severity + confidence.  
- **Data ingestion & health** → verifies logs are being received correctly.  
- **IOC matches** → top domain/IP/device threats over time.  
- **Main dashboard** → timeline view of events (failed logins, spikes).  
- **Rule detections** → lists recurring high-severity detections.  
- **User sign-in overview** → unusual user activity (e.g., logins from 2 countries).  

---

## Future of SIEM  

- Moving to **cloud-hosted** and **cloud-native** environments.  
- **Cloud-native** = full use of cloud advantages (scalability, flexibility).  
- Growth of **IoT** = larger attack surface, more logs to manage.  
- Integration of **AI/ML** → better detection, visualization, anomaly spotting.  
- **SOAR** (Security Orchestration, Automation, and Response): automates common responses, freeing analysts for complex issues.  
- Expectation: more interconnectivity between platforms + streamlined incident handling.  

---

## Open-Source vs Proprietary Tools  

### Open-Source Tools  
- Free, customizable, source code available.  
- Community-driven → quick bug fixes, more transparency.  
- Misconception: less secure — in reality, wide visibility often makes them safer.  

**Linux**  
- Open-source OS.  
- Used widely in cybersecurity due to flexibility + CLI tools.  
- Basis for many security labs and exercises.  

**Suricata**  
- Open-source network analysis + threat detection.  
- Developed by OISF.  
- Inspects network traffic, detects suspicious IP/user behavior, integrates with SIEM.  

### Proprietary Tools  
- Owned/maintained by vendors, typically paid.  
- Limited customization but often polished with support/training.  
- Examples: Splunk, Google Chronicle.  

---

## Key Takeaways  

- Logs are the foundation of monitoring threats and vulnerabilities.  
- SIEM tools centralize logs, provide dashboards, and support incident detection/response.  
- SIEM is evolving toward **cloud-native, automated, AI-enhanced platforms**.  
- Both open-source (Linux, Suricata) and proprietary (Splunk, Chronicle) tools are valuable.  
- Analysts must stay current with tool advancements (cloud, AI, SOAR).  

---

## Glossary  

- **Chronicle** → Google’s cloud-native SIEM tool.  
- **Incident response** → detecting, containing, correcting effects of a breach.  
- **Log** → record of system or network events.  
- **Metrics** → technical attributes used to measure performance (uptime, errors).  
- **Operating System (OS)** → interface between hardware and user.  
- **Playbook** → manual of operational/security actions.  
- **SIEM** → tool that collects, analyzes, correlates log data for threat detection.  
- **SOAR** → automation of security responses to incidents.  
- **Splunk Cloud** → vendor-hosted SIEM service.  
- **Splunk Enterprise** → self-hosted SIEM deployment.  

---

