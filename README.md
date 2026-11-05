# Cisco Packet Tracer Lab Modules (Switching & Routing)

This repository contains my personal learning modules and hands-on lab files built using Cisco Packet Tracer. 

When I first started learning networking, standard certification handbooks (like MTCNA or CCNA) felt too dense and jumped straight into complex theories without showing the practical logic first. I wrote these modules to break down basic switching and routing step-by-step from the perspective of someone who recently struggled through those exact concepts.

Each lab includes a blank topology file (`.pkt`) to practice with, a solved configuration, and notes explaining why certain commands are used.

## Author & Context
- **Author:** Yugi Farsya Nugraha
- **Background:** Vocational High School Student (Computer Network Engineering)
- **Status:** In progress (updating alongside my CCNA preparation)
- **Module Language:** Bahasa Indonesia (guides/explanations), English (topology documentation & repository overview)

## Lab Index

| Chapter | Topic | What We Practice |
| :--- | :--- | :--- |
| Lab 01 | Basic VLAN | Isolating broadcast domains using access ports (VLAN 10 & 20) |
| Lab 02 | 802.1Q Trunking | Passing multiple VLANs across a single inter-switch cable |
| Lab 03 | Native VLAN & Tagging | Fixing traffic leakage, PVID mismatch, and isolating Native VLAN |
| Challenge 03 | Native VLAN Challenge | Multi-switch troubleshooting with transit VLAN drops |
| Lab 04 | Allowed VLAN | Filtering trunk traffic using `add`, `remove`, and `except` |
| Lab 05 | VTP (VLAN Trunking Protocol) | Syncing VLANs via Server-Client-Transparent & avoiding revision bombs |
| Lab 06 | Inter-VLAN Routing | Router-on-a-Stick (RoAS) with 802.1Q sub-interfaces & gateways |
| Lab 07 | Switch Virtual Interface (SVI) | Giving Layer 2 switches an IP & understanding line protocol status |
| Lab 08 | User & Privilege Management | Creating local users, testing Privilege 1 vs 15, and `secret` hashing |
| Lab 09.1 | Out-of-Band (Console) | Initial switch configuration via physical rollover cable |
| Lab 09.2 | Remote Access (Telnet) | Setting up VTY lines and understanding plaintext security risks |
| Lab 09.3 | Secure Remote (SSH) | Hardening VTY with RSA crypto keys (1024-bit) and local login |
| Lab 10 | Port Security | MAC address locking & violation modes |
| Lab 11 | EtherChannel | Link aggregation architectures via LACP |
| Lab 12 | Spanning Tree Protocol (STP) | Loop prevention & Root Bridge election |

## How to Follow the Labs
1. Open the initial `.pkt` file in Cisco Packet Tracer.
2. Follow the lab objectives outlined in each folder's markdown guide.
3. Compare your final configuration with the solved `.pkt` file if you run into issues.
