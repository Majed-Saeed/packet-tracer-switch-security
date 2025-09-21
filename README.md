# 🔒 Packet Tracer - Switch Security Lab

A comprehensive Cisco Packet Tracer lab focusing on securing Layer 2 switches using industry best practices. This project is ideal for students, network engineers, or professionals building a portfolio in network security and switching.

---

## 🧠 Overview

This lab demonstrates the configuration of:
- Secure VLAN segmentation
- Trunk hardening
- Port security
- DHCP snooping
- Spanning Tree Protocol enhancements (PortFast, BPDU Guard)

---

## 🗂 VLAN Table

| Switch | VLAN | Name        | Ports              | Network           |
|--------|------|-------------|--------------------|-------------------|
| SW-1   | 10   | Admin       | F0/1, F0/2          | 192.168.10.0/24   |
| SW-1   | 20   | Sales       | F0/10               | 192.168.20.0/24   |
| SW-1   | 99   | Management  | F0/24               | 192.168.99.0/24   |
| SW-1   | 100  | Native      | G0/1, G0/2          | None              |
| SW-1   | 999  | BlackHole   | All unused ports    | None              |
| SW-2   | 10   | Admin       | F0/1, F0/22         | 192.168.10.0/24   |
| SW-2   | 20   | Sales       | F0/10               | 192.168.20.0/24   |
| SW-2   | 99   | Management  | F0/24               | 192.168.99.0/24   |
| SW-2   | 100  | Native      | N/A                 | None              |
| SW-2   | 999  | BlackHole   | All unused ports    | None              |

---

## 🎯 Objectives

### 🔗 Part 1: Create a Secure Trunk
- Configure static trunking on G0/1 and G0/2
- Disable DTP (Dynamic Trunking Protocol)
- Create Native VLAN 100 and assign it to trunk ports

### 📴 Part 2: Secure Unused Switchports
- Shutdown all unused ports on SW-1
- Create VLAN 999 named "BlackHole"
- Move all unused ports to VLAN 999

### 🔐 Part 3: Implement Port Security
- Enable port security on active access ports (F0/1, F0/2, F0/10, F0/24)
- Limit to 4 MAC addresses per port
- Statically configure MAC on F0/1
- Enable sticky MAC learning
- Set violation mode to `restrict` (drop + log)

### 🌐 Part 4: Configure DHCP Snooping
- Trust trunk ports on SW-1
- Limit untrusted ports to 5 DHCP packets/second
- Enable DHCP snooping globally and for VLANs 10, 20, 99 on SW-2

### ⚡ Part 5: Configure STP Enhancements
- Enable PortFast on all active access ports (SW-1)
- Enable BPDU Guard on access ports (SW-1)
- Set PortFast as default on SW-2

---

## 💾 Files Included

- `Switch_Security_Configuration.pkt` – Main Packet Tracer project file

---

## 🛠 Tools Used

- **Cisco Packet Tracer** (Recommended version: 8.x or later)
- **Cisco IOS CLI**
- Knowledge of:
  - VLANs and trunking
  - Layer 2 security
  - DHCP Snooping
  - STP and BPDU Guard
