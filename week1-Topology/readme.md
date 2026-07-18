# Week 1 — Foundations: VLANs, Trunking & Inter-VLAN Routing

Packet Tracer labs covering VLAN segmentation, trunk links, and the two standard
methods of inter-VLAN routing (Router-on-a-Stick and Layer 3 switch SVIs).
Built from memory after study, not copied from a walkthrough.

## Topics covered
- VLAN creation and port assignment (access ports)
- 802.1Q trunking between switches
- Native VLAN behavior and trunk security
- Inter-VLAN routing via Router-on-a-Stick (sub-interfaces)
- Inter-VLAN routing via Layer 3 switch SVIs (no external router)
- End-to-end topology design combining VLANs with a default route to the internet

## Labs in this folder

| File | What it demonstrates |
|---|---|
| `Basic_VLAN_Isolation.pkt` | Two VLANs configured on a single switch, confirming hosts in different VLANs cannot reach each other without routing |
| `VLAN_crosslink_Trunk.pkt` | Dual-switch topology with an 802.1Q trunk link carrying multiple VLANs between switches |
| `ROAS_inter_vlan_routing.pkt` | Router-on-a-Stick: single router interface with sub-interfaces routing between 3 VLANs |
| `layer3_switch_with_SVI.pkt` | Layer 3 switch configured with SVIs to route between VLANs without a separate router |
| `3_vlan_network.pkt` | Larger topology with 3 VLANs, trunking, and routing combined |
| `full_network.pkt` | Complete Week 1 topology: multi-VLAN switching, Layer 3 routing, and a default route out to the internet |

## Verification checklist used in these labs
- `show vlan brief` — confirm VLAN-to-port assignment
- `show interfaces trunk` — confirm trunk state and allowed VLANs
- `show ip route` — confirm inter-VLAN routes are present
- End-to-end `ping` tests between hosts in different VLANs

---
*Part of the [networking-study](../) CCNA 200-301 program — see root README for the full weekly progress tracker.*