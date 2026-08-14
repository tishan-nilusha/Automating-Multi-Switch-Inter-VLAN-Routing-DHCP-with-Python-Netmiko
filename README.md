# 🌐 Automated Multi-Switch Inter-VLAN & DHCP Deployment via Netmiko

A production-grade network automation framework built with **Python and Netmiko** to programmatically provision multi-layer Cisco switches in a **GNS3** simulated environment. This project demonstrates programmatic SSH device management, dynamic VLAN/SVI creation, automated DHCP pools, and OSPF wildcard network routing.

---

## 📐 Network Topology

![Automated Network Topology](Screenshot%202026-08-13%20050410.png)

---

## 🚀 Key Architectural Highlights

* **🐍 Python & Netmiko Automation:** Programmatically pushes complex device configurations from an Ubuntu control node to multiple Cisco IOS switches via secure SSH.
* **🏢 Dynamic VLAN & SVI Provisioning:** Automatically provisions distinct VLANs (HR VLAN 10, Accounting VLAN 20, IT VLAN 30) along with their corresponding gateway SVI IP addresses .
* **📡 Automated DHCP Scope Management:** Deploys dynamic DHCP pools, network scopes, default routers, and excludes core gateway addresses for seamless IP allocation .
* **🔄 Advanced OSPF Routing & Summarization:** Implements OSPF protocol with wildcard network statements (`10.0.0.0 0.255.255.255`) to handle multi-subnet connectivity efficiently .
* **🔌 Robust Connectivity Framework:** Integrates complete base static routing and core router/switch build configurations for underlying network transport .
---

## 📁 Repository Structure & Device Configurations

The complete project files and automation templates are organized as follows:

* 📄 `Conectivity.txt` - Base router, switch, and static routing build configurations 
* 📄 `DHCP_and_InterVlan_Routing.txt` - Main Python Netmiko automation script for switch provisioning
* 🖼️ `Screenshot 2026-08-13 050410.png` - GNS3 network topology screenshot 

---

## 🛠️ Tech Stack & Tools

* **Automation & Language:** Python 3, Netmiko Library 
* **Network Simulator:** GNS3 / Cisco IOU / VPCS
* **Operating System:** Ubuntu Linux (Control Node) 
* **Protocols:** OSPFv2, Inter-VLAN Routing, DHCP, SSH 

---

## 👤 Author

**Tishan Nilusha**  
*Cybersecurity | Networking Enthusiast*  
