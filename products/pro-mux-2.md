# PRO-MUX-2 — Type-Approved NMEA 0183 Multiplexer

> A type-approved intelligent NMEA 0183 multiplexer, combining and managing multiple 0183 data streams for professional installations.

| | |
|---|---|
| **Category** | NMEA 0183 Multiplexer (PRO range) |
| **Status** | Current |
| **Connects** | Multiple NMEA 0183 devices ↔ combined NMEA 0183 output |
| **Product page** | https://actisense.com/products/pro-mux-2/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-25192) |

---

## Overview

The PRO-MUX-2 is a type-approved intelligent NMEA 0183 multiplexer. It combines several
NMEA 0183 inputs into managed outputs with configurable routing, filtering, and prioritisation,
and is designed for professional and commercial installations.

## Key Features

- Intelligent multiplexing of multiple isolated NMEA 0183 inputs
- Configurable routing, filtering, and prioritisation
- Per-port configurable baud rates
- Type approved for professional/commercial use
- Ethernet (RJ45) data routing to a local network via 4 Data Servers (TCP/UDP)
- Robust PRO-range enclosure

## Connections & Interfaces

- **NMEA 0183:** Multiple isolated input ports and combined output ports
- **Configuration:** Via the built-in web interface (over Ethernet)
- **Power:** Powered independently from its own dedicated supply (see datasheet for voltage range).
- **Ethernet:** RJ45 port — routes data to a local network and hosts the web-configuration interface

## Ethernet & Data Servers

This unit has an **RJ45 Ethernet** port. As well as routing data to a local network, the port is used to configure the unit through its **web interface**.

Data is served through **4 Data Servers**, which work like the Data Servers on the wireless W2K-1 / W2K-2 / WGX-1 but over a wired connection:

- Each Data Server communicates over **TCP or UDP**.
- Each can be configured for **Transmit, Receive, or Both**.

## Getting Started

1. Mount the unit and wire each NMEA 0183 talker to a numbered input.
2. Connect combined output(s) to your listener(s).
3. Configure baud rates, routing, and filtering via the web interface.
4. Verify all required sentences appear on the output.

## Firmware & Updates

Firmware and configuration are handled through the built-in **web interface** over Ethernet (the same approach as the W2K-1, W2K-2, and WGX-1). Always run the latest —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-25192).

## Common Use Cases

- Combining multiple 0183 talkers onto a single listener
- Filtering and prioritising navigation data
- Type-approved commercial installations

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| Input not seen | Baud rate / polarity mismatch | Set correct per-port baud rate and wiring |
| Sentences dropped | Output throughput exceeded | Apply filtering / prioritisation |

## Specifications

See the official datasheet for port counts, approvals, and power:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-25192).

## Related

- [PRO-NDC-1E](./pro-ndc-1e.md) — multiplexer with routing intelligence
- [PRO-BUF-2](./pro-buf-2.md) — NMEA buffer

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
