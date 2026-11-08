---
title: Network Security
summary: Guest isolation with ACLs, separate VLANs for CCTV, AV and control, firewall and VPN configuration on WatchGuard and DrayTek, and SSH-only device management.
related:
  - private-yacht-network
writing:
  - title: "Secure Remote Access with a Raspberry Pi VPN"
    url: https://quadavpro.com/the-ultimate-teamviewer-alternative-secure-remote-access-with-a-raspberry-pi-vpn/
---
## How I approach it
1. **Keep guests out of the private network.** Guest traffic is isolated with access control lists, and the isolation is tested, not assumed.
2. **Separate the systems.** CCTV, AV and control each sit on their own VLAN, so one compromised or faulty device can't reach everything.
3. **Lock down the edge.** Firewall rules and VPN access configured on WatchGuard or DrayTek.
4. **Manage devices safely.** SSH-only management, and configuration backups kept for every device.

## Why I work this way
High-end homes and yachts are attractive targets, and the owners rarely think about the network until something goes wrong. Security has to be part of the design, not added later, and it has to be proven: guest isolation is one of the tests on every commissioning schedule.

## Tools I use
Firewall Rules, ACLs, SSH, configuration backups, Afara
