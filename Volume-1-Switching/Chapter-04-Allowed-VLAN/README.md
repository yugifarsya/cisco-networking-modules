# Lab 04: Trunk Allowed VLANs

## Objective
- Understand default trunk forwarding behavior where all VLANs (1-4094) are permitted.
- Restrict and filter unauthorized VLAN traffic across 802.1Q trunks using the `allowed vlan` parameter.
- Safely modify permitted VLAN lists using `add`, `remove`, and `except` without dropping active links.
- Verify active trunk forwarding states using CLI show commands.

## Topology & Addressing
- **Switches:** 2x Cisco Catalyst 2960 (`SW-1` & `SW-2`)
- **Trunk Link:** `Fa0/1` <-> `Fa0/1`
- **Configured VLANs:**
  - VLAN 10: Marketing
  - VLAN 20: Technical
  - VLAN 30: Guest
- **Traffic Validation:**
  - Ping verification before filtering (all VLANs communicate across switches).
  - Selective filtering applied on trunk to permit only specific VLANs while pruning unwanted broadcast traffic.

## Key Commands Tested
```text
SW-1(config)# interface fa0/1
SW-1(config-if)# switchport trunk allowed vlan 10,20
SW-1(config-if)# switchport trunk allowed vlan add 30
SW-1(config-if)# switchport trunk allowed vlan remove 30
SW-1# show interfaces trunk
