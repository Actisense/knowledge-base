# NDC-4 — NMEA 0183 Multiplexer (Legacy)

> The long-serving intelligent NMEA 0183 multiplexer. Widely installed; succeeded by the PRO-range multiplexers.

| | |
|---|---|
| **Category** | NMEA 0183 Multiplexer |
| **Status** | Legacy (see [PRO-NDC-1E](./pro-ndc-1e.md) / [PRO-MUX-2](./pro-mux-2.md)) |
| **Connects** | Multiple NMEA 0183 devices ↔ combined NMEA 0183 output |
| **Product page** | https://actisense.com/products/ndc-4-nmea-0183-multiplexer/ |
| **Datasheet & manual** | [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-3174) |

---

## Overview

The NDC-4 was Actisense's established intelligent NMEA 0183 multiplexer, combining several
0183 talkers into managed outputs with prioritisation and filtering. It remains in wide use.
New installations should look at the PRO-range multiplexers
([PRO-NDC-1E](./pro-ndc-1e.md), [PRO-MUX-2](./pro-mux-2.md)), but existing NDC-4 units remain
serviceable.

## Key Features

- Intelligent multiplexing of multiple NMEA 0183 inputs
- Configurable prioritisation and filtering
- Per-port configurable baud rates
- Combined managed output(s)

## Connections & Interfaces

- **NMEA 0183:** Multiple input ports and combined output ports
- **Power:** Powered independently from its own dedicated supply (see datasheet for voltage range).
- **Configuration:** Via Actisense PC toolkit

## Getting Started

1. Wire each NMEA 0183 talker to a numbered input (mind polarity).
2. Connect the combined output(s) to your listener(s).
3. Configure baud rates, routing, and priorities with the Actisense toolkit.
4. Confirm all required sentences appear on the output.

## Software & Tools

- **Actisense Toolkit** — configuration, filtering, and firmware updates

## Firmware & Updates

Managed via the Actisense toolkit. Always run the latest —
see [actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-3174).

## Common Use Cases

- Existing installations built around the NDC-4
- Merging GPS, AIS, heading, and instrument data into one 0183 feed

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| Input not seen | Baud rate / polarity mismatch | Set correct per-port baud rate and wiring |
| Sentences dropped | Output throughput exceeded | Apply filtering / prioritisation |

## Specifications

See the official datasheet for port counts and power:
[actisense.com/downloads](https://actisense.com/downloads/?type=&products=.pro-3174).

## Related

- [PRO-NDC-1E](./pro-ndc-1e.md) — current type-approved replacement
- [PRO-MUX-2](./pro-mux-2.md) — current multiplexer

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
