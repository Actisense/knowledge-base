# PRO-NDC-1E2K — Type-Approved NMEA 0183 Multiplexer / NMEA 2000 Gateway

> A type-approved intelligent NMEA 0183 multiplexer with an integrated NMEA 2000 gateway, for professional and commercial installations.

| | |
|---|---|
| **Category** | NMEA 0183 Multiplexer + NMEA 2000 Gateway (PRO range) |
| **Status** | Current |
| **Connects** | Multiple NMEA 0183 devices ↔ combined output ↔ NMEA 2000 |
| **Product page** | https://actisense.com/products/pro-ndc-1e2k/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-54400) |

---

## Overview

The PRO-NDC-1E2K combines Actisense's intelligent NMEA 0183 multiplexer with an NMEA 2000
gateway in a single type-approved unit. It merges several NMEA 0183 inputs into combined
outputs and bridges that data to and from an NMEA 2000 backbone, making it suited to
commercial vessels and professional installations that must meet type-approval requirements.

## Key Features

- Intelligent multiplexing of multiple NMEA 0183 inputs
- Integrated NMEA 0183 ↔ NMEA 2000 gateway
- Type approved for professional/commercial use
- Ethernet (RJ45) data routing to a local network via 2 Data Servers (TCP/UDP)
- Configurable prioritisation, filtering, and baud rates
- Robust PRO-range enclosure and connectors

## Connections & Interfaces

- **NMEA 0183:** Multiple isolated input ports and combined output ports
- **NMEA 2000:** Micro-C drop connection to the backbone
- **Configuration:** Via the built-in web interface (over Ethernet)
- **Power:** Powered independently from its own dedicated supply (see datasheet for voltage range).
- **Ethernet:** RJ45 port — routes data to a local network and hosts the web-configuration interface

## Ethernet & Data Servers

This unit has an **RJ45 Ethernet** port. As well as routing data to a local network, the port is used to configure the unit through its **web interface**.

Data is served through **2 Data Servers**, which work like the Data Servers on the wireless W2K-1 / W2K-2 / WGX-1 but over a wired connection:

- Each Data Server communicates over **TCP or UDP**.
- Each can be configured for **Transmit, Receive, or Both**.

## Getting Started

1. Mount the unit and wire each NMEA 0183 talker to a numbered input (mind polarity).
2. Connect combined outputs to listeners and the unit to the NMEA 2000 backbone.
3. Use the web interface to set baud rates, routing, filtering, and priorities.
4. Verify merged data on both the 0183 outputs and the NMEA 2000 network.

## Firmware & Updates

Firmware and configuration are handled through the built-in **web interface** over Ethernet (the same approach as the W2K-1, W2K-2, and WGX-1). Always run the latest —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-54400).

## Common Use Cases

- Merging GPS, AIS, heading, and instrument data on commercial vessels
- Bridging a professional NMEA 0183 installation to NMEA 2000
- Installations requiring type-approved equipment

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| Missing input data | Wrong baud rate / polarity | Check per-port baud rate and wiring |
| Output overload / dropped sentences | Combined throughput exceeds output rate | Apply filtering or prioritisation |
| No 2000 data | Backbone not powered/terminated | Verify NMEA 2000 power and termination |

## Specifications

See the official datasheet for port counts, isolation, approvals, and power:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-54400).

## Related

- [PRO-NDC-1E](./pro-ndc-1e.md) — multiplexer without the NMEA 2000 gateway
- [PRO-MUX-2](./pro-mux-2.md) — multiplexer variant
- [WGX-1](./wgx-1.md) — Wi-Fi 0183/2000 gateway

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
