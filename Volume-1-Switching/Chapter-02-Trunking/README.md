# Lab 02: IEEE 802.1Q Trunking

## Objective
- Configure an inter-switch trunk link across Cisco Catalyst switches.
- Enable multi-VLAN traffic across a single physical connection using IEEE 802.1Q tagging.
- Verify intra-VLAN connectivity between devices connected to different switches.

## Topology & Addressing
- **Switches:** 2x Cisco Catalyst 2960 (`SW-atas` & `SW-bawah`)
- **Trunk Link:** `Fa0/1` <-> `Fa0/1`
- **VLAN 10 (Marketing):**
  - `SW-atas` `Fa0/2` -> PC0 (`192.168.10.1/24`)
  - `SW-bawah` `Fa0/2` -> PC1 (`192.168.10.2/24`)
- **VLAN 15 (Developer):**
  - `SW-atas` `Fa0/3` -> PC2 (`192.168.15.1/24`)
  - `SW-bawah` `Fa0/3` -> PC3 (`192.168.15.2/24`)

## Key Commands Tested
```text
SW-atas(config)# interface fa0/1
SW-atas(config-if)# switchport mode trunk
SW-atas# show interfaces trunk
