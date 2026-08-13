# 🌐 GNS3 Enterprise Core Network Design

A production-grade, highly available, and secure multi-zone enterprise network infrastructure simulated in **GNS3 / Cisco IOU**. This project demonstrates multi-area OSPF routing, dynamic route redistribution with EIGRP, first-hop redundancy protocols (FHRP), Layer 3 EtherChannels, and core backbone hardening.

---

## 📐 Network Topology

![Enterprise Network Topology](Screenshot%202026-07-24%20005439.png)

---

## 🚀 Key Architectural Highlights

* **🛡️ Hardened Core Backbone (Area 0):** MD5 Authentication enabled across OSPF Area 0 core routers (`R6`, `R13`, `R14`, `R15`, `R16`) to protect against unauthorized neighbor adjacencies and route injection.
* **🔀 Multi-Domain Dynamic Routing:** Implementation of Mutual Route Redistribution between **OSPF Area 0** and **EIGRP 100** via Autonomous System Boundary Router (**ASBR - R17**).
* **⚡ Layer 3 EtherChannels & SVIs:** High-speed, loop-free link aggregation using L3 Port-Channels alongside Switch Virtual Interfaces (SVI) for inter-VLAN routing.
* **🔄 High Availability & Gateway Redundancy:** First-Hop Redundancy Protocols deployed across access zones using **HSRP** (Zone 1) and **VRRP** (Zone 3) to prevent single points of failure.
* **📡 Edge Infrastructure Services:** Centralized **DHCP Router Stack** (Zone 2) dedicated to dynamic IP management.

---

## 🗺️ Zone & Architecture Breakdown

| Zone / Area | Description & Key Protocols | Primary Capabilities |
| :--- | :--- | :--- |
| **Zone 0 (Core Backbone)** | OSPF Area 0 Core Routing | MD5 Authentication, Central Backbone Transit |
| **Zone 1 (Pink Area)** | OSPF Area 1 + SVIs | **HSRP** Gateway Redundancy, VLAN 10 Routing |
| **Zone 2 (Blue Area)** | OSPF Area 2 | **DHCP Router Stack**, Edge LAN Addressing |
| **Zone 3 (Green Area)** | OSPF Area 3 + SVIs | **VRRP** Resilient Gateway, VLAN 20 Routing |
| **Zone 4 (Red Area)** | EIGRP 100 Domain + L3 EtherChannels | **OSPF ↔ EIGRP Redistribution (ASBR - R17)**, L3 EtherChannels, VLAN 30 |

---

## 📁 Repository Structure & Device Configurations

The complete Cisco IOS/IOU device configurations are organized by zone:

* 📄 `Zone 0 Central Core Backbone Area 0 MD5 AUTH.txt` - OSPF Area 0 MD5 Security Configs
* 📄 `Zone 0 Central Core Backbone OSPF Routing.txt` - Central Core Routers (`R6`, `R13-R16`) Configs
* 📄 `Zone 1 HSRP & Inter-VLAN Routing Distribution.txt` - Area 1 Layer 3 Switches & HSRP Configs
* 📄 `Zone 2 DHCP & Edge LAN Zone.txt` - Area 2 Edge DHCP Router Stack Configs
* 📄 `Zone 3 VRRP-Based Resilient Gateway Zone.txt` - Area 3 Layer 3 Switches & VRRP Configs
* 📄 `Zone 4 Hybrid OSPF-EIGRP Enterprise Architecture.txt` - ASBR (`R17`), EIGRP 100, L3 EtherChannels & SVI Configs
