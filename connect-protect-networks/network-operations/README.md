# Network Operations  

---

## Table of Contents  
- [At a Glance](#at-a-glance)  
- [Common Network Protocols](#common-network-protocols)  
- [Additional Protocols (NAT, DHCP, ARP, Telnet, SSH, Email)](#additional-protocols-nat-dhcp-arp-telnet-ssh-email)  
- [Wireless Security: WEP → WPA2 → WPA3](#wireless-security-wep--wpa2--wpa3)  
- [Subnetting & CIDR](#subnetting--cidr)  
- [Virtual Networks & Privacy (Firewalls, Proxies, VPN, SD-WAN)](#virtual-networks--privacy-firewalls-proxies-vpn-sd-wan)  
- [VPN Protocols: WireGuard vs IPSec](#vpn-protocols-wireguard-vs-ipsec)  
- [Ports Quick Reference](#ports-quick-reference)  
- [Key Takeaways](#key-takeaways)  
- [Glossary](#glossary)  

---

## At a Glance  
- **Protocols** are the rules for how data moves; grouped as **communication**, **management**, and **security**.  
- **NAT, DHCP, ARP, Telnet/SSH, POP3/IMAP/SMTP** are must-know building blocks for analysts.  
- **Wi-Fi security** evolved from weak **WEP** → **WPA/WPA2** (AES/CCMP) → **WPA3** (SAE, stronger crypto).  
- **Subnetting/CIDR**: segment networks for performance, manageability, and security zones.  
- **Firewalls (stateless/stateful/NGFW)**, **proxies**, **VPNs**, and **SD-WAN** secure modern operations.  
- **VPN protocols**: **WireGuard** (simple/fast) vs **IPSec** (mature/widely supported).  

---

## Common Network Protocols  
**Communication**  
- **TCP** – reliable, connection-oriented (3-way handshake: SYN → SYN/ACK → ACK).  
- **UDP** – connectionless, faster, used when low latency matters (e.g., DNS queries).  
- **HTTP** (80) – web communication; **HTTPS** (443) = HTTP + TLS encryption.  
- **DNS** (UDP 53; TCP 53 for large replies) – resolves names ⇄ IPs.

**Management**  
- **SNMP** – monitor/manage devices (e.g., config, bandwidth stats).  
- **ICMP** – error/status reporting; tools like `ping` and `traceroute`.

**Security**  
- **HTTPS** – encrypted web traffic (TLS).  
- **SFTP** – file transfers over **SSH** (TCP 22); uses strong encryption (e.g., AES).  

> Note: Encryption hides contents, not metadata (source/destination IPs remain visible).

---

## Additional Protocols (NAT, DHCP, ARP, Telnet, SSH, Email)  
- **NAT** – translates many private IPs to a single public IP at the edge (router/firewall).  
- **DHCP** – auto-assigns IP, DNS, gateway (Server **UDP 67** / Client **UDP 68**).  
- **ARP** – maps IP ⇄ MAC within a LAN (layer 2; no port).  
- **Telnet** (TCP 23) – remote CLI **in clear text** (legacy; avoid).  
- **SSH** (TCP 22) – secure remote shell/tunneling; preferred over Telnet.  
- **POP3** – retrieve email (TCP/UDP **110**; **995** with SSL/TLS).  
- **IMAP** – sync/read email on server (TCP **143**; **993** with SSL/TLS).  
- **SMTP** – send/relay email (TCP/UDP **25** unencrypted; **587** with TLS).

---

## Wireless Security: WEP → WPA2 → WPA3  
- **WEP (1999)** – legacy; weak encryption; high risk.  
- **WPA (2003)** – interim fix; TKIP, integrity check; still vulnerable (e.g., KRACK).  
- **WPA2 (2004)** – **AES/CCMP**; standard for years; KRACK exposed handshake weakness.  
  - **Personal** – shared passphrase (home/small).  
  - **Enterprise** – centralized auth; per-user control; users don’t hold keys.  
- **WPA3 (2018)** – **SAE** handshake, stronger default crypto (128-bit; **192-bit** optional in Enterprise), mitigates KRACK-style attacks.

---

## Subnetting & CIDR  
- **Subnetting** = splitting a network into smaller logical **subnets** for performance and security zones.  
- **CIDR** notation: `198.51.100.0/24` covers `198.51.100.0–198.51.100.255`.  
- Benefits: smaller broadcast domains, cleaner routing tables, easier isolation (DMZ/controlled/restricted zones).

---

## Virtual Networks & Privacy (Firewalls, Proxies, VPN, SD-WAN)  
**Firewalls**  
- **Stateless** – rule-based; doesn’t track sessions (rules needed both directions).  
- **Stateful** – tracks sessions (state table); return traffic allowed automatically.  
- **NGFW** – adds deep packet inspection, IPS, app awareness, malware sandboxing, URL/DNS filtering.

**Proxies**  
- **Forward proxy** – clients → Internet (policy/filtering, NAT).  
- **Reverse proxy** – Internet → internal services (offload, shielding, policy).  

**VPNs**  
- **Encrypts** data in transit; **encapsulation** creates a protected tunnel; hides user’s public IP.  
- Used by orgs for secure access to internal apps/servers; individuals for privacy.  
- **SD-WAN** pairs with VPN to securely connect users/apps across many sites with policy-driven routing.

---

## VPN Protocols: WireGuard vs IPSec  
- **WireGuard** – newer, open source, lightweight codebase → high performance, simpler setup; supports site-to-site & client-server.  
- **IPSec** – mature, widely supported by OSes and gear; strong crypto/auth; more complex to configure; common for site-to-site.  
- **Choice depends on**: performance, compatibility, operational simplicity, and org requirements.

---

## Ports Quick Reference  
| Protocol | Port(s) | Notes |
|---|---|---|
| HTTP | 80 | Insecure web |
| HTTPS | 443 | Web with TLS |
| DNS | 53 UDP/TCP | Name resolution |
| DHCP | 67/68 UDP | Server/Client |
| SSH | 22 TCP | Secure remote shell/SFTP |
| Telnet | 23 TCP | Insecure remote shell (legacy) |
| POP3 | 110 / 995 | Unencrypted / SSL/TLS |
| IMAP | 143 / 993 | Unencrypted / SSL/TLS |
| SMTP | 25 / 587 | Unencrypted / TLS submission |

---

## Key Takeaways  
- Know **what protocol does what**, **where it lives** in TCP/IP, and **which port(s)** it uses.  
- Prefer **secure** replacements: **HTTPS** over HTTP, **SSH/SFTP** over Telnet/FTP.  
- **WPA3 > WPA2 > WPA** > WEP; use **Enterprise mode** for business networks.  
- **Subnetting + CIDR** improve performance and enable **security zones**.  
- Modern defenses blend **NGFW**, **proxies**, **VPN**, and **SD-WAN** to reduce risk and improve reliability.  

---

## Glossary  
- **ARP** – Maps IP to MAC inside a LAN.  
- **Cloud-based firewall** – Firewall hosted by a CSP.  
- **Controlled zone** – Subnet protecting internal network from the uncontrolled zone.  
- **DNS** – Resolves domain names to IP addresses.  
- **Encapsulation** – Wrapping data inside another packet (e.g., VPN tunneling).  
- **Firewall** – Filters traffic entering/leaving a network.  
- **Forward proxy** – Client-side intermediary to the Internet.  
- **HTTP/HTTPS** – Web protocols (HTTPS adds TLS).  
- **IEEE 802.11** – Wi-Fi standards family.  
- **Network protocols** – Rules for data format, order, and handling across networks.  
- **Network segmentation** – Dividing networks into security/performance zones.  
- **Port filtering** – Allow/block traffic based on port numbers.  
- **Proxy server** – Forwards client requests to other servers (forward/reverse).  
- **Reverse proxy** – Internet-facing intermediary for internal services.  
- **SFTP** – Secure file transfer over SSH.  
- **SSH** – Secure remote shell/tunnel protocol.  
- **SNMP** – Monitor/manage network devices.  
- **Stateful/Stateless** – Firewall session-tracking vs rule-only filtering.  
- **Subnetting** – Splitting a network into smaller subnets.  
- **TCP** – Reliable, connection-oriented transport.  
- **Uncontrolled zone** – Portion of network outside the org.  
- **VPN** – Encrypted tunnel; hides IP, protects data in transit.  
- **WPA** – Wi-Fi security protocol family (WEP → WPA → WPA2 → WPA3).  

---

