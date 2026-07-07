# NGX-1 — NMEA 2000 Gateway

> A dual-mode NMEA 2000 gateway: a PC interface for viewing/logging/developing (Transfer mode), or a standalone NMEA 0183 ↔ NMEA 2000 converter (Convert mode).

| | |
|---|---|
| **Category** | NMEA 2000 to PC Gateway / NMEA 0183 ↔ NMEA 2000 Converter |
| **Status** | Current |
| **Connects** | NMEA 2000 ↔ PC (USB) · NMEA 0183 ↔ NMEA 2000 |
| **Product page** | https://actisense.com/products/nmea-2000-gateway-ngx-1/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-16546) |

---

## Overview

The NGX-1 is the successor to the popular NGT-1, and combines two gateways in one device. It
has two selectable operating modes, so it can act either as an NMEA 2000-to-PC interface *or*
as a standalone NMEA 0183 ↔ NMEA 2000 converter — effectively replacing both the NGT-1 and the
NGW-1. The mode is chosen using Actisense configuration software.

## Operating Modes

The NGX-1 operates in one of two modes at a time. Select the mode with the Actisense
configuration software (see the manual for the exact procedure).

### Transfer mode (like the [NGT-1](./ngt-1.md))

Acts as an **NMEA 2000-to-PC gateway**. Software on the connected computer gets full
bidirectional access to the NMEA 2000 network — reading live PGNs and, where appropriate,
transmitting onto the bus. This is the mode for diagnostics, logging, and developing NMEA 2000
applications with the [Actisense SDK](https://github.com/Actisense/SDK).

### Convert mode (like the [NGW-1](./ngw-1.md))

Acts as a **standalone NMEA 0183 ↔ NMEA 2000 converter**. It translates between the two
standards so legacy NMEA 0183 equipment can share data with an NMEA 2000 network (and vice
versa), running independently without a PC attached once configured.

## Key Features

- Two selectable operating modes (Transfer and Convert) in a single device
- **Transfer:** bidirectional NMEA 2000 ↔ PC interface over USB
- **Convert:** standalone NMEA 0183 ↔ NMEA 2000 conversion
- Works with Actisense NMEA Reader and the Actisense SDK (Transfer mode)

## Connections & Interfaces

- **NMEA 2000:** Micro-C drop connection to the backbone
- **PC / serial:** USB connection to the host computer (also carries the NMEA 0183 serial data used in Convert mode)
- **Power:** Powered exclusively from the NMEA 2000 network on **both** the ISO and USB variants — **not** from USB.
- See the manual for the exact NMEA 0183 wiring used in Convert mode

## Getting Started

1. Connect the NGX-1 to a drop on a powered, terminated NMEA 2000 backbone.
2. Connect the USB cable to your PC and install/allow the driver if prompted.
3. Using the Actisense configuration software, **select the operating mode** you need
   (Transfer or Convert).
4. **Transfer mode:** open Actisense NMEA Reader (or your own SDK application), select the
   NGX-1 port, and confirm live PGN traffic.
   **Convert mode:** configure the conversion, then confirm data crosses between the NMEA 0183
   and NMEA 2000 sides.

## Software & Tools

- **Actisense NMEA Reader** — view and decode live NMEA 2000 traffic
- **Actisense Toolkit** — configuration and diagnostics
- **[Actisense SDK](https://github.com/Actisense/SDK)** — build your own applications (C, C++, Python)

## Firmware & Updates

Firmware and drivers are managed via Actisense PC tools. Always run the latest —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-16546).

## Common Use Cases

- **Transfer:** developing and testing NMEA 2000 software with the SDK
- **Transfer:** diagnosing and logging network traffic from a laptop
- **Transfer:** bridging NMEA 2000 data into a PC-based application
- **Convert:** sharing legacy NMEA 0183 instrument data onto an NMEA 2000 network
- **Convert:** feeding NMEA 2000 data to an older NMEA 0183 display or autopilot

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| Device not detected (Transfer) | Driver not installed / wrong COM port | Reinstall driver, check port in Device Manager |
| No traffic seen | Backbone not powered or terminated | Verify NMEA 2000 power and termination |
| Cannot transmit | App not configured for TX / conflicting source | Check app settings and network addressing |
| Software can't connect | Device is in Convert mode | Switch to Transfer mode in the Actisense config software |
| No conversion happening | Device is in Transfer mode, or conversion not configured | Switch to Convert mode and set up the conversion |

## Specifications

See the official datasheet for supported protocols, power, and LEN:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-16546).

## Related

- [NGT-1](./ngt-1.md) — the PC-gateway predecessor (equivalent to Transfer mode)
- [NGW-1](./ngw-1.md) — the legacy NMEA 0183 ↔ NMEA 2000 converter (equivalent to Convert mode)
- [WGX-1](./wgx-1.md) — Wi-Fi gateway that also does NMEA 0183 ↔ NMEA 2000 conversion
- [Actisense SDK](https://github.com/Actisense/SDK)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
