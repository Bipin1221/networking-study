# Week 1 & 2 — Review Practice Labs

Consolidation labs built after Weeks 1–2, combining VLANs, routing, and OSPF
into single larger topologies to test retention across topics rather than
practicing them in isolation.

## Purpose
Each file here re-does a core Week 1–2 topic from scratch, without notes, as
a self-check before moving on to the next week's material.

## Labs in this folder

| File | What it demonstrates |
|---|---|
| `vlan_trunk.pkt` | VLAN + trunking review — rebuilt from memory to confirm retention |
| `layer3_switch.pkt` | Layer 3 switch / SVI inter-VLAN routing review |
| `static_floating_routing.pkt` | Static and floating static routing review, including backup path failover |
| `fullospf.pkt` | Full OSPF topology review — adjacencies, cost, and route verification |
| `all_combined.pkt` | Single topology combining VLANs, inter-VLAN routing, static routing, and OSPF end-to-end |

## Verification checklist used in these labs
- `show vlan brief`, `show interfaces trunk` — VLAN/trunk state
- `show ip route` — confirm both static and OSPF-learned routes appear correctly
- `show ip ospf neighbor` — confirm adjacencies in the combined topology
- End-to-end `ping`/`traceroute` across the full topology

---
*Part of the [networking-study](../) CCNA 200-301 program — see root README for the full weekly progress tracker.*