# NGT-1 — NMEA 2000 to PC Gateway (Legacy)

> The long-serving USB gateway between an NMEA 2000 network and a PC. Widely deployed; superseded by the NGX-1.

| | |
|---|---|
| **Category** | NMEA 2000 to PC Gateway |
| **Status** | Legacy (superseded by [NGX-1](./ngx-1.md)) |
| **Connects** | NMEA 2000 ↔ PC (USB, and ISO/serial variants) |
| **Product page** | https://actisense.com/products/ngt-1-nmea-2000-to-pc-interface/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2608) |

---

## Overview

The NGT-1 was Actisense's flagship NMEA 2000-to-PC interface for many years and remains in
very wide use. It provides bidirectional access to an NMEA 2000 network from a computer over
USB, and became a de-facto standard interface supported by a broad range of third-party marine
software. New installations should consider the [NGX-1](./ngx-1.md), but existing NGT-1 units
remain fully usable.

## Key Features

- Bidirectional NMEA 2000 ↔ PC interface over USB
- Broad third-party software support
- Works with Actisense NMEA Reader and the Actisense SDK
- Available in USB and ISO/serial variants

## Connections & Interfaces

- **NMEA 2000:** Micro-C drop connection to the backbone
- **PC:** USB (NGT-1-USB) or serial/ISO variant
- **Power:** The **NGT-1-USB** is powered from USB; the **ISO** variant is powered from the NMEA 2000 backbone.

## Getting Started

1. Connect the NGT-1 to a powered, terminated NMEA 2000 backbone.
2. Connect to the PC and install the Actisense driver if prompted.
3. Open NMEA Reader (or your SDK application) and select the NGT-1 COM port.
4. Confirm live PGN traffic is visible.

## Software & Tools

- **Actisense NMEA Reader** — view and decode NMEA 2000 traffic
- **Actisense Toolkit** — configuration and diagnostics
- **[Actisense SDK](https://github.com/Actisense/SDK)** — build custom applications

## Firmware & Updates

Firmware and drivers are managed via Actisense PC tools. Always run the latest —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2608).

## Common Use Cases

- Existing NMEA 2000 software installations built around the NGT-1
- Diagnostics and logging from a PC
- SDK-based application development

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| Device not detected | Driver not installed / wrong COM port | Reinstall driver, check Device Manager |
| No traffic | Backbone not powered/terminated | Verify NMEA 2000 power and termination |
| Cannot transmit | App TX not configured | Check application transmit settings |

## Specifications

See the official datasheet for supported protocols, power, and LEN:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2608).

## Related

- [NGX-1](./ngx-1.md) — the current replacement
- [Actisense SDK](https://github.com/Actisense/SDK)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
