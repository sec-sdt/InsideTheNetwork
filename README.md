# InsideTheNetwork
Secure enterprise network architecture built in Cisco Packet Tracer with VLAN segmentation, OSPF routing, dual ISP redundancy, and firewall-based layered security.


## 📘 Overview

This project demonstrates the **design and implementation of a secure, redundant enterprise network** for a mid-sized business organization using **Cisco Packet Tracer**.  
As a cybersecurity graduate with a passion for networking, I approached this design not only from a connectivity standpoint but with **security and resilience** as core principles.

The network simulates a **600-user organization** spread across three floors and six departments, each isolated by VLANs, interconnected through multilayer switches, and protected by firewalls.  
This setup mirrors a **real-world enterprise deployment** with redundancy, scalability, and layered defense.

---

## 🏢 Case Study Summary

A trading support center with 600 employees is expanding into a new building that requires a complete network setup.  
The design must include:

- Hierarchical model with redundancy at every layer.  
- Two routers, two multilayer switches, and two ISP connections.  
- Wireless connectivity per department.  
- VLAN-based segmentation and DHCP configuration.  
- Secure inter-VLAN routing using Layer 3 switches.  
- OSPF as the dynamic routing protocol.  
- NAT Overload (PAT) for internet access.  
- Access Control Lists (ACLs) for traffic filtering.  
- Port security for critical departments.  

---

## ⚙️ My Implementation

I implemented all baseline requirements and then **enhanced the network with security-focused improvements**.  

### 🔧 Core Features
- Hierarchical design using **redundant core routers and multilayer switches**.  
- **Inter-VLAN routing** via Switch Virtual Interfaces (SVIs).  
- **DHCP server** for dynamic IP allocation to all departments.  
- **Dual ISP connections** to ensure internet redundancy.  
- **OSPF** configured for dynamic route advertisement across routers and switches.  
- **NAT Overload (PAT)** configured for efficient public IP utilization.  
- **Port security** on the Finance department switch ports (sticky MAC + violation shutdown).  

### 🔐 Security Enhancements
- Introduced **stateful firewalls** between the core routers and multilayer switches for each path.  
- Configured **ACL-based filtering** on the firewalls to permit legitimate traffic and block unauthorized access.  
- Enabled **SSH** for secure remote administration across routers and switches.  
- Disabled unnecessary services (e.g., CDP on external interfaces, IP domain lookup) to reduce attack surface.  
- Applied **layered defense strategy** ensuring segmentation, inspection, and control at every stage.  

---

## 🌐 Network Architecture

The design follows a **three-layer hierarchical model**:
- **Core Layer:** Dual routers connected to two ISPs for redundancy.  
- **Distribution Layer:** Dual multilayer switches handling inter-VLAN routing and redundancy.  
- **Access Layer:** Switches connecting user departments and wireless APs.  

Firewalls are strategically placed between the **core** and **distribution layers** to ensure traffic inspection and policy enforcement before reaching internal VLANs.


<img width="1917" height="992" alt="Screenshot 2025-10-04 123208" src="https://github.com/user-attachments/assets/5a911986-ebe1-44c3-ad67-52dfc5037a0e" />

---

## 🧩 Technologies & Protocols

| Category | Technology Used |
|-----------|------------------|
| Routing | OSPFv2 |
| Switching | VLANs, SVIs, Port Security |
| Addressing | Subnetting (172.16.1.0/16 base) |
| Security | ACLs, Firewalls, SSH |
| Internet Access | NAT Overload (PAT) |
| Redundancy | Dual Routers + Dual ISPs |
| Device Management | DHCP, Static IPs (Servers) |

---

## 🧱 Key Security Practices

- Layered security (firewalls + ACLs + VLAN segmentation).  
- Least privilege in ACL design.  
- Port security in sensitive departments.  
- SSH for remote management (no Telnet).  
- Static IP assignment for server assets.  

---

## 🧠 Lessons Learned

- Balancing redundancy, scalability, and security in enterprise design.  
- Importance of VLAN segmentation and inter-VLAN routing efficiency.  
- Applying real-world firewall policies using ACLs and stateful inspection.  
- Fine-tuning OSPF for optimal internal route advertisement.  
- Thinking like both a **network engineer** and a **security professional**.

---


