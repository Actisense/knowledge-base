# Feeding AIS (or GPS) from a USG-2 into PC Charting Software

> Connect an NMEA 0183 AIS receiver or GPS to a PC via a USG-2 so charting software can display targets and position.

| | |
|---|---|
| **Products used** | [USG-2](../products/usg-2.md) |
| **Target** | PC charting software (OpenCPN, TimeZero, etc.) |
| **Difficulty** | Beginner |
| **You will need** | USG-2, an NMEA 0183 AIS/GPS source, a PC, charting software |

---

## Overview

A USG-2 presents an NMEA 0183 device to your PC as a serial (COM) port. Charting software
then reads sentences from that port. The single most common pitfall is the **baud rate**:
standard NMEA 0183 is **4800 baud**, but **AIS runs at 38400 baud**. Getting this wrong is the
usual cause of "no data" or garbled text.

## Prerequisites

- The USG-2 driver installed and a known COM port assigned
  (see [USB driver & COM port issues](../troubleshooting/usb-driver-and-com-port.md)).
- Your AIS/GPS output wires identified (data +/- and ground).

## Step 1 — Wire the NMEA 0183 source

Connect the device's NMEA 0183 output to the USG-2 input, observing polarity (data-A/+ to
input +, data-B/- to input -). Reversed polarity is a common "nothing received" cause.

## Step 2 — Set the correct baud rate

- **AIS receiver:** 38400 baud
- **GPS / standard instruments:** 4800 baud

Set this in your charting software's connection settings (and in the Actisense tool if you
configure the port there).

## Step 3 — Add the connection in your charting software

In the software's data-source/connection settings:

- **Type:** Serial
- **Port:** the USG-2's COM port
- **Baud:** as per Step 2

Enable it and, if offered, turn on the input/NMEA data monitor to watch raw sentences.

## Verifying It Works

- You should see raw sentences (e.g. `!AIVDM` for AIS, `$GPRMC`/`$GPGGA` for GPS) in the data monitor.
- AIS targets should begin to appear on the chart; GPS should show your position.

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| No data at all | Reversed polarity or dead source | Swap +/- wiring; confirm the source is powered |
| Garbled / random characters | Wrong baud rate | 38400 for AIS, 4800 for standard 0183 |
| No COM port | Driver not installed | [USB driver & COM port](../troubleshooting/usb-driver-and-com-port.md) |
| Sentences seen but no targets | App filtering / wrong source type | Check the app's AIS/source configuration |

## Related

- [USG-2 product page](../products/usg-2.md)
- [NMEA 0183 baud & wiring](../troubleshooting/nmea-0183-baud-and-wiring.md)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
