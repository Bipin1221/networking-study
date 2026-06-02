# Networking Study — CCNA 200-301 v1.1

Self-directed networking study program targeting **NOC Analyst / Network Engineer** roles.
Building from zero practical knowledge to CCNA certification and job-ready skills.

**Background:** Computer Engineering graduate with Python/ML experience
**Start date:** 20 may 2026 
**Target:** CCNA 200-301 v1.1 exam + NOC/Network Engineer role.

---

## Progress tracker

| Week | Topics | Labs |
|---|---|---|
| Week 1 | OSI · TCP/IP · Subnetting · TCP/UDP · DHCP · ARP · VLANs · Trunks · Inter-VLAN routing · SVIs | 11 labs |
| Week 2 | Static routing · OSPF · STP | In progress |
| Week 3 | ACLs · NAT · DHCP server config | Planned |
| Week 4+ | NOC tools · Python automation · Portfolio | Planned |

---

## Week 1 — Foundations

### Topics covered
- OSI model (all 7 layers) and TCP/IP model
- IPv4 addressing, binary conversion, subnetting (/24–/30)
- TCP, UDP, DNS, DHCP, ARP — how they work and Wireshark captures
- Cisco IOS CLI — router and switch configuration
- VLANs, trunk links (802.1Q), inter-VLAN routing
- Router-on-a-Stick (ROAS) and Layer 3 switch SVIs
- Default routing to internet simulation

### Subnetting benchmark
| Benchmark | Average time | Accuracy |
|---|---|---|
| Day 3 (baseline) | 69 seconds | 30/30  |
| Day 7 (Week 1 close) | 34 seconds | 20/20  |
| Improvement | **51% faster** | Perfect |

### Labs

| File | What it demonstrates |
|---|---|
| Basic_VLAN_Isolation.pkt | VLAN isolation built from memory |
| VLAN_Cross_Link_Trunk.pkt | Dual-switch trunk with native VLAN security |
| ROAS_Inter_VLAN_Routing.pkt | 3-VLAN Router-on-a-Stick from scratch |
| Layer3_switch_with_svi.pkt | Layer 3 switch SVIs — inter-VLAN without external router |
| full_Netowork.pkt | Full topology: L3 switch + router + default route to internet |
| 3_VLAN_Network.pkt | Full topology with complex VLAN setup and route to internet |

### Wireshark captures
| File | What it shows |
|---|---|
| dhcp-dora-4packets.png | Full DORA process, source IP 0.0.0.0, UDP 67/68 |
| arp-request-reply.png | Broadcast request ff:ff:ff:ff:ff:ff, unicast reply |

---

## Tools used
- **Cisco Packet Tracer** — network simulation and lab environment
- **Wireshark** — live packet capture and protocol analysis
- **Anki** — spaced repetition flashcard system (150+ cards)
- **subnettingpractice.com** — daily subnetting speed drills

## Resources
- Jeremy's IT Lab (YouTube) — CCNA 200-301 v1.1 full course
- Professor Messer N10-009 — protocol reference videos
- PowerCert Animated Videos — visual protocol explanations

---

*Updated weekly as study progresses.*