# Networking Study — CCNA 200-301 v1.1

Self-directed networking study program targeting **NOC Analyst / Network Engineer** roles.
Building from zero practical knowledge to CCNA certification and job-ready skills.

**Background:** Computer Engineering graduate with Python/ML experience
**Start date:** 20 May 2026
**Target:** CCNA 200-301 v1.1 exam + NOC/Network Engineer role.

---

## Progress tracker

| Week | Topics | Labs | Status |
|---|---|---|---|
| Week 1 | OSI · TCP/IP · Subnetting · TCP/UDP · DHCP · ARP · VLANs · Trunks · Inter-VLAN routing · SVIs | 6 labs | ✅ Complete |
| Week 2 | Static routing · OSPF (single/multi-area, failover, troubleshooting) · STP/RSTP · EtherChannel | 23 labs | ✅ Complete |
| Week 3 | ACLs (standard, numbered/named) · EIGRP · RIP v2 | 5 labs | ✅ Complete |
| Week 4+ (in progress) | EIGRP/OSPF deep dive · subnetting up to /26 · continued daily MCQ + Anki review | Ongoing | 🔄 In progress — Day 16 |

---

## Week 1 — Foundations
📁 [`week1-Topology/`](./week1-Topology)

### Topics covered
- OSI model (all 7 layers) and TCP/IP model
- IPv4 addressing, binary conversion, subnetting (/24–/30)
- TCP, UDP, DNS, DHCP, ARP — how they work and Wireshark captures
- Cisco IOS CLI — router and switch configuration
- VLANs, trunk links (802.1Q), inter-VLAN routing
- Router-on-a-Stick (ROAS) and Layer 3 switch SVIs
- Default routing to internet simulation

### Labs
| File | What it demonstrates |
|---|---|
| `Basic_VLAN_Isolation.pkt` | VLAN isolation built from memory |
| `VLAN_crosslink_Trunk.pkt` | Dual-switch trunk with native VLAN security |
| `ROAS_inter_vlan_routing.pkt` | 3-VLAN Router-on-a-Stick from scratch |
| `layer3_switch_with_SVI.pkt` | Layer 3 switch SVIs — inter-VLAN without external router |
| `full_network.pkt` | Full topology: L3 switch + router + default route to internet |
| `3_vlan_network.pkt` | Full topology with complex VLAN setup and route to internet |

### Wireshark captures
📁 [`wireshark dhcp DORA/`](./wireshark%20dhcp%20%20DORA) · 📁 [`wireshark arp req and reply/`](./wireshark%20arp%20%20req%20and%20reply)

| File | What it shows |
|---|---|
| `Discover.png` / `Offer.png` / `Request.png` / `ACK.png` | Full DHCP DORA process, source IP 0.0.0.0, UDP 67/68 |
| `arp_request.png` / `arp-reply.png` | Broadcast request `ff:ff:ff:ff:ff:ff`, unicast reply |

---

## Week 2 — Routing, OSPF, STP & EtherChannel
📁 [`week2-Topology/`](./week2-Topology)

The largest lab set in the program so far — static routing fundamentals,
single- and multi-router OSPF (including failure scenarios), Spanning Tree
behavior, and EtherChannel link aggregation.

### Topics covered
- Static and floating static routes, default routing to the internet
- OSPF: single-area and multi-area, DR/BDR election, cost, interface config
  methods, passive interfaces, router ID, route summarization, failover,
  structured troubleshooting
- STP and RSTP — loop prevention behavior
- EtherChannel — PAgP, LACP, and static configurations

### Labs (selected highlights — full list in folder README)
| File | What it demonstrates |
|---|---|
| `basic_single_area_OSPF.pkt` → `4_router_ospf_config.pkt` | OSPF built up from single-area to a 4-router topology |
| `OSPF_failover.pkt` / `troubleshoot_ospf_network.pkt` | Link failure and deliberately broken topology for reconvergence/troubleshooting practice |
| `ospf_challange_4_router.pkt` / `final_ospf_challange.pkt` | Self-imposed challenge labs — no hints, task list only |
| `intro_spanning_tree.pkt` / `rstp.pkt` | STP root bridge election vs. RSTP faster convergence |
| `etherchannel-pagp.pkt` / `etherchannel-lacp.pkt` / `complete-etherchannel.pkt` | PAgP vs. LACP negotiation, combined into a full switching topology |

*See [`week2-Topology/README.md`](./week2-Topology) for the complete 23-lab breakdown.*

---

## Week 3 — ACLs, EIGRP & RIP
📁 [`week3-Topology/`](./week3-Topology)

### Topics covered
- Standard ACLs — numbered and named syntax
- Traffic filtering logic and rule ordering (implicit deny)
- EIGRP configuration and route exchange
- RIP v2 configuration and route exchange

### Labs
| File | What it demonstrates |
|---|---|
| `numbered_standard_ACL.pkt` | Standard ACL using legacy numbered syntax (1–99) |
| `named_standard_ACL.pkt` | Same filtering logic using named ACL syntax |
| `Standard ACLs.pkt` | Applied ACL topology with traffic-filtering verification |
| `eigrp-config.pkt` | EIGRP across a multi-router topology |
| `rip-config.pkt` | RIP v2 across a multi-router topology |

---

## Review labs — Weeks 1 & 2
📁 [`week 1&2 pratice lab/`](./week%201%262%20pratice%20lab%20)

Consolidation labs rebuilding VLANs, routing, and OSPF from memory to test
retention before moving to the next week's material: `vlan_trunk.pkt`,
`layer3_switch.pkt`, `static_floating_routing.pkt`, `fullospf.pkt`, and
`all_combined.pkt` (full combined topology, VLANs → OSPF, end-to-end).

---

## Subnetting benchmark

| Benchmark | Average time | Accuracy |
|---|---|---|
| Day 3 (baseline) | 69 seconds | 30/30 |
| Day 7 (Week 1 close) | 34 seconds | 20/20 |
| Day 16 (current, up to /26) | ~27 seconds | Consistently high |
| Improvement so far | **~61% faster** | Strong and stable |

---

## Tools used
- **Cisco Packet Tracer** — network simulation and lab environment
- **Wireshark** — live packet capture and protocol analysis
- **Anki** — spaced repetition flashcard system (150+ cards, missed questions pinned for review)
- **subnettingpractice.com** — daily subnetting speed drills

## Resources
- Jeremy's IT Lab (YouTube) — CCNA 200-301 v1.1 full course
- Professor Messer N10-009 — protocol reference videos
- PowerCert Animated Videos — visual protocol explanations

---

## What's next
- Finish EIGRP/OSPF comparison drills and NAT/DHCP server configuration labs
- Continue daily MCQ tests + Anki review with missed-question tracking
- Move toward full CCNA 200-301 exam readiness

---

*Updated weekly as study progresses. Last updated: Day 16 of the program.*