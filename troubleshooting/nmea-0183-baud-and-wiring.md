# NMEA 0183 Baud Rate & Wiring

> Why NMEA 0183 devices show nothing or garbled data — almost always a baud-rate or wiring-polarity problem — and how to fix it.

**Applies to:** [USG-2](../products/usg-2.md), [WGX-1](../products/wgx-1.md), the PRO multiplexers/buffers, legacy [NDC-4](../products/ndc-4.md)

---

## Symptoms

- **Garbled / random characters** in your software's data monitor.
- **Nothing received at all**, even though the device is wired in.

## Cause 1 — Wrong baud rate (garbled data)

NMEA 0183 is asynchronous serial. If the baud rate doesn't match, you get well-formed-looking
but nonsense characters. The rule of thumb:

- **Standard NMEA 0183** (GPS, instruments, heading): **4800 baud**
- **AIS** (and other high-speed 0183): **38400 baud**

Set the baud rate to match the *talker*, in both your software and any Actisense port config.

## Cause 2 — Reversed polarity (nothing received)

NMEA 0183 is a differential pair (data-A/+ and data-B/-). If the two lines are swapped, you
typically receive **nothing**.

**Fix:** swap the two data wires. Wire **talker output + → listener input +**, and **- → -**.
Also connect a common ground/shield where provided.

## Cause 3 — Talker/listener direction

- A **talker** transmits; a **listener** receives. Make sure you've wired the source's *output*
  to the Actisense device's *input*.
- Some ports are input-only or output-only — check which is which for your device.

## How to diagnose

1. Enable your software's raw NMEA/data monitor.
2. **Random characters?** → fix the baud rate (Cause 1).
3. **Completely blank?** → swap polarity (Cause 2), confirm the talker is powered and actually
   transmitting, and confirm you're on the correct input port.

## Related

- [USG-2: AIS/GPS into PC charting](../integration-guides/usg-2-ais-to-pc-charting.md)
- [No-data checklist](./no-data-checklist.md)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
