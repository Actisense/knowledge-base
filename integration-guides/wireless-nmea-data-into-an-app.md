# Getting Wireless NMEA Data into an App (W2K-2 / WGX-1)

> Stream live NMEA data from a W2K-2 or WGX-1 over Wi-Fi into a chartplotter app or your own software using a TCP/UDP connection.

| | |
|---|---|
| **Products used** | [W2K-2](../products/w2k-2.md) or [WGX-1](../products/wgx-1.md) |
| **Target** | A navigation app (phone/tablet) or custom software over the network |
| **Difficulty** | Beginner–Intermediate |
| **You will need** | A W2K-2/WGX-1 on a powered network, a device on the same Wi-Fi, a client app |

---

## Overview

The W2K-2 and WGX-1 publish vessel data onto Wi-Fi/Ethernet as a network data stream. Most
marine apps connect by pointing at the gateway's IP address and a port; the transport is
usually **TCP** (reliable, ordered) or **UDP** (lightweight broadcast). This guide covers the
general connection pattern — the exact ports and output formats are configured in the
gateway's web interface.

## Prerequisites

- The gateway connected to a **powered and terminated** NMEA 2000 backbone
  (and, for WGX-1, any NMEA 0183 devices wired in).
- Your phone/tablet/PC joined to the **same network** as the gateway — either the gateway's
  own access point or your onboard router if the gateway is in client mode.

## Step 1 — Find the gateway on the network

1. Join the gateway's Wi-Fi (access-point mode) or your onboard Wi-Fi (client mode).
2. Open the gateway's **web interface** in a browser (its address is shown in the product's
   quick-start; on its own AP it's typically a fixed IP).
3. Note the gateway's **IP address** and the **output port(s)** it is serving.

## Step 2 — Choose the output format and transport

In the web interface, confirm which data format and transport the gateway is outputting
(e.g. an NMEA data stream over TCP or UDP on a given port). Match this to what your client
app expects. If your app supports both, **TCP** is the safer default for a single device.

## Step 3 — Connect the client

In your app's connection settings, add a network/TCP (or UDP) source and enter:

- **Host / IP:** the gateway's IP address from Step 1
- **Port:** the output port from Step 1

Save and connect.

## Verifying It Works

- The app should show live position, speed, depth, wind, AIS, etc.
- The gateway's web interface usually shows client connections and data activity — confirm
  your device appears and traffic is flowing.

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| Can't reach the web interface | Not on the same network | Re-check Wi-Fi; confirm AP vs client mode |
| Connected but no data | Backbone not powered/terminated | [Power & termination](../troubleshooting/nmea-2000-power-and-termination.md) |
| App can't connect to port | Wrong port or transport (TCP vs UDP) | Re-check the web interface output settings |
| WGX-1: missing 0183 data | Baud/wiring issue | [NMEA 0183 baud & wiring](../troubleshooting/nmea-0183-baud-and-wiring.md) |

## Related

- [W2K-2](../products/w2k-2.md) · [WGX-1](../products/wgx-1.md)
- [SD Card Guidance](../faq/faq-1.md) — for onboard logging on these gateways

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
