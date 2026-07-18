# Week 2 — Routing, OSPF, STP & EtherChannel

The largest lab set in the program. Covers static routing fundamentals, single-
and multi-router OSPF (including failure scenarios), Spanning Tree Protocol
behavior, and EtherChannel link aggregation.

## Topics covered
- Static and floating static routes (primary + backup path)
- Default routing to the internet
- OSPF: single-area and multi-area, DR/BDR election, cost calculation, interface
  configuration methods, passive interfaces, router ID, route summarization,
  failover behavior, and structured troubleshooting
- Spanning Tree Protocol (STP) and Rapid STP (RSTP) — loop prevention behavior
- EtherChannel — both PAgP and LACP negotiation, static (no protocol), and
  combined configurations

## Labs in this folder

### Static routing
| File | What it demonstrates |
|---|---|
| `simple_static_route .pkt` | Basic two-router static routing between subnets |
| `simple_3router_static.pkt` | Static routing extended across a 3-router topology |
| `floating_static_as_backup.pkt` | Floating static route configured as a backup path with higher administrative distance |
| `4_router_static_route_challange.pkt` | Self-imposed challenge lab: full static routing across 4 routers, no walkthrough used |
| `default_to_internet.pkt` | Default route configuration simulating internet-bound traffic |

### OSPF
| File | What it demonstrates |
|---|---|
| `basic_single_area_OSPF.pkt` | Foundational single-area OSPF adjacency and route exchange |
| `ospf_interface_method.pkt` | OSPF enabled via interface-level configuration (vs. network statements) |
| `ospf_dr_bdr.pkt` | DR/BDR election behavior on a multi-access segment |
| `ospf_cost.pkt` | Manual cost manipulation to influence OSPF path selection |
| `passive_interface_router_id.pkt` | Passive-interface configuration and manual router ID assignment |
| `route_summarisation .pkt` | OSPF route summarization to reduce routing table size |
| `4_router_ospf_config.pkt` | OSPF configured across a 4-router topology |
| `OSPF_failover.pkt` | Link failure scenario testing OSPF reconvergence |
| `troubleshoot_ospf_network.pkt` | Deliberately broken OSPF topology used for structured troubleshooting practice |
| `ospf_challange_4_router.pkt` / `final_ospf_challange.pkt` | Self-imposed challenge labs building full OSPF topologies from a task list, no hints |

### Spanning Tree
| File | What it demonstrates |
|---|---|
| `intro_spanning_tree.pkt` | Baseline STP behavior — root bridge election, port roles/states |
| `Configuring Spanning Tree.pkt` | Manual STP priority configuration to control root bridge election |
| `rstp.pkt` | Rapid STP configuration and faster convergence behavior vs. legacy STP |

### EtherChannel
| File | What it demonstrates |
|---|---|
| `etherchannel-pagp.pkt` | EtherChannel negotiated using PAgP (Cisco proprietary) |
| `etherchannel-lacp.pkt` | EtherChannel negotiated using LACP (IEEE standard) |
| `etherchannel-pagp&static.pkt` | Comparison of PAgP-negotiated vs. static (on/on) EtherChannel |
| `complete-etherchannel.pkt` | Full EtherChannel setup combined with a broader switching topology |

## Verification checklist used in these labs
- `show ip route` / `show ip ospf neighbor` — confirm routes and adjacencies
- `show ip ospf interface` — confirm cost, DR/BDR, and timers
- `show spanning-tree` — confirm root bridge and port states
- `show etherchannel summary` — confirm bundle status and protocol

---
*Part of the [networking-study](../) CCNA 200-301 program — see root README for the full weekly progress tracker.*