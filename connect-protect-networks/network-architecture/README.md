# Network Architecture  

---

## Table of Contents  
- [At a Glance](#at-a-glance)  
- [Network Basics](#network-basics)  
- [Common Network Devices](#common-network-devices)  
- [Cloud Computing & SDN](#cloud-computing--sdn)  
- [TCP/IP Model](#tcpip-model)  
- [OSI Model (7 Layers)](#osi-model-7-layers)  
- [IP Addressing & Packets](#ip-addressing--packets)  
- [Key Takeaways](#key-takeaways)  
- [Glossary](#glossary)  

---

## At a Glance  
- A **network** = connected devices that communicate via wired/wireless links (LAN vs WAN). 
- Core devices: **routers, switches, firewalls, modems, WAPs, servers, endpoints**. 
- **Cloud networking** uses CSPs; **SDN** virtualizes network functions for cost, reliability, and scalability. 
- **TCP/IP (4 layers)** and **OSI (7 layers)** organize how data moves; both are troubleshooting maps.   
- **IPv4/IPv6** addressing + **packet structure** matter for routing, security analysis, and detection.   

---

## Network Basics  
- **LAN**: small geographic area (home, office). **WAN**: large area (city/country/Internet). 
- Devices need **addresses** to find each other: **IP** (network location) and **MAC** (hardware ID).  
- Security analysts use **network diagrams** to visualize topology and plan defenses. (Client–server model, device roles.) 

---

## Common Network Devices  
- **Hub**: broadcasts to all ports (insecure; legacy).  
- **Switch**: forwards to destination MAC (faster, more secure; maintains MAC table).  
- **Router**: connects networks, forwards by IP, may include firewall features.  
- **Modem**: connects LAN to ISP/Internet.  
- **Wireless Access Point (WAP)**: Wi-Fi radio bridge for clients. 

- **Firewalls**: first-line filter for inbound/outbound traffic; policy-driven.  
- **Servers**: provide services (DNS, mail, file). **Clients** request/consume.  
- **Endpoints**: PCs, laptops, phones; each has **IP + MAC** and a NIC. 

---

## Cloud Computing & SDN  
- **Cloud computing**: remote servers/apps/services over the Internet (CSP-managed). Benefits: **reliability, cost, scalability**. :contentReference[oaicite:10]{index=10}  
- **Service models**: **SaaS** (apps), **PaaS** (dev platforms), **IaaS** (virtual compute/storage/network). 
- **Hybrid cloud**: on-prem + CSP; **multi-cloud**: multiple CSPs. 
- **Software-Defined Networking (SDN)**: virtual switches/routers/firewalls; quick changes via API/console; aligns with cloud scale.   

---

## TCP/IP Model  
**Purpose**: visualize how data is organized/transmitted; locate failures/attacks. Layers:   
1. **Network Access** – physical/media, frames, local delivery (cables, switches, ARP).  
2. **Internet** – IP addressing/routing between networks; ICMP for errors/diagnostics.  
3. **Transport** – **TCP** (reliable, connection-oriented) & **UDP** (fast, connectionless); ports segment traffic. 
4. **Application** – protocols/services (HTTP, SMTP, SSH, FTP, DNS). 

---

## OSI Model (7 Layers)  
A deeper, standardized view used for comms/troubleshooting: **App, Presentation, Session, Transport, Network, Data Link, Physical**. 
- **L7 Application**: User-facing protocols (HTTP/HTTPS, SMTP, DNS).  
- **L6 Presentation**: Formatting, **encryption** (e.g., SSL/TLS).  
- **L5 Session**: Session setup/teardown, checkpoints.  
- **L4 Transport**: Segmentation, flow/error control (**TCP/UDP**).  
- **L3 Network**: IP routing between networks.  
- **L2 Data Link**: Local delivery within a LAN (switches, NICs).  
- **L1 Physical**: Cables, radio, signaling.  

> Both OSI and TCP/IP help teams communicate about where issues occur; TCP/IP is a simplified mapping of OSI. 
---

## IP Addressing & Packets  
- **Packets** carry: header (addresses, protocol, size, TTL, etc.) + data + trailer/footer; bandwidth/speed anomalies can indicate attacks; **packet sniffing** inspects flows. 
- **IPv4 vs IPv6**:  
  - IPv4 = dotted decimal (e.g., 198.51.100.0), ~4.3B addresses.  
  - IPv6 = 128-bit hex, huge space, `::` shorthand; simpler header; adds **Flow Label**.  
- **Public vs Private IP**: Public from ISP (shared by your home), private used inside LAN. **MAC**: hardware ID used by switches (MAC table).

**Why packet fields matter (IPv4 header examples):** version, header length (IHL), ToS, total length, identification/flags/fragment offset, **TTL**, protocol, checksum, source/destination IP, options. Useful for routing, detection, and forensics. 

---

## Key Takeaways  
- Know **what each device does** (hub vs switch vs router vs firewall) and where it fits in a diagram. 
- **Cloud & SDN** shift hardware functions into software → faster changes, lower cost, elastic scale. 
- Use **TCP/IP & OSI** to reason about incidents and pinpoint impacted layers.   
- Understand **packets, ports, IPs, MACs** to investigate anomalies & attacks.   

---

## Glossary  
- **Bandwidth** – max data capacity (bps). 
- **Cloud computing** – remote servers/apps/services over Internet. 
- **Cloud network** – remotely hosted servers/data accessed via Internet. 
- **Data packet** – basic unit of data transfer on a network. 
- **Hub** – broadcasts frames to all ports (legacy). 
- **IP / IP address** – routing standard / unique device location.   
- **LAN / WAN** – small / large area network.   
- **MAC address** – unique hardware identifier for a NIC. 
- **Modem** – connects router/LAN to ISP.  
- **Packet sniffing** – capturing/inspecting packets on the network.  
- **Port** – software endpoint organizing traffic by service. 
- **Router** – connects networks and forwards by IP. 
- **Switch** – forwards by MAC to specific port; builds MAC table. 
- **TCP/UDP** – transport protocols (reliable vs fast). 
- **TCP/IP model** – 4-layer comms framework. 
- **OSI model** – 7-layer comms framework. 

---

