# PRO-BUF-2 — Type-Approved NMEA Buffer

> A type-approved intelligent NMEA buffer that distributes a single NMEA 0183 talker to many listeners without signal degradation.

| | |
|---|---|
| **Category** | NMEA Buffer (PRO range) |
| **Status** | Current |
| **Connects** | One NMEA 0183 talker ↔ multiple isolated NMEA 0183 listeners |
| **Product page** | https://actisense.com/products/pro-buf-2-nmea-0183-buffer/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-8083) |

---

## Overview

The PRO-BUF-2 is a type-approved intelligent NMEA buffer. A single NMEA 0183 talker often
cannot reliably drive many listeners; the PRO-BUF-2 takes one input and reproduces it across
multiple isolated outputs, preserving signal integrity across a larger installation. It is
aimed at professional and commercial vessels.

## Key Features

- Distributes one NMEA 0183 source to multiple isolated outputs
- Maintains signal integrity across many listeners
- Electrically isolated outputs
- Type approved for professional/commercial use
- Ethernet (RJ45) data routing to a local network via a single Data Server (TCP/UDP)
- Robust PRO-range enclosure

## Connections & Interfaces

- **NMEA 0183:** One input port, multiple buffered/isolated output ports
- **Configuration:** Via Actisense Toolkit or the built-in web interface (over Ethernet)
- **Power:** Powered independently from its own dedicated supply (see datasheet for voltage range).
- **Ethernet:** RJ45 port — routes data to a local network and hosts the web-configuration interface

## Ethernet & Data Servers

This unit has an **RJ45 Ethernet** port. As well as routing data to a local network, the port is used to configure the unit through its **web interface**.

Data is served through a **single Data Server**, which works like the Data Servers on the wireless W2K-1 / W2K-2 / WGX-1 but over a wired connection:

- Each Data Server communicates over **TCP or UDP**.
- Each can be configured for **Transmit, Receive, or Both**.

## Getting Started

1. Wire the source talker to the buffer input (mind polarity and baud rate).
2. Connect each listener to a separate output port.
3. Confirm every listener receives the data cleanly.

## Software & Tools

- **Actisense Toolkit** — configuration and firmware updates (where applicable)
- **Web interface** — configuration and status over the RJ45 Ethernet connection

## Firmware & Updates

Managed via the Actisense toolkit. Always run the latest —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-8083).

## Common Use Cases

- Feeding one GPS or AIS source to several displays and instruments
- Isolating listeners to prevent ground loops and loading
- Type-approved commercial installations

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| One output dead | Wiring fault on that port | Check that output's wiring/polarity |
| All outputs dead | No/incorrect input signal | Verify input source, baud rate, and polarity |

## Specifications

See the official datasheet for output count, isolation, approvals, and power:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-8083).

## Related

- [PRO-NBF-1](./pro-nbf-1.md) — type-approved NMEA buffer variant
- [PRO-MUX-2](./pro-mux-2.md) — multiplexer

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
