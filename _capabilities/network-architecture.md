---
title: Network Architecture
summary: Segmented networks for homes and yachts. VLAN and IP plans, Layer 3 core switching, enterprise Wi-Fi, dual-WAN failover, and the multicast and QoS settings AV-over-IP depends on.
related:
  - private-yacht-network
writing:
  - title: "An AV Engineer's Journey to High-End Smart Homes"
    url: https://quadavpro.com/high-end-av-installation-journe/
---
## How I approach it
I've designed networks for residential homes, private yachts, meeting rooms and home cinemas. The approach is the same each time:
1. **Design alongside the AV design.** I design the network for each project around the AV and control design, so every system has what it needs from day one.
2. **Segment by purpose.** Separate VLANs for the home, guests, AV-over-IP, control and CCTV, with an IP addressing plan written down before anything is configured.
3. **Route at the core.** A Layer 3 core switch handles inter-VLAN routing and DHCP, with 802.1Q trunks to the edge switches and access points.
4. **Build in resilience.** MST spanning tree with the core as root bridge, loop protection, PoE budgets checked, and dual-WAN failover for internet.
5. **Tune it for AV.** IGMP snooping and querier, unregistered multicast filtering, QoS trusting 802.1p, and PTP clocking for Dante and AES67.

## Why I work this way
In a modern home or yacht, the network carries everything: audio, video, control, cameras and the internet. A flat network works until it doesn't, and then everything fails at once. Segmenting and planning it properly keeps each system isolated, makes faults easy to trace, and gives AV-over-IP the conditions it needs to run without dropouts.

## Tools I use
Network testers, Wireshark, a Wi-Fi scanner, an IP scanner, network scripts (such as a DHCP hunt for rogue DHCP servers), and Afara.

## Hardware I work with
Cisco Catalyst 1300 and CBS350, Netgear M4250 AV Line, Ruckus, Ubiquiti UniFi, Aruba, Pepwave, DrayTek, WatchGuard.
