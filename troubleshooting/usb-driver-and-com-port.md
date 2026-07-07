# USB Driver & COM Port Issues

> When a USB Actisense device (NGX-1, NGT-1, USG-2) isn't detected or its COM port won't open.

**Applies to:** [NGX-1](../products/ngx-1.md), [USG-2](../products/usg-2.md), legacy [NGT-1](../products/ngt-1.md)

---

## Symptoms

- The device doesn't appear in your software's port list.
- The COM port exists but **won't open** ("access denied" / "port in use").
- The port number keeps changing between sessions.

## Cause 1 — Driver not installed

Actisense USB devices present as a virtual COM port and need the appropriate driver.

**Fix (Windows):**
- Open **Device Manager** and look under **Ports (COM & LPT)**.
- If the device shows with a warning triangle (or under "Other devices"), install/repair the
  driver from [actisense.com/support](https://actisense.com/support/).
- After installation, note the assigned **COMx** number.

## Cause 2 — Wrong or unknown COM port

Software often defaults to the wrong port.

**Fix:**
- In Device Manager, unplug/replug the device and watch which COM entry appears/disappears —
  that's your port.
- Select that exact port in your application.

## Cause 3 — Port already in use

A serial COM port can only be opened by **one application at a time**.

**Fix:**
- Close any other program that might hold the port (a previous instance of NMEA Reader, a
  charting app, a logger).
- Re-open the port in the app you actually want to use.

## Cause 4 — Port number keeps changing

Windows can assign a new COM number when a device is plugged into a different USB socket.

**Fix:**
- Use the **same USB port** each time, or set a fixed COM number in Device Manager
  (Port Settings → Advanced → COM Port Number).

## Related

- [No-data checklist](./no-data-checklist.md)
- [NGX-1 with your own application (SDK)](../integration-guides/ngx-1-sdk-getting-started.md)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
