# Week 3 — ACLs, EIGRP & RIP

Access control lists for traffic filtering, plus two additional routing
protocols (EIGRP and RIP v2) to compare against the OSPF work from Week 2.

## Topics covered
- Standard ACLs — numbered and named
- Traffic filtering logic and rule ordering (implicit deny)
- EIGRP configuration and route exchange
- RIP v2 configuration and route exchange

## Labs in this folder

| File | What it demonstrates |
|---|---|
| `numbered_standard_ACL.pkt` | Standard ACL configured using the legacy numbered syntax (1–99) |
| `named_standard_ACL.pkt` | Same filtering logic using the named ACL syntax for readability/maintainability |
| `Standard ACLs.pkt` | Applied standard ACL topology with traffic-filtering verification |
| `eigrp-config.pkt` | EIGRP enabled across a multi-router topology, neighbor adjacency and route exchange |
| `rip-config.pkt` | RIP v2 enabled across a multi-router topology, route exchange and hop-count behavior |

## Verification checklist used in these labs
- `show access-lists` — confirm rule order and match counters
- `show ip interface` — confirm ACL applied to correct interface/direction
- `show ip eigrp neighbors` / `show ip route eigrp` — confirm EIGRP adjacency and routes
- `show ip protocols` / `show ip route rip` — confirm RIP timers and routes

---
*Part of the [networking-study](../) CCNA 200-301 program — see root README for the full weekly progress tracker.*