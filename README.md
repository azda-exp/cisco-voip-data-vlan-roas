cisco-voip-data-vlan-roas
Cisco Packet Tracer lab demonstrating Router-on-a-Stick (ROAS) with dual Voice &amp; Data VLAN segmentation, 802.1Q trunking, and inter-VLAN routing.


# Inter-VLAN Routing with Voice & Data Segmentation (ROAS)

## 📌 Project Overview
This repository contains a Cisco Packet Tracer simulation demonstrating the implementation of **Router-on-a-Stick (ROAS)** architecture combined with **Voice VLAN** technology. The project focuses on network segmentation, traffic prioritization, and inter-VLAN routing using industry-standard protocols.

## 🏗️ Network Architecture
The topology is designed to simulate a modern enterprise branch office where data and voice traffic share the same physical infrastructure but remain logically isolated for security and Quality of Service (QoS).

### Key Components:
- **Core Router (ISR4331):** Handles Inter-VLAN routing via 802.1Q sub-interfaces.
- **Multilayer Switch (Catalyst 3560):** Manages VLAN tagging and provides trunking services.
- **Endpoint Integration:** IP Phones (7960) act as mini-switches, daisy-chaining PCs to reduce cabling costs.

## ⚙️ Technical Specifications

### VLAN Segmentation
| VLAN ID | Name  | Network Segment    | Purpose               |
|---------|-------|--------------------|-----------------------|
| 10      | Data  | 192.168.10.0/24    | End-user PC Traffic   |
| 20      | Voice | 192.168.20.0/24    | VoIP/Telephony Traffic|

### Infrastructure Configuration
- **Access Ports:** Configured with dual-VLAN membership (`switchport access vlan 10` and `switchport voice vlan 20`).
- **Trunk Link:** Implemented 802.1Q encapsulation on the uplink to the router.
- **Router Sub-interfaces:** 
  - `Gi0/0/0.10`: Default Gateway for Data VLAN.
  - `Gi0/0/0.20`: Default Gateway for Voice VLAN.

## 🔍 Verification & Analysis
The configuration has been verified through the following steps:
1. **ICMP Connectivity:** Successful ping across the Data VLAN.
2. **Encapsulation Analysis:** Using Simulation Mode to verify **802.1Q Tagging** on the trunk link.
3. **VoIP Registration:** Verified IP Phone power-up and simulated voice traffic flow.

## 🚀 How to Use
1. Download the `.pkt` file from this repository.
2. Open it using **Cisco Packet Tracer (v8.2 or higher)**.
3. Observe the green link states (Ensure Power Adapters are connected to IP Phones).
4. Run a simulation to inspect VLAN headers in the PDU details.

---
**Author:** [""EHSAN""]  
**Topic:** Network Engineering | Cisco IOS | CCNA Lab
![GitHub stats](https://github-readme-stats.vercel.app/api?username=azda-exp&show_icons=true&theme=radical&hide_border=true&count_private=true)
