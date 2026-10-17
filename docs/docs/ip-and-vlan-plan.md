# IP and VLAN plan

## Addressing scheme
Subnets follow the pattern `10.<building>.<VLAN>.0/24`.

- Building 1 = HQ, Building 2 = Warehouse, Building 3 = Annex
- VLAN IDs are the same in every building, so a function always has the same number

## VLANs
| VLAN | Name | Purpose |
|------|------|---------|
| 10 | Staff | Employee devices |
| 20 | Voice | IP phones |
| 30 | Guest | Visitors, internet only |
| 40 | Scanners | Warehouse handhelds |
| 99 | Management | Switch and device management |

## Subnets
| Building | VLAN | Subnet |
|----------|------|--------|
| HQ | 10 Staff | 10.1.10.0/24 |
| HQ | 20 Voice | 10.1.20.0/24 |
| HQ | 30 Guest | 10.1.30.0/24 |
| HQ | 99 Mgmt | 10.1.99.0/24 |
| Warehouse | 10 Staff | 10.2.10.0/24 |
| Warehouse | 20 Voice | 10.2.20.0/24 |
| Warehouse | 30 Guest | 10.2.30.0/24 |
| Warehouse | 40 Scanners | 10.2.40.0/24 |
| Warehouse | 99 Mgmt | 10.2.99.0/24 |
| Annex | 10 Staff | 10.3.10.0/24 |
| Annex | 20 Voice | 10.3.20.0/24 |
| Annex | 30 Guest | 10.3.30.0/24 |
| Annex | 99 Mgmt | 10.3.99.0/24 |

## Why this design
- Each /24 holds 254 hosts, enough for 30% growth per building
- Building and VLAN are readable straight from the address
- Guest and scanner traffic stays in its own subnets, so firewall rules are simple
