# Lab 03: Native VLAN & Security

## Objective
- Understand the role of Native VLAN in handling untagged frames across 802.1Q trunks.
- Diagnose and analyze Native VLAN mismatch warnings and inter-VLAN traffic leakage.
- Remediate security risks by dedicating an unused VLAN (VLAN 99) as the Native VLAN.
- Solve multi-switch transit VLAN dropping in the practical challenge topology.

## Topology & Addressing

### Understanding Lab
- **Switches:** 2x Cisco Catalyst 2960 (`SW-1` & `SW-2`)
- **Trunk Link:** `Fa0/2` <-> `Fa0/2`
- **Initial Setup (Traffic Leak Demo):**
  - `SW-1`: Laptop0 on `Fa0/1` (VLAN 20, IP: `192.168.10.1/24`), Native VLAN set to 20
  - `SW-2`: Laptop1 on `Fa0/1` (VLAN 30, IP: `192.168.10.2/24`), Native VLAN set to 30
- **Remediation Setup:**
  - Dedicated Native VLAN 99 created and assigned on both switches to restore Layer 2 isolation.

### Challenge 3 (Multi-Switch Transit)
- Multi-switch environment validating frame tagging across intermediate transit switches.

## Key Commands Tested
```text
SW-1(config)# vlan 99
SW-1(config-vlan)# name NATIVE_ISOLATION
SW-1(config)# interface fa0/2
SW-1(config-if)# switchport trunk native vlan 99
SW-1# show interfaces trunk
