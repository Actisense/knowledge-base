# PRO-NBF-1 — Type-Approved NMEA Buffer

> A type-approved NMEA buffer that safely distributes a single NMEA 0183 source to multiple listeners.

| | |
|---|---|
| **Category** | NMEA Buffer (PRO range) |
| **Status** | Current |
| **Connects** | One NMEA 0183 talker ↔ multiple isolated NMEA 0183 listeners |
| **Product page** | https://actisense.com/products/pro-nbf-1-nmea-0183-buffer/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-8080) |

---

## Overview

The PRO-NBF-1 is a type-approved NMEA buffer. It takes a single NMEA 0183 talker and drives
multiple isolated outputs, allowing one data source to be shared reliably across several
listeners. It is designed for professional and commercial installations that require
type-approved equipment.

> **Note:** Unlike the other PRO-range units (PRO-NDC-1E, PRO-NDC-1E2K, PRO-MUX-2, PRO-BUF-2), the PRO-NBF-1 has **no Ethernet port and no Data Servers** — it is a standalone buffer.

## Key Features

- Distributes one NMEA 0183 source to multiple isolated outputs
- Preserves signal integrity across many listeners
- Electrically isolated outputs
- Type approved for professional/commercial use
- Robust PRO-range enclosure

## Connections & Interfaces

- **NMEA 0183:** One input port, multiple buffered/isolated output ports
- **Power:** Powered independently from its own dedicated supply (see datasheet for voltage range).

## Getting Started

1. Wire the source talker to the buffer input (mind polarity and baud rate).
2. Connect each listener to a separate output port.
3. Confirm every listener receives the data cleanly.

## Software & Tools

- **Actisense Toolkit** — configuration and firmware updates (where applicable)

## Firmware & Updates

Managed via the Actisense toolkit. Always run the latest —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-8080).

## Common Use Cases

- Sharing one GPS/AIS source across multiple displays
- Isolating listeners to avoid loading and ground loops
- Type-approved commercial installations

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| One output dead | Wiring fault on that port | Check that output's wiring/polarity |
| All outputs dead | No/incorrect input signal | Verify input source, baud rate, and polarity |

## Specifications

See the official datasheet for output count, isolation, approvals, and power:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-8080).

## Related

- [PRO-BUF-2](./pro-buf-2.md) — intelligent NMEA buffer
- [PRO-NDC-1E](./pro-ndc-1e.md) — multiplexer

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
