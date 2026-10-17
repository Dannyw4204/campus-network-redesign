# Design decisions log

Each entry records a choice, the options considered, and why.

## 1. Collapsed core instead of three-tier
- **Options:** collapsed core, or separate core, distribution, and access layers
- **Choice:** collapsed core
- **Why:** 500 users in 3 buildings doesn't need a separate distribution layer. Fewer devices means less to buy, configure, and troubleshoot.
- **Trade-off:** harder to scale if the company grows well beyond 3 buildings

## 2. Routed links between buildings, VLANs stay local
- **Options:** stretch VLANs across all buildings, or keep each VLAN inside one building and route between them
- **Choice:** keep VLANs local, route between buildings
- **Why:** avoids spanning tree problems across buildings, and a loop in one building can't take down the others
- **Trade-off:** devices can't keep the same IP when moved between buildings

## 3. OSPF as the internal routing protocol
- **Options:** OSPF, or BGP
- **Choice:** OSPF, single area
- **Why:** simple, widely understood, and fast to converge at this size
- **Trade-off:** would need rethinking if the network grew into multiple sites with many routes
