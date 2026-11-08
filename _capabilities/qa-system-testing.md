---
title: QA & System Testing
summary: Testing every layer before sign-off. DHCP per VLAN, guest isolation, WAN failover, Wi-Fi coverage and roaming, spanning tree, PoE, IGMP and PTP clock lock.
related:
  - private-yacht-network
---
## How I approach it
1. **Write the schedule first.** The test schedule is written from the design, so every requirement has a test.
2. **Test each layer.** DHCP on every VLAN, guest isolation, WAN failover, Wi-Fi coverage and roaming, spanning-tree root, PoE draw, IGMP querier and snooping, and PTP clock lock.
3. **Test for time, not just a moment.** Dropout tests over a set period, and recovery after switches are power-cycled.
4. **Record every result.** Pass or fail, with notes, in the commissioning record handed to the client.

## Why I work this way
QA is my job, and it's the part I care most about. A schedule turns "it seems fine" into evidence. It catches the faults that only show up under load or after a power cut, and it gives the client and the next engineer a clear record of what was proven.

## Tools I use
Written test schedules, Afara, Dante Controller, switch and Wi-Fi management tools.
