---
# Case study page. The part between the --- lines is the page's details (Obsidian shows them as Properties);
# everything below the second --- is the write-up, in normal Markdown.
title: Residential AV Rack
category: Residential
role: Lead Network & AV Commissioning Engineer
focus: Control / AV-over-IP / Network
status: Commissioned & Active

# Cards on the home page and the Work page
group: rack-builds
featured: true
order: 2
summary: A 42U primary rack for a multi-floor home, with centralised audio routing over Crestron NAX, AES67 endpoints and Crestron Home control.

# Keeps the page at its original web address
permalink: /residential_av_rack.html

hero: /assets/images/Residential AV Rack.png
hero_alt: Residential AV and Network Rack

hardware:
  - "Middle Atlantic 42U Enclosure"
  - "Crestron CP4-R"
  - "Crestron NAX Encoders/Decoders"
  - "Cisco Catalyst 1300 Switches"
  - "GUDE Power Distribution Units"
  - "Custom Lacing Bars"

software:
  - "Crestron Home Setup"
  - "Crestron Toolbox"
  - "Afara commissioning Software"

# Photos under "Technical Details". Figure numbers are added automatically.
gallery:
  - image: /assets/images/residential-av-rack/residential-rack-full.jpg
    alt: The full rack in the workshop before going to site
    fit: whole
    caption: The full rack, with power and switching at the top, sources and video distribution below, then the amplifiers, Crestron processor and NAX units.
  - image: /assets/images/residential-av-rack/residential-rack-sources.jpg
    alt: Power units, network switch, NVR and TV sources, each labelled
    caption: Power units, network switch, NVR and TV sources, each one labelled.
  - image: /assets/images/residential-av-rack/residential-amplifier-wiring.jpg
    alt: Amplifier outputs wired in orange speaker cable
    caption: Amplifier outputs in speaker cable, labelled and dressed along the rear.
  - image: /assets/images/residential-av-rack/residential-speaker-terminations.jpg
    alt: Labelled speaker cables in braided sleeving, tied to a lacing bar
    caption: Speaker runs with heat-shrink labels, sleeved and tied to the lacing bar above the amplifiers.
  - image: /assets/images/residential-av-rack/residential-cable-management.jpg
    alt: Speaker and data cables in separate bundles tied to the rack frame
    caption: Vertical cable management, with speaker and data runs kept in separate bundles.

back_link: /work/#rack-builds
---
## The Overview

This project required the fabrication and deployment of a 42U primary rack designed to serve a multi-floor residential home. The system needed to handle over 10 individual AES67 audio endpoints, amplifiers, complete centralized audio routing via Crestron NAXs, and a massive 8 x 8 video switching matrix spanning multiple meeting rooms and central control with Crestron Home.

## The Challenge

The primary hurdle was extreme density. With four high-output amplifiers and a loaded Cisco network switch housed in a single rack, thermal management was a critical concern. Furthermore, a zero-tolerance policy for signal interference, requiring strict physical separation of low-voltage power lines and extra low-voltage CAT6a control networks.

## The Engineering Solution

To address thermal throttling, I opted to use blanking panels and incorporated passive airways at the top of the rack to promote a forced‑air chimney effect, drawing cool air from the bottom. For cable management, I implemented customized rear lacing bars. All 230V power was routed cleanly down the left vertical channel, while all audio stream, control, and video signals were organized along the right. Spacing and separation were carefully planned to minimize crosstalk and preserve the low‑noise performance required for the video matrix.
