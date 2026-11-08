---
# Personal project. The repository is private: no client data, no addresses, no review findings on this page.
title: "Afara: Automated Commissioning and Audit Tool"
category: Personal project
role: Designer and developer
focus: Python / Network / AV
status: In use, under active development

# Cards on the Work page
group: software
featured: false
order: 1
summary: A tool I built that checks a network and its AV devices against the project schedule, maps it live, and writes the commissioning report.

hero: /assets/images/afara/afara-report-sample.png
hero_alt: A page from an Afara commissioning report, showing power and control system results with addresses hidden
hero_fit: whole

software:
  - Python
  - FastAPI
  - Netmiko and Paramiko
  - Requests
  - vis-network
  - Excel (input)
  - PDF and Word (output)
  - Git and Docker

gallery:
  - image: /assets/images/afara/afara-watchdog-code.jpg
    alt: Python code for the Afara watchdog script, open in a code editor
    caption: Part of the watchdog script that checks each device is still reachable.
    fit: whole
---
## The Idea

*Afara* is Yoruba for "the bridge". It bridges the gap between the design documents and the system that actually gets built.

On most systems integration projects, commissioning is still done by hand: an engineer logs into each device in turn, copies firmware versions, VLANs and port details into a checklist, saves configuration backups and then writes the report. It's slow, and it depends on remembering every step on every device. Mistakes there become security gaps and return visits.

Afara treats the **project schedule** (the Excel file engineers already keep) as the source of truth, and checks the real devices against it automatically. An audit and report that takes about a day by hand, depending on the size of the project, takes 10 to 20 minutes with Afara.

## Where It's Used

- **Before the rack leaves the workshop:** confirm it's ready for site: firmware, VLANs, configuration and backups.
- **During commissioning on site:** see straight away which devices are online and configured as designed.
- **After handover:** audit an existing system on a maintenance visit, to spot configuration changes or failing equipment.

## What It Does Today

- **Live topology map.** A network map in the browser, built from each device's uplink in the schedule. Click a switch, router or endpoint to see its status, MAC address, firmware and IP.
- **Two engines working side by side.** One checks the network every 15 seconds and updates the dashboard with pass or fail; the other runs the deeper audits and builds the reports in the background, so the dashboard never stalls.
- **Commissioning reports.** When the deep audit finishes, the dashboard offers the PDF and Word reports: a commissioning certificate with every device grouped by system (network, power, control, AV and media, security, servers), each marked pass or fail with its address, MAC, serial, firmware and location. It adds the detail underneath: VLANs on each switch, any cabling errors (CRC and input drops), PDU voltage, current and outlet states, and the internet connection's speed and latency.
- **One way of talking to every device.** Cisco switches over SSH, Windows machines over PowerShell, Crestron processors over CIP and SSH, GUDE power units over HTTP, and the same for Netgear, Ruckus, DrayTek, Hikvision and Loxone. Each is handled as a node in the same model.
- **Configuration backups** of switches, routers and Wi-Fi, ready for handover.

The banner above is a page from a test report run on lab equipment, with the addresses, MACs and serials hidden.

## Where It's Going

Afara is under active development. Next:

- **One central dashboard** covering every project, with history kept in a database.
- **Support for live projects:** notice when a device goes offline or is only partly working, try to bring it back, and report what happened.
- **A fuller report.** I've written a specification for what a complete Afara report should verify, system by system: network and Wi-Fi, power, control (Crestron, Control4, Lutron), video and audio, CCTV, and servers.

**Source code** is in a private GitHub repository and available to review on request.
