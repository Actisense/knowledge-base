# WGX-1 — NMEA 0183 and NMEA 2000 to Wi-Fi Gateway

> A Wi-Fi gateway that bridges both NMEA 0183 and NMEA 2000 data onto a wireless network, with conversion between the two standards.

| | |
|---|---|
| **Category** | NMEA 0183 + NMEA 2000 to Wi-Fi Gateway |
| **Status** | Current |
| **Connects** | NMEA 0183 & NMEA 2000 ↔ Wi-Fi / Ethernet |
| **Product page** | https://actisense.com/products/wgx-1/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-54510) |

---

## Overview

The WGX-1 combines NMEA 0183 and NMEA 2000 connectivity in a single Wi-Fi gateway. It makes
data from both buses available wirelessly and can convert between NMEA 0183 and NMEA 2000,
making it well suited to mixed-generation installations where older 0183 instruments coexist
with a modern NMEA 2000 backbone. It also supports onboard logging.

## Key Features

- Bridges NMEA 0183 and NMEA 2000 to Wi-Fi and Ethernet
- Conversion between NMEA 0183 and NMEA 2000
- Serves multiple wireless clients at once
- Onboard data logging to SD card
- Built-in web interface for configuration

## Connections & Interfaces

- **NMEA 2000:** Micro-C drop connection to the backbone
- **NMEA 0183:** Input/output serial lines for 0183 devices
- **Network:** Wi-Fi (access point / client) and wired Ethernet
- **Storage:** SD card slot — see [SD Card Guidance](../faq/faq-1.md)
- **Power:** Powered from the NMEA 2000 backbone.

## Getting Started

1. Connect the WGX-1 to a powered, terminated NMEA 2000 backbone and wire any NMEA 0183 devices.
2. Join the device's Wi-Fi network and open its web interface.
3. Configure 0183 baud rates, conversion rules, and output ports.
4. Verify data from both buses appears in your app.

## Software & Tools

- **Built-in web interface** — configuration, conversion setup, and firmware updates
- Compatible with apps that consume TCP/UDP NMEA data streams

## Firmware & Updates

Firmware is updated through the web interface. Always run the latest firmware —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-54510).

## Common Use Cases

- Adding Wi-Fi access to a mixed NMEA 0183 / NMEA 2000 installation
- Converting legacy 0183 instrument data onto an NMEA 2000 network (and vice versa)
- Wireless viewing and logging of combined vessel data

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| No 0183 data | Wrong baud rate or wiring polarity | Check baud rate and TX/RX wiring |
| No 2000 data | Backbone not powered/terminated | Verify NMEA 2000 power and termination |
| Logging issues | SD card full or wrong format | Use FAT32 ≤32 GB; see [SD Card Guidance](../faq/faq-1.md) |

## Specifications

See the official datasheet for supported sentences/PGNs, power, and LEN:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-54510).

## Related

- [W2K-2](./w2k-2.md) — NMEA 2000-only Wi-Fi gateway
- [PRO-NDC-1E2K](./pro-ndc-1e2k.md) — type-approved 0183 multiplexer + 2000 gateway

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
