---
title: Troubleshooting
summary: Fault isolation across switching, Wi-Fi, WAN and AV streams, from interface error counters to multicast and clock sync.
related:
  - private-yacht-network
writing:
  - title: "An AV Engineer's 10 Essential On-site Tools"
    url: https://quadavpro.com/av-engineer-onsite-essentials-10-tools-installation/
  - title: "Secure Remote Access with a Raspberry Pi VPN"
    url: https://quadavpro.com/the-ultimate-teamviewer-alternative-secure-remote-access-with-a-raspberry-pi-vpn/
---
## How I approach it
1. **Work through the layers.** Start at the physical layer and work up: cables and interface errors, then switching, then IP and services, then the application.
2. **Use the evidence.** Interface error counters, switch logs, multicast group membership and clock status, rather than guesswork.
3. **Change one thing at a time.** So the cause is clear and the fix can be recorded.
4. **Fix the cause, not the symptom.** And note it so it doesn't come back on the next project.
5. **Diagnose remotely where I can.** Through a secure VPN I can reach switches, processors and AV devices directly, so many faults are found before anyone travels to site.

## Why I work this way
Faults in AV systems often look like one thing and turn out to be another: an audio dropout that's really a clock or multicast problem, or a control fault that's really an address conflict. A methodical approach finds the real cause faster and stops the same problem happening again.

## Tools I use
Switch and router management interfaces, interface counters and logs, Dante Controller, Afara.
