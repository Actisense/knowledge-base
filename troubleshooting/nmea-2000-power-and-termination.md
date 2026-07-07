# NMEA 2000 Power & Termination

> The two most common causes of NMEA 2000 network faults — no power on the backbone, and incorrect termination — and how to check them.

**Applies to:** all NMEA 2000 products ([NGX-1](../products/ngx-1.md), [W2K-2](../products/w2k-2.md), [WGX-1](../products/wgx-1.md), [EMU-1](../products/emu-1.md), legacy [NGT-1](../products/ngt-1.md)/[W2K-1](../products/w2k-1.md))

---

## Symptoms

- A device shows no data, or intermittently drops out.
- Devices appear only sometimes, or the whole network is unreliable.

## Background: how an NMEA 2000 network is built

An NMEA 2000 network is a **backbone** (trunk) with short **drop** cables to each device.
It has two hard rules that, when broken, cause most faults:

1. **One power source**, injected into the backbone (usually via a power T-piece).
2. **Two terminating resistors — one at each physical end of the backbone.** Not one, not three,
   and not at the drops.

## Cause 1 — No / insufficient power

NMEA 2000 devices draw their power *from the backbone*, not from their data connection to your
PC. If the backbone isn't powered (or the power T isn't fitted correctly), devices are simply dead.

**Check:**
- Confirm a power connection is fitted to the backbone and switched on.
- Measure roughly 12 V across the backbone power pins if you can.
- Check the network's total load (LEN) isn't exceeding what the supply provides.

## Cause 2 — Incorrect termination

The backbone must be terminated by a **120 Ω resistor at each end** (two total). Termination
sets the correct electrical characteristics for CAN; get it wrong and data becomes unreliable
or absent.

**Check (power off):**
- Measure resistance across the backbone data pins (CAN-H / CAN-L). With two 120 Ω terminators
  in parallel you should read **≈ 60 Ω**.
- **≈ 120 Ω** → only one terminator (add the second).
- **Open / very high** → no terminators.
- **Much lower than 60 Ω** → too many terminators, or a wiring fault.

## Fix

- Ensure exactly **one power injection** point and **two terminators**, one at each end.
- Replace damaged drop/backbone cables and re-seat connectors.
- Keep drop cables within spec length; overly long drops degrade the network.

## Related

- [No-data checklist](./no-data-checklist.md)
- [NMEA 2000 network range on actisense.com](https://actisense.com/products/?range=nmea-2000-network-range)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
