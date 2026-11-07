---
# Case study page. The part between the --- lines is the page's details (Obsidian shows them as Properties);
# everything below the second --- is the write-up, in normal Markdown.
title: Residential AV Rack
category: Residential
role: Lead AV & Commissioning Engineer
focus: Control / AV-over-IP / Network
status: Commissioned & Active

# Keeps the page at its original web address
permalink: /residential_av_rack.html

hero: /assets/images/Residential AV Rack.png
hero_alt: Residential AV and Network Rack

hardware:
  - "Middle Atlantic 42U Enclosure"
  - "Control4 CP4-R"
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
  - image: https://images.unsplash.com/photo-1544197150-b99a580bb7a8?auto=format&fit=crop&q=80&w=800
    alt: "Cable Management Detail"
    caption: "Detail of the right-channel signal dressing. CAT6a bundles are separated by destination to ensure rapid serviceability and fault finding."
  - image: https://images.unsplash.com/photo-1563396983906-b3795482a59a?auto=format&fit=crop&q=80&w=800
    alt: "Rear Rack View"
    caption: "Rear view showing the amplifier tier and custom lacing bars utilized to support the weight of the heavy analog audio looms."

back_link: /portfolio.html#racks
next_title: Theater Lighting Panel
next_url: "#"
---
## The Overview

This project required the fabrication and deployment of a 42U primary rack designed to serve a multi-floor residential home. The system needed to handle over 10 individual AES67 audio endpoints, amplifiers, complete centralized audio routing via Crestron NAXs, and a massive 8 x 8 video switching matrix spanning multiple meeting rooms and central control with Crestron Home.

## The Challenge

The primary hurdle was extreme density. With four high-output amplifiers and a loaded Cisco network switch housed in a single rack, thermal management was a critical concern. Furthermore, a zero-tolerance policy for signal interference, requiring strict physical separation of low-voltage power lines and extra low-voltage CAT6a control networks.

## The Engineering Solution

To address thermal throttling, I opted to use blanking panels and incorporated passive airways at the top of the rack to promote a forced‑air chimney effect, drawing cool air from the bottom. For cable management, I implemented customized rear lacing bars. All 230V power was routed cleanly down the left vertical channel, while all audio stream, control, and video signals were organized along the right. Spacing and separation were carefully planned to minimize crosstalk and preserve the low‑noise performance required for the video matrix.
