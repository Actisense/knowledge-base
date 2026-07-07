# PRO-NDC-1E — Type-Approved NMEA 0183 Multiplexer

> A type-approved intelligent NMEA 0183 multiplexer for professional installations, combining several 0183 inputs into managed outputs.

| | |
|---|---|
| **Category** | NMEA 0183 Multiplexer (PRO range) |
| **Status** | Current |
| **Connects** | Multiple NMEA 0183 devices ↔ combined NMEA 0183 output |
| **Product page** | https://actisense.com/products/pro-ndc-1e/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-25196) |

---

## Overview

The PRO-NDC-1E is an intelligent, type-approved NMEA 0183 multiplexer. It combines multiple
NMEA 0183 talkers into one or more managed outputs, with configurable prioritisation and
filtering so critical data is never lost. It is aimed at professional and commercial
installations where type approval is required.

## Key Features

- Intelligent multiplexing of multiple isolated NMEA 0183 inputs
- Configurable prioritisation and sentence filtering
- Per-port configurable baud rates
- Type approved for professional/commercial use
- Ethernet (RJ45) data routing to a local network via a single Data Server (TCP/UDP)
- Robust PRO-range enclosure

## Connections & Interfaces

- **NMEA 0183:** Multiple isolated input ports and combined output ports
- **Configuration:** Via the built-in web interface (over Ethernet)
- **Power:** Powered independently from its own dedicated supply (see datasheet for voltage range).
- **Ethernet:** RJ45 port — routes data to a local network and hosts the web-configuration interface

## Ethernet & Data Servers

This unit has an **RJ45 Ethernet** port. As well as routing data to a local network, the port is used to configure the unit through its **web interface**.

Data is served through a **single Data Server**, which works like the Data Servers on the wireless W2K-1 / W2K-2 / WGX-1 but over a wired connection:

- Each Data Server communicates over **TCP or UDP**.
- Each can be configured for **Transmit, Receive, or Both**.

## Getting Started

1. Mount the unit and wire each NMEA 0183 talker to a numbered input.
2. Connect the combined output(s) to your listener(s).
3. Configure baud rates, routing, and priorities via the web interface.
4. Confirm merged output contains all required sentences.

## Firmware & Updates

Firmware and configuration are handled through the built-in **web interface** over Ethernet (the same approach as the W2K-1, W2K-2, and WGX-1). Always run the latest —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-25196).

## Common Use Cases

- Merging GPS, AIS, and heading data into a single NMEA 0183 feed
- Prioritising critical navigation data on busy 0183 networks
- Type-approved commercial installations

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| Input not seen | Baud rate / polarity mismatch | Set correct per-port baud rate and wiring |
| Sentences dropped | Output throughput exceeded | Apply filtering / prioritisation |

## Specifications

See the official datasheet for port counts, approvals, and power:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-25196).

## Related

- [PRO-NDC-1E2K](./pro-ndc-1e2k.md) — adds an NMEA 2000 gateway
- [PRO-MUX-2](./pro-mux-2.md) — multiplexer variant
- [NDC-4](./ndc-4.md) — legacy multiplexer

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
