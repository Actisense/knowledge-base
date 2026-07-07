# "No Data" — First-Response Checklist

> A fast, ordered checklist to run through when an Actisense device shows no data. Start here before diving into product-specific articles.

**Applies to:** all Actisense gateways and interfaces

---

## Work through these in order

Most "no data" cases are resolved by one of the first few checks.

### 1. Power

- Is the device powered? (LED lit / appears in software / web interface reachable?)
- **NMEA 2000 devices** are powered *by the backbone* — if the backbone has no power, the
  device is dead. See [NMEA 2000 power & termination](./nmea-2000-power-and-termination.md).

### 2. The bus itself

- **NMEA 2000:** Is the backbone correctly **terminated** (a resistor at *each* end, two total)?
  An unterminated or single-terminated bus is a classic no-data cause.
- **NMEA 0183:** Is the wiring polarity correct, and the **baud rate** right (4800 standard,
  38400 for AIS)? See [NMEA 0183 baud & wiring](./nmea-0183-baud-and-wiring.md).

### 3. The connection to your PC / app

- **USB devices:** Is a **COM port** assigned and the **driver** installed? See
  [USB driver & COM port issues](./usb-driver-and-com-port.md).
- **Wi-Fi devices:** Are you on the **same network**, using the right **IP and port**, and the
  right transport (**TCP vs UDP**)?

### 4. Is there actually anything to see?

- Confirm a *talker* is present and transmitting (a lone gateway on a bus with no sensors has
  nothing to report).
- Cross-check with a second tool (e.g. [NMEA Reader](https://actisense.com/downloads/?type=&products=.pro-1881) or the
  gateway's web interface) to isolate whether the problem is the device or your software.

### 5. Firmware

- Run the **latest firmware** for your device — check
  [actisense.com/support](https://actisense.com/downloads/).

## Still stuck?

If you've cleared all five and still see nothing, capture what you *do* see (LED states, web
interface status, any partial data) and contact
[Actisense support](https://actisense.com/contact/).

## Related

- [NMEA 2000 power & termination](./nmea-2000-power-and-termination.md)
- [NMEA 0183 baud & wiring](./nmea-0183-baud-and-wiring.md)
- [USB driver & COM port issues](./usb-driver-and-com-port.md)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
