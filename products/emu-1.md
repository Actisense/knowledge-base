# EMU-1 — Engine Monitoring Unit

> Converts analogue engine gauge signals into NMEA 2000 data, bringing older engines onto a modern digital network.

| | |
|---|---|
| **Category** | NMEA 2000 Engine Monitoring Unit |
| **Status** | Current |
| **Connects** | Analogue engine senders ↔ NMEA 2000 |
| **Product page** | https://actisense.com/products/emu-1-nmea-2000-engine-data/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2605) |

---

## Overview

The EMU-1 reads the analogue signals from a traditional engine's gauges and senders —
such as RPM, temperature, oil pressure, and voltages — and publishes them onto an NMEA 2000
network. This lets owners of older or non-digital engines display engine data on a modern
NMEA 2000 chartplotter or MFD without replacing the engine's instrumentation.

## Key Features

- Converts multiple analogue engine inputs to NMEA 2000
- Supports voltage, resistive, and tachometer-type inputs
- Configurable calibration to match a wide range of sender types

## Connections & Interfaces

- **Engine side:** Screw-terminal inputs for analogue gauge/sender signals and tacho pickup
- **NMEA 2000:** Micro-C drop connection to the backbone (powers the CAN interface only)
- **Power:** Requires its own supply on the **VE+ / VE−** terminals. Only the CAN interface is powered by the NMEA 2000 network — the unit itself is not.

## Getting Started

1. Identify the engine's sender types and signal ranges.
2. Wire the relevant senders to the EMU-1 inputs.
3. Connect the EMU-1 to the NMEA 2000 backbone.
4. Calibrate each channel using the Actisense configuration tool to match your senders.
5. Confirm readings on your MFD/display.

## Software & Tools

- **Actisense EMU configuration tool / Toolkit** — assign inputs, set sender curves, and calibrate

## Firmware & Updates

Firmware and configuration are managed via Actisense PC tools. Always run the latest —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2605).

## Common Use Cases

- Displaying an older engine's data on a modern NMEA 2000 MFD
- Adding engine monitoring to a vessel without digital engine electronics
- Logging engine parameters alongside other NMEA 2000 data

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| Incorrect readings | Sender curve not calibrated | Recalibrate the channel for the actual sender type |
| No RPM | Wrong tacho input source or scaling | Check pickup source and configure pulses/rev |
| No data on network | Backbone not powered/terminated | Verify NMEA 2000 power and termination |

## Specifications

See the official datasheet for input types, channel count, and calibration ranges:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-2605).

## Related

- [Integration guides](../integration-guides/) — engine data display setups

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
