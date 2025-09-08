# Securing Networks from Attacks

## Table of Contents
1. [How Intrusions Compromise Systems](#how-intrusions-compromise-systems)  
2. [Network Interception Attacks](#network-interception-attacks)  
   - [Packet Sniffing](#packet-sniffing)  
   - [On-Path Attacks](#on-path-attacks)  
   - [Replay Attacks](#replay-attacks)  
   - [Smurf Attacks](#smurf-attacks)  
   - [Denial of Service (DoS) Attacks](#denial-of-service-dos-attacks)  
3. [Backdoor Attacks](#backdoor-attacks)  
4. [Impacts on Organizations](#impacts-on-organizations)  
5. [tcpdump and Packet Analysis](#tcpdump-and-packet-analysis)  
   - [Key tcpdump Fields](#key-tcpdump-fields)  
   - [Uses of tcpdump](#uses-of-tcpdump)  
6. [Real-life DDoS Attack (2016 DNS Attack)](#real-life-ddos-attack-2016-dns-attack)  
7. [Glossary](#glossary)  

---

## How Intrusions Compromise Systems
- All networks have **inherent vulnerabilities**.  
- Attackers can be motivated by **financial gain, political/activist goals, or insider threats**.  
- Security analysts must **detect vulnerabilities early** and respond quickly.

---

## Network Interception Attacks
Network interception attacks steal or manipulate data in transit.

### Packet Sniffing
- Capturing and inspecting packets across a network.  
- **Passive sniffing**: quietly monitoring traffic.  
- **Active sniffing**: intercepting or altering packets.  
- Tools: **Wireshark, tcpdump**.  
- **Defense**: encryption (TLS/SSL, VPNs), secured Wi-Fi, NGFW monitoring.

### On-Path Attacks
- Attacker places themselves “in the middle” of communication between two trusted parties.  
- Can steal **usernames, passwords, or DNS lookups**.  
- Defense: **encrypt traffic in transit** (TLS).

### Replay Attacks
- Malicious actor intercepts a packet, delays it, or resends it later.  
- Often used to **replay login credentials**.  
- Defense: time-based tokens, session IDs, encryption.

### Smurf Attacks
- Uses **IP spoofing + ICMP floods**.  
- Spoofed packets sent to broadcast address trigger massive ICMP responses.  
- Effect: **overloads servers → denial of service**.  
- Defense: **NGFWs** that detect and block unusual broadcast traffic.

### Denial of Service (DoS) Attacks
- Flooding a server with packets until it can’t respond to legitimate traffic.  
- **DDoS (Distributed DoS)**: uses botnets to amplify the attack.  
- Defense: rate limiting, load balancing, DDoS mitigation services.

---

## Backdoor Attacks
- **Backdoor** = hidden method to bypass normal authentication.  
- May be left intentionally by developers/admins or created by attackers.  
- Used for **persistent access** after compromise.  
- Attackers can install malware, perform DoS, or disable defenses.

---

## Impacts on Organizations
- **Financial**: downtime, ransomware, recovery costs, lawsuits.  
- **Reputation**: loss of public trust, customer churn.  
- **Public Safety**: threats to critical infrastructure (power, water, defense systems).  

---

## tcpdump and Packet Analysis
`tcpdump` = lightweight, command-line packet analyzer (preinstalled on many Linux distros).

### Key tcpdump Fields
- **Timestamp** – time packet was captured.  
- **Source IP / Source Port** – where the packet originated.  
- **Destination IP / Destination Port** – where the packet is going.  

### Uses of tcpdump
- Monitor and troubleshoot network issues.  
- Detect suspicious/malicious traffic.  
- Establish baseline patterns of network use.  
- Create custom alerts.  
- Attackers may also use tcpdump to steal sensitive data.

---

## Real-life DDoS Attack (2016 DNS Attack)
- On **October 21, 2016**, a major DNS provider was targeted.  
- Attackers used a **botnet** to flood the DNS service with millions of requests.  
- Result: websites relying on that DNS provider went offline (North America + Europe).  
- Recovery: DNS services restored within 2 hours, later attacks mitigated.  
- Demonstrated the **disruptive power of DDoS attacks**.

---

## Glossary
- **Packet Sniffing**: Capturing/inspecting data packets on a network.  
- **IP Spoofing**: Faking the source IP address of packets to impersonate a trusted device.  
- **On-Path Attack**: Attacker intercepts communications between trusted systems.  
- **Replay Attack**: Capturing and resending legitimate packets at another time.  
- **Smurf Attack**: DoS using spoofed ICMP floods to a broadcast address.  
- **DoS/DDoS**: Flooding systems to prevent legitimate use.  
- **tcpdump**: Command-line packet analyzer.  
- **Botnet**: Network of malware-infected devices controlled by attackers.

---
