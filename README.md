# 🌐 Automated Multi-Switch Inter-VLAN & DHCP Deployment via Netmiko

A production-grade network automation framework built with **Python and Netmiko** to programmatically provision multi-layer Cisco switches in a **GNS3** simulated environment. This project demonstrates programmatic SSH device management, dynamic VLAN/SVI creation, automated DHCP pools, and OSPF wildcard network routing.

---

## 📐 Network Topology

![Automated Network Topology](Screenshot%202026-08-13%20050410.png)

---

## 🚀 Key Architectural Highlights

* **🐍 Python & Netmiko Automation:** Programmatically pushes complex device configurations from an Ubuntu control node to multiple Cisco IOS switches via secure SSH.
* **🏢 Dynamic VLAN & SVI Provisioning:** Automatically provisions distinct VLANs (HR VLAN 10, Accounting VLAN 20, IT VLAN 30) along with their corresponding gateway SVI IP addresses [cite: 1].
* **📡 Automated DHCP Scope Management:** Deploys dynamic DHCP pools, network scopes, default routers, and excludes core gateway addresses for seamless IP allocation [cite: 1].
* **🔄 Advanced OSPF Routing & Summarization:** Implements OSPF protocol with wildcard network statements (`10.0.0.0 0.255.255.255`) to handle multi-subnet connectivity efficiently [cite: 1].
* **🔌 Robust Connectivity Framework:** Integrates complete base static routing and core router/switch build configurations for underlying network transport [cite: 1].

---

## 🗺️ Script & Architecture Breakdown

| Component / File | Description & Key Functions | Primary Capabilities |
| :--- | :--- | :--- |
| **`dhcpnew.py`** | Core Python Automation Script | Multi-device connection handling via Netmiko, dynamic dictionary data modeling, configuration batch pushing. |
| **`Conectivity.txt`** | Base Topology Build & Setup | Ubuntu static routing, Core Router (R1), Distribution Routers (R2, R3, R4), and L3 Switch base configs [cite: 1]. |
| **`DHCP_and_InterVlan_Routing.txt`** | Design Documentation | Notes and references regarding inter-VLAN routing and DHCP architecture [cite: 1]. |
| **`Screenshot 2026-08-13 050410.png`** | GNS3 Topology Diagram | Visual layout of the automated multi-switch environment and connected client PCs [cite: 1]. |

---

## 📁 Repository Structure & Device Configurations

The complete project files and automation templates are organized as follows:

* 📄 `dhcpnew.py` - Main Python Netmiko automation script for switch provisioning
* 📄 `Conectivity.txt` - Base router, switch, and static routing build configurations [cite: 1]
* 📄 `DHCP_and_InterVlan_Routing.txt` - Deployment notes and architecture details [cite: 1]
* 🖼️ `Screenshot 2026-08-13 050410.png` - GNS3 network topology screenshot [cite: 1]

---

## 🛠️ Tech Stack & Tools

* **Automation & Language:** Python 3, Netmiko Library [cite: 1]
* **Network Simulator:** GNS3 / Cisco IOU / VPCS [cite: 1]
* **Operating System:** Ubuntu Linux (Control Node) [cite: 1]
* **Protocols:** OSPFv2, Inter-VLAN Routing, DHCP, SSH [cite: 1]

---

## 👤 Author

**Tishan Nilusha**  
*Cybersecurity | Networking Enthusiast*  
