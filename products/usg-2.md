# USG-2 — USB to Serial (NMEA 0183) Gateway

> A robust, isolated USB-to-serial gateway for reliably connecting NMEA 0183 devices to a PC.

| | |
|---|---|
| **Category** | NMEA 0183 USB Gateway |
| **Status** | Current |
| **Connects** | NMEA 0183 (serial) ↔ PC (USB) |
| **Product page** | https://actisense.com/products/usg-2-nmea-0183-converter/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2591) |

---

## Overview

The USG-2 is a bidirectional USB-to-serial gateway designed for marine NMEA 0183 data. Unlike
generic USB-serial adapters, it is built for the electrical environment of a vessel, providing
isolation and configurable baud rates so NMEA 0183 talkers and listeners connect reliably to a
computer for viewing, logging, or routing.

## Key Features

- Bidirectional NMEA 0183 ↔ PC over USB
- Configurable baud rates for standard and high-speed 0183 (e.g. AIS)
- Electrical isolation suited to the marine environment
- Works with Actisense NMEA Reader and the SDK

## Connections & Interfaces

- **NMEA 0183:** Serial input and output lines
- **PC:** USB connection to the host computer
- **Power:** Powered via USB.

## Getting Started

1. Wire the NMEA 0183 talker/listener to the USG-2 input/output lines (mind polarity).
2. Connect the USB cable to your PC and install/allow the driver if prompted.
3. Open NMEA Reader (or your app) and select the USG-2 port and correct baud rate.
4. Confirm sentences are received/sent as expected.

## Software & Tools

- **Actisense NMEA Reader** — view and log NMEA 0183 sentences
- **[Actisense SDK](https://github.com/Actisense/SDK)** — integrate into custom applications

## Firmware & Updates

Drivers and configuration are managed via Actisense PC tools. Always run the latest —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2591).

## Common Use Cases

- Connecting an AIS receiver or GPS to a PC charting application
- Logging NMEA 0183 traffic for diagnostics
- Bridging legacy 0183 instruments into PC software

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| No data / garbled data | Wrong baud rate | Match baud rate to the connected device (e.g. 38400 for AIS) |
| Nothing received | Reversed data polarity | Swap NMEA 0183 +/- wiring |
| Port not found | Driver not installed | Reinstall driver, check Device Manager |

## Specifications

See the official datasheet for isolation, baud rates, and connector details:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2591).

## Related

- [NGX-1](./ngx-1.md) — the NMEA 2000 equivalent PC gateway
- [Actisense SDK](https://github.com/Actisense/SDK)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
