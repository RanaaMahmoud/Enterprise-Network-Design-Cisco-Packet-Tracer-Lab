<img src="images/network.png" width="400"/>

# Enterprise Network Design – Cisco Packet Tracer Lab


## 📌 Overview
This project is a complete enterprise network simulation built using Cisco Packet Tracer.  
It demonstrates real-world networking concepts such as VLAN segmentation, inter-VLAN routing, redundancy, DHCP services, PAT (NAT Overload), VTP, STP roles, SSH access, and port security.

The topology simulates a multi-site enterprise network with core, distribution, and access layers.

---

## 🏗️ Topology Summary
The network consists of:

- **3 Routers (R1, R2, R3)** for WAN connectivity
- **Multilayer Switches (Layer 3 switches)** for inter-VLAN routing
- **Access Switches (2960 series)** for end devices
- **Multiple VLAN segments**
- **Servers (DHCP, Application, etc.)**
- **End devices (PCs in different VLANs and departments)**

WAN links use point-to-point /30 subnets between routers.

---

## 🧠 Key Technologies Implemented

### 🔹 VLANs & Segmentation
- VLAN 100 → 192.168.100.0/24
- VLAN 200 → 192.168.200.0/24
- VLAN 300 → 192.168.30.0/24
- VLAN 400 → 192.168.40.0/24
- VLAN 500 → 192.168.50.0/24
- VLAN 600 → 192.168.60.0/24
- VLAN 70  → 192.168.70.0/24

Each VLAN represents a different department or security zone.

---

### 🔹 Inter-VLAN Routing
- Implemented using **Layer 3 Switches (SVI interfaces)**
- Enables communication between VLANs securely and efficiently

---

### 🔹 VTP (VLAN Trunking Protocol)
- Centralized VLAN management
- Some switches act as **VTP Server / Client**
- Ensures VLAN consistency across the network

---

### 🔹 Spanning Tree Protocol (STP)
- Root bridge selection configured (PVST / PVST+)
- Prevents loops in redundant switch topology

---

### 🔹 DHCP Services
- DHCP configured for VLANs (100 & 400 and others depending on design)
- Automatic IP allocation for end devices

---

### 🔹 PAT (Port Address Translation)
- Configured on edge router (R3)
- Allows internal private networks to access external networks using a single public IP

---

### 🔹 Security Features

#### ✔ Port Security
- Restricts unauthorized devices on switch ports
- Modes used:
  - Restrict
  - Protect
  - Shutdown

#### ✔ DHCP Snooping
- Prevents rogue DHCP servers
- Enhances trust in DHCP responses

#### ✔ SSH Access
- Secure remote management enabled on switches

---

## 🌐 WAN Connectivity
Routers are interconnected using point-to-point links:

- R1 ↔ R2
- R2 ↔ R3
- R1 ↔ R3

Subnet examples:
- 20.20.20.0/30
- 30.30.30.0/30
- 40.40.40.0/30

---

## 🖥️ Services Included
- DHCP Server
- Internal Application Server
- PC end devices across multiple VLANs
- Inter-network communication testing

---

## 🔐 Security Design Goals
- Network segmentation using VLANs
- Controlled inter-VLAN routing
- Port-level security enforcement
- DHCP spoofing protection
- Secure remote access via SSH
- NAT for internet simulation

---

## 🚀 How to Use
1. Open the `.pkt` file in Cisco Packet Tracer
2. Verify VLAN configurations on switches
3. Check trunk links between switches
4. Test inter-VLAN connectivity
5. Validate DHCP assignment
6. Test NAT/PAT internet access
7. Verify SSH access to network devices

---

## 🎯 Learning Outcomes
This lab demonstrates:
- Enterprise network design principles
- VLAN and trunk configuration
- Layer 3 switching
- WAN routing between multiple routers
- Network security hardening techniques
- Real-world troubleshooting scenarios

---

## 📂 Author
Network Security Lab Project – Designed for hands-on practice in enterprise networking and cybersecurity fundamentals.
