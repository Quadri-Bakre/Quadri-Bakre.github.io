---
# Case study: anonymised. No vessel name, company name, project number, IPs, MACs or serials.
title: "Private Yacht: Converged AV and Network"
category: Marine
role: Design & Commissioning Engineer
focus: Network / AV-over-IP / Control
status: Commissioned & Handed Over

hero: /assets/images/yacht/yacht-rack-front.jpg
hero_alt: Front of the finished rack, with power distribution, network switch, Crestron control processor and four Crestron NAX units
hero_position: center 30%

hardware:
  - Cisco Layer 3 core switch
  - Netgear switch for AV traffic
  - Cisco rack switch
  - 8 PoE edge switches in the cabins
  - 9 Ruckus access points
  - Pepwave router with two Starlink services
  - Crestron CP4-R control processor
  - 4 Crestron DM NAX units
  - 5 Bluetooth input plates
  - 8 Dante-enabled amplifiers

software:
  - Crestron Home Setup
  - Dante Controller
  - Afara
  - Netgear Engage
  - Crestron Toolbox

gallery:
  - image: /assets/images/yacht/yacht-patch-terminations.jpg
    alt: Top-down view of the patch panel terminations and power
    caption: Patch panel terminations and power, dressed and labelled before the rack left the workshop.
  - image: /assets/images/yacht/yacht-power-labelling.jpg
    alt: Labelled power leads dressed along the rack frame
    caption: Power leads labelled by circuit and dressed along the frame.
  - image: /assets/images/yacht/yacht-rack-rear.jpg
    alt: Rear of the rack showing power distribution and amplifiers
    caption: Rear of the rack, with power distribution at the top and the amplifiers below.
  - image: /assets/images/yacht/yacht-amplifier-wiring.jpg
    alt: Amplifier rear panels with speaker cables in braided looms
    caption: Amplifier tier, with speaker runs gathered into braided looms.
  - image: /assets/images/yacht/yacht-speaker-outputs.jpg
    alt: Labelled speaker outputs on an amplifier
    caption: Speaker outputs, each labelled so every run can be traced at handover.
  - image: /assets/images/yacht/yacht-rack-on-rails.jpg
    alt: The finished rack on its rails with cable looms coiled
    caption: The finished rack on its rails, ready to go on board.

diagram: diagrams/yacht-network.svg
diagram_caption: Simplified diagram drawn for this page, showing device types and VLANs only.

back_link: /portfolio.html
---
## The Brief

Everything on board had to run on one converged network: multi-zone audio, control, TV, and separate owner and guest internet, with connectivity that stays up at sea.

## The Design

**Core and switching.** A Cisco Layer 3 core switch handles inter-VLAN routing and DHCP for the Home, Guest, AV-over-IP and Crestron NAX VLANs. A dedicated Netgear switch carries the AV traffic, with a Cisco rack switch and eight PoE edge switches in the cabins.

**Wireless and WAN.** Nine Ruckus access points on trunk ports serve the owner and guest SSIDs. A Pepwave router with two Starlink services (land and marine) provides WAN failover.

**Security.** The guest VLAN is isolated from the private network with an inbound ACL. TV, AV and control each sit on their own VLAN, and devices are managed over SSH only.

**AV over IP.** Four Crestron DM NAX units, five Bluetooth input plates and eight Dante-enabled amplifiers run on AES67/Dante streams with PTPv2 clocking, controlled by a Crestron CP4-R.

## Configuration That Mattered

MST with the core as root bridge; loopback detection with err-disable auto-recovery; IGMP snooping and querier on the AV VLAN; unregistered multicast filtering; QoS trusting 802.1p for AV traffic; DHCP reservations.

## A Problem on the Way

The design took TV audio over HDMI ARC into the Dante amplifiers, but the Crestron driver for the Dante devices didn't behave reliably with that set-up. We found it while commissioning the system at our workshop, before it went on board, and I switched the TV audio to optical, which proved more dependable. It cost some commissioning time, but the problem was solved before the system reached the yacht.

## Testing and Handover

An 18-point commissioning schedule: DHCP per VLAN, guest isolation, WAN failover, Wi-Fi coverage and roaming on every deck, spanning-tree root, PoE draw, IGMP querier and snooping, PTP clock lock, a 30-minute dropout test and switch power-cycle recovery. All tests passed. The system was handed over with configuration backups, a topology drawing and an as-built commissioning record.
