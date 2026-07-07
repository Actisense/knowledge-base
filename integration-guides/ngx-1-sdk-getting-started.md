# NGX-1 with Your Own Application (via the Actisense SDK)

> Read and write NMEA 2000 data from your own C++ or Python application using an NGX-1 (or NGT-1) and the Actisense SDK.

| | |
|---|---|
| **Products used** | [NGX-1](../products/ngx-1.md) (or legacy [NGT-1](../products/ngt-1.md)) |
| **Target** | A custom application built with the [Actisense SDK](https://github.com/Actisense/SDK) |
| **Difficulty** | Intermediate |
| **You will need** | NGX-1, a powered & terminated NMEA 2000 network, a PC, a C++/Python toolchain |

---

## Overview

The NGX-1 exposes an NMEA 2000 network to a PC over a serial/USB link. The Actisense SDK
speaks the protocols that run over that link, so your application can decode incoming
NMEA 2000 messages and transmit onto the bus. This guide gets you from a connected NGX-1 to a
program that prints live data.

## How the pieces fit together

Your app talks to the SDK; the SDK frames and parses the serial data to and from the NGX-1:

```
Your app  ⇄  Actisense SDK  ⇄  NGX-1  ⇄  NMEA 2000 backbone
```

Key protocol layers you'll encounter in the SDK docs:

- **BDTP** — the DLE-escaped binary framing used on all Actisense serial links (the transport).
- **BST (Binary Serial Transfer)** — the datagram/message layer carried over BDTP; **BST-BEM** adds an extended command framework.
- **NMEA 2000 / PGNs** — reassembled application messages you actually consume (each carries a PGN identifying its content).

You generally work at the NMEA 2000/PGN level; the SDK handles BDTP/BST framing for you.

## Prerequisites

- An NGX-1 connected to a **powered and correctly terminated** NMEA 2000 backbone
  (see [NMEA 2000 power & termination](../troubleshooting/nmea-2000-power-and-termination.md)).
- The NGX-1 recognised by your PC on a known COM port
  (see [USB driver & COM port issues](../troubleshooting/usb-driver-and-com-port.md)).
- A build toolchain: a C++17 compiler + CMake, or Python — the SDK is primarily C++ with Python bindings.

## Step 1 — Get the SDK

```bash
git clone https://github.com/Actisense/SDK.git
cd SDK
```

Read `docs/README.md` in the repo first — it is the authoritative index for the protocol
docs (BDTP, BST, BST-BEM, EBL logging) and the current build instructions.

## Step 2 — Build the SDK

The SDK uses **CMake**. Follow the build steps in the repository's documentation for your
platform (Windows/Linux/macOS). At a high level:

```bash
cmake -S . -B build
cmake --build build
```

> Always follow the repo's own build instructions — they take precedence over this summary.

## Step 3 — Open the NGX-1 and read messages

Point the SDK at the NGX-1's serial port and open a session. Then run your read loop and
decode the NMEA 2000 messages as they arrive. Start from the SDK's example programs rather
than writing framing code yourself — the examples show the correct open/read/decode pattern
for both C++ and Python.

## Step 4 — (Optional) Transmit onto the network

Once you can read, you can construct and send NMEA 2000 messages. Be deliberate about this on
a live vessel network — only transmit PGNs you understand, and test on a bench network first.

## Verifying It Works

- Run [Actisense NMEA Reader](https://actisense.com/support/) alongside your build to
  confirm the NGX-1 sees traffic independently of your code.
- Your program should print a steady stream of PGNs (e.g. position, speed, depth) matching
  what NMEA Reader shows.

## Troubleshooting

| Symptom | Likely cause | Resolution |
|---|---|---|
| Port opens but no messages | Backbone not powered/terminated | [Power & termination](../troubleshooting/nmea-2000-power-and-termination.md) |
| Port won't open / not found | Driver or COM-port issue | [USB driver & COM port](../troubleshooting/usb-driver-and-com-port.md) |
| Garbage/partial frames | Bypassing SDK framing | Use the SDK's parser — don't read raw bytes directly |
| Build fails | Toolchain/CMake mismatch | Follow the SDK repo's platform build notes |

## Related

- [NGX-1 product page](../products/ngx-1.md) · [NGT-1 (legacy)](../products/ngt-1.md)
- [Actisense SDK](https://github.com/Actisense/SDK)
- [Logging & analysis with EBL](../examples/logging-and-analysis.md)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
