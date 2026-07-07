# A Raspberry Pi Boat Server with Signal K

> Turn a Raspberry Pi and an Actisense gateway into an onboard data server — a dashboard, logger, and bridge for your NMEA 2000 network.

| | |
|---|---|
| **Products used** | [NGX-1](../products/ngx-1.md)/[NGT-1](../products/ngt-1.md) (USB) or [W2K-2](../products/w2k-2.md) (network) |
| **Also needs** | A Raspberry Pi, [Signal K](https://signalk.org/) server (third-party, open source) |
| **Difficulty** | Intermediate |

---

## What you'll build

A small always-on server on the boat that reads your NMEA 2000 network via an Actisense
gateway and serves web dashboards, logs data, and can bridge it to apps and the cloud.

```
NMEA 2000  ⇄  Actisense gateway  ⇄  Raspberry Pi (Signal K)  ⇄  phones / tablets / apps
```

> **Note:** Signal K is an independent open-source project, not an Actisense product. This
> recipe shows how an Actisense gateway feeds it; follow Signal K's own docs for its setup.

## Ingredients

- A Raspberry Pi (with power and, ideally, a case suited to the boat).
- An Actisense gateway:
  - **USB route:** [NGX-1](../products/ngx-1.md) or legacy [NGT-1](../products/ngt-1.md) plugged into the Pi.
  - **Network route:** [W2K-2](../products/w2k-2.md) sharing data over the network the Pi is on.
- Signal K server installed on the Pi.

## Method

1. **Connect the gateway.**
   - *USB:* plug the NGX-1 into the Pi; note its serial device (e.g. `/dev/ttyUSB0`). See
     [USB driver & COM port issues](../troubleshooting/usb-driver-and-com-port.md) if it doesn't appear.
   - *Network:* put the W2K-2 and Pi on the same network and note the gateway's IP/port.
2. **Add the data source in Signal K.** In Signal K's admin UI, add a new connection:
   - *USB:* an NMEA 2000 (Actisense/serial) source pointing at the device path.
   - *Network:* a TCP/UDP source pointing at the W2K-2's IP and port.
3. **Confirm data flows.** Signal K's data browser should populate with vessel values.
4. **Add dashboards / plugins** as you like from the Signal K app store.

## Result

A browsable onboard dashboard, plus logging and app-bridging — all fed live from your
NMEA 2000 network through the Actisense gateway.

## Ideas to extend it

- Auto-start Signal K on boot so the server is ready whenever the boat powers up.
- Log to disk on the Pi in parallel with the gateway's own [SD logging](../examples/logging-and-analysis.md).
- Feed data onward to a phone app over Wi-Fi.

## Related

- [Getting wireless NMEA data into an app](../integration-guides/wireless-nmea-data-into-an-app.md)
- [NGX-1](../products/ngx-1.md) · [W2K-2](../products/w2k-2.md)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
