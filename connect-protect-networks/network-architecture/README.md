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
- A **network** = connected devices that communicate via wired/wireless links (LAN vs WAN). :contentReference[oaicite:0]{index=0}  
- Core devices: **routers, switches, firewalls, modems, WAPs, servers, endpoints**. :contentReference[oaicite:1]{index=1}  
- **Cloud networking** uses CSPs; **SDN** virtualizes network functions for cost, reliability, and scalability. :contentReference[oaicite:2]{index=2}  
- **TCP/IP (4 layers)** and **OSI (7 layers)** organize how data moves; both are troubleshooting maps.   
- **IPv4/IPv6** addressing + **packet structure** matter for routing, security analysis, and detection.   

---

## Network Basics  
- **LAN**: small geographic area (home, office). **WAN**: large area (city/country/Internet). :contentReference[oaicite:5]{index=5}  
- Devices need **addresses** to find each other: **IP** (network location) and **MAC** (hardware ID). :contentReference[oaicite:6]{index=6}  
- Security analysts use **network diagrams** to visualize topology and plan defenses. (Client–server model, device roles.) :contentReference[oaicite:7]{index=7}  

---

## Common Network Devices  
- **Hub**: broadcasts to all ports (insecure; legacy).  
- **Switch**: forwards to destination MAC (faster, more secure; maintains MAC table).  
- **Router**: connects networks, forwards by IP, may include firewall features.  
- **Modem**: connects LAN to ISP/Internet.  
- **Wireless Access Point (WAP)**: Wi-Fi radio bridge for clients. :contentReference[oaicite:8]{index=8}  

- **Firewalls**: first-line filter for inbound/outbound traffic; policy-driven.  
- **Servers**: provide services (DNS, mail, file). **Clients** request/consume.  
- **Endpoints**: PCs, laptops, phones; each has **IP + MAC** and a NIC. :contentReference[oaicite:9]{index=9}  

---

## Cloud Computing & SDN  
- **Cloud computing**: remote servers/apps/services over the Internet (CSP-managed). Benefits: **reliability, cost, scalability**. :contentReference[oaicite:10]{index=10}  
- **Service models**: **SaaS** (apps), **PaaS** (dev platforms), **IaaS** (virtual compute/storage/network). :contentReference[oaicite:11]{index=11}  
- **Hybrid cloud**: on-prem + CSP; **multi-cloud**: multiple CSPs. :contentReference[oaicite:12]{index=12}  
- **Software-Defined Networking (SDN)**: virtual switches/routers/firewalls; quick changes via API/console; aligns with cloud scale.   

---

## TCP/IP Model  
**Purpose**: visualize how data is organized/transmitted; locate failures/attacks. Layers: :contentReference[oaicite:14]{index=14}  
1. **Network Access** – physical/media, frames, local delivery (cables, switches, ARP).  
2. **Internet** – IP addressing/routing between networks; ICMP for errors/diagnostics.  
3. **Transport** – **TCP** (reliable, connection-oriented) & **UDP** (fast, connectionless); ports segment traffic. :contentReference[oaicite:15]{index=15}  
4. **Application** – protocols/services (HTTP, SMTP, SSH, FTP, DNS). :contentReference[oaicite:16]{index=16}  

---

## OSI Model (7 Layers)  
A deeper, standardized view used for comms/troubleshooting: **App, Presentation, Session, Transport, Network, Data Link, Physical**. Highlights: :contentReference[oaicite:17]{index=17}  
- **L7 Application**: User-facing protocols (HTTP/HTTPS, SMTP, DNS).  
- **L6 Presentation**: Formatting, **encryption** (e.g., SSL/TLS).  
- **L5 Session**: Session setup/teardown, checkpoints.  
- **L4 Transport**: Segmentation, flow/error control (**TCP/UDP**).  
- **L3 Network**: IP routing between networks.  
- **L2 Data Link**: Local delivery within a LAN (switches, NICs).  
- **L1 Physical**: Cables, radio, signaling.  

> Both OSI and TCP/IP help teams communicate about where issues occur; TCP/IP is a simplified mapping of OSI. :contentReference[oaicite:18]{index=18}  

---

## IP Addressing & Packets  
- **Packets** carry: header (addresses, protocol, size, TTL, etc.) + data + trailer/footer; bandwidth/speed anomalies can indicate attacks; **packet sniffing** inspects flows. :contentReference[oaicite:19]{index=19}  
- **IPv4 vs IPv6**:  
  - IPv4 = dotted decimal (e.g., 198.51.100.0), ~4.3B addresses.  
  - IPv6 = 128-bit hex, huge space, `::` shorthand; simpler header; adds **Flow Label**. :contentReference[oaicite:20]{index=20}  
- **Public vs Private IP**: Public from ISP (shared by your home), private used inside LAN. **MAC**: hardware ID used by switches (MAC table). :contentReference[oaicite:21]{index=21}  

**Why packet fields matter (IPv4 header examples):** version, header length (IHL), ToS, total length, identification/flags/fragment offset, **TTL**, protocol, checksum, source/destination IP, options. Useful for routing, detection, and forensics. :contentReference[oaicite:22]{index=22}  

---

## Key Takeaways  
- Know **what each device does** (hub vs switch vs router vs firewall) and where it fits in a diagram. :contentReference[oaicite:23]{index=23}  
- **Cloud & SDN** shift hardware functions into software → faster changes, lower cost, elastic scale. :contentReference[oaicite:24]{index=24}  
- Use **TCP/IP & OSI** to reason about incidents and pinpoint impacted layers.   
- Understand **packets, ports, IPs, MACs** to investigate anomalies & attacks.   

---

## Glossary  
- **Bandwidth** – max data capacity (bps). :contentReference[oaicite:27]{index=27}  
- **Cloud computing** – remote servers/apps/services over Internet. :contentReference[oaicite:28]{index=28}  
- **Cloud network** – remotely hosted servers/data accessed via Internet. :contentReference[oaicite:29]{index=29}  
- **Data packet** – basic unit of data transfer on a network. :contentReference[oaicite:30]{index=30}  
- **Hub** – broadcasts frames to all ports (legacy). :contentReference[oaicite:31]{index=31}  
- **IP / IP address** – routing standard / unique device location.   
- **LAN / WAN** – small / large area network. :contentReference[oaicite:33]{index=33}  
- **MAC address** – unique hardware identifier for a NIC. :contentReference[oaicite:34]{index=34}  
- **Modem** – connects router/LAN to ISP. :contentReference[oaicite:35]{index=35}  
- **Packet sniffing** – capturing/inspecting packets on the network. :contentReference[oaicite:36]{index=36}  
- **Port** – software endpoint organizing traffic by service. :contentReference[oaicite:37]{index=37}  
- **Router** – connects networks and forwards by IP. :contentReference[oaicite:38]{index=38}  
- **Switch** – forwards by MAC to specific port; builds MAC table. :contentReference[oaicite:39]{index=39}  
- **TCP/UDP** – transport protocols (reliable vs fast). :contentReference[oaicite:40]{index=40}  
- **TCP/IP model** – 4-layer comms framework. :contentReference[oaicite:41]{index=41}  
- **OSI model** – 7-layer comms framework. :contentReference[oaicite:42]{index=42}  

---

