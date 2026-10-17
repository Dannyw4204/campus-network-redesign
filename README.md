# Campus Network Redesign

A network design portfolio project: redesigning the LAN for a fictional company, Northbridge Logistics, including a Cisco-to-Juniper migration. All details are made up.

## Scenario
- 500 users across 3 buildings: Headquarters, Warehouse, Annex
- Current network: ageing Cisco access switches, flat VLAN design
- Goal: refresh to Juniper with a cleaner, more secure design

## Requirements
- Redundant uplinks between buildings
- Separate networks for staff, guests, voice, and warehouse scanners
- Room to grow by 30% over 5 years
- Minimal downtime during migration

## Contents
1. [High-level design](docs/high-level-design.md): topology and why
2. [IP and VLAN plan](docs/ip-and-vlan-plan.md): addressing scheme and subnets
3. [Diagrams](docs/diagrams.md): VLANs by building, firewall policy
4. [Design decisions log](docs/decisions-log.md): the choices and trade-offs
5. [Migration plan](docs/migration-plan.md): phased Cisco-to-Juniper cutover
6. [Security design](docs/security-design.md): segmentation and resilience

## Skills shown
Network design, IP planning, segmentation, migration planning, documentation, diagrams as code
