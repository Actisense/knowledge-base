# NGW-1 — NMEA 0183 to NMEA 2000 Gateway (Legacy)

> The long-serving standalone NMEA 0183 ↔ NMEA 2000 converter. Legacy, but still very heavily used for retrofitting NMEA 2000 onto boats with legacy NMEA 0183 equipment.

| | |
|---|---|
| **Category** | NMEA 0183 ↔ NMEA 2000 Converter |
| **Status** | Legacy (conversion role now also offered by the [NGX-1](./ngx-1.md) in Convert mode) |
| **Connects** | NMEA 0183 ↔ NMEA 2000 |
| **Product page** | https://actisense.com/products/nmea-2000-gateway-ngw-1/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2614) |

---

## Overview

The NGW-1 bridges an NMEA 2000 network with older NMEA 0183 electronics, converting data
between the two standards so legacy instruments can share data with a modern NMEA 2000 network
(and vice versa). It has one of the largest ranges of conversions available, and remains a
popular, cost-effective way to retrofit NMEA 2000 without replacing existing NMEA 0183 kit.

Multiple NGW-1 units can be used together to bring several NMEA 0183 devices onto a single
NMEA 2000 network.

> The [NGX-1](./ngx-1.md) now offers the same conversion function in its **Convert mode** (as
> well as an NGT-1-style PC-gateway "Transfer" mode). Existing NGW-1 units remain fully usable.

## Variants

The NGW-1 ships in several configurations — pick the one that matches your wiring:

| Variant | Description |
|---|---|
| **NGW-1-ISO** | Standard option — opto-isolated NMEA 0183 input and ISO-Drive output |
| **NGW-1-USB** | NMEA 0183 over USB for bidirectional connection to a PC / NMEA 0183 software |
| **NGW-1-STNG** | As the ISO variant, plus an STNG (SeaTalk NG) to NMEA 2000 adapter cable |

> See Actisense's "[Which NGW-1 do I need?](https://actisense.com/which-ngw-1-do-i-need/)"
> guidance if you're unsure which variant suits your installation.

## Key Features

- Standalone NMEA 0183 ↔ NMEA 2000 conversion (no PC required in normal operation)
- One of the widest conversion ranges available
- Multiple units can combine several NMEA 0183 sources onto one NMEA 2000 network
- Available in ISO, USB, and STNG variants
- Configurable using Actisense Toolkit

## Connections & Interfaces

- **NMEA 2000:** Micro-C drop connection to the backbone
- **NMEA 0183:** Serial input/output (opto-isolated on the ISO/STNG variants; USB on the USB variant)
- **STNG variant:** additional SeaTalk NG adapter cable
- **Power:** The **NGW-1-USB** is powered from USB; the **NGW-1-ISO** and **-STNG** variants are powered from the NMEA 2000 backbone.

## Getting Started

1. Choose the correct variant for your wiring (see the table above).
2. Wire the NMEA 0183 device(s) to the NGW-1 and connect it to a powered, terminated
   NMEA 2000 backbone.
3. Configure the required conversions using **Actisense Toolkit** (see the manual).
4. Confirm data crosses between the NMEA 0183 and NMEA 2000 sides.

## Software & Tools

- **Actisense Toolkit** — set up conversions, direction, and options; apply firmware updates

## Firmware & Updates

Firmware and configuration are managed via Actisense Toolkit. Always run the latest —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2614).

## Common Use Cases

- Retrofitting NMEA 2000 onto a boat that still has NMEA 0183 instruments
- Bringing a legacy NMEA 0183 GPS, AIS, or heading source onto an NMEA 2000 network
- Driving an older NMEA 0183 display or autopilot from NMEA 2000 data

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| No conversion happening | Conversion not configured in Toolkit | Configure the required conversions and directions |
| No NMEA 0183 data in | Wrong baud rate or reversed polarity | See [NMEA 0183 baud & wiring](../troubleshooting/nmea-0183-baud-and-wiring.md) |
| No NMEA 2000 data | Backbone not powered/terminated | See [NMEA 2000 power & termination](../troubleshooting/nmea-2000-power-and-termination.md) |
| Wrong variant for the install | e.g. expecting USB on an ISO unit | Check which variant you have against the table above |

## Specifications

See the official datasheet for the full conversion list, isolation, power, and LEN:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2614).

## Related

- [NGX-1](./ngx-1.md) — current gateway that offers this conversion in **Convert mode**
- [WGX-1](./wgx-1.md) — Wi-Fi gateway that also does NMEA 0183 ↔ NMEA 2000 conversion
- [NMEA 0183 baud & wiring](../troubleshooting/nmea-0183-baud-and-wiring.md)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
