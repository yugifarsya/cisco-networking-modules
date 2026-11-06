# Lab 01: Basic VLAN Configuration

## Objective
- Create and manage VLANs on a Cisco Catalyst switch.
- Assign switchports to access mode across isolated broadcast domains.
- Verify Layer 2 traffic isolation using ICMP ping tests.

## Topology & Addressing
- **Switch:** Cisco Catalyst 2960-24TT (`SW-1`)
- **VLAN 10 (Ruang1):**
  - `Fa0/1` -> Laptop0 (`192.168.10.1/24`)
  - `Fa0/2` -> Laptop1 (`192.168.10.2/24`)
- **VLAN 20 (Ruang2):**
  - `Fa0/3` -> PC0 (`192.168.10.3/24`)
  - `Fa0/4` -> PC1 (`192.168.10.4/24`)

## Key Commands Tested
```text
SW-1(config)# vlan 10
SW-1(config-vlan)# name Ruang1
SW-1(config-if)# switchport mode access
SW-1(config-if)# switchport access vlan 10
SW-1# show vlan brief
