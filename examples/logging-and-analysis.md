# Logging a Voyage and Analysing It Later

> Capture a full NMEA session to a log file, then replay and analyse it on your PC — for diagnostics, development, or reviewing a trip.

| | |
|---|---|
| **Products used** | [W2K-2](../products/w2k-2.md)/[WGX-1](../products/wgx-1.md) (SD logging) or [NGX-1](../products/ngx-1.md)/[NGT-1](../products/ngt-1.md) (PC logging) |
| **Also needs** | An SD card (for gateway logging) or PC software / the SDK |
| **Difficulty** | Beginner–Intermediate |

---

## What you'll build

A recorded log of everything on your network that you can replay later — useful for chasing an
intermittent fault, testing software against real data without being on the boat, or reviewing
a passage.

## Two ways to log

### A. Onboard, to SD card (W2K-2 / WGX-1)

These gateways log directly to an SD card with no PC required.

1. Fit a correctly formatted SD card — **FAT32, 32 GB or smaller** is the no-fuss choice.
   See [SD Card Guidance](../faq/faq-1.md) for larger cards and formatting.
2. Enable logging in the gateway's web interface.
3. Go sailing. The gateway records as it runs.
4. Remove the card (or download via the web interface) and copy the logs to your PC.

> Leave some free space on the card — a completely full card can make the web interface
> unresponsive even though logging continues. See [SD Card Guidance](../faq/faq-1.md).

### B. On the PC, via a gateway (NGX-1 / NGT-1)

With a PC connected, log using Actisense tools or your own SDK application.

1. Connect the [NGX-1](../products/ngx-1.md) to the network and PC.
2. Use [Actisense NMEA Reader](https://actisense.com/support/) (or an SDK app) to record.
3. The Actisense **EBL (Enhanced Binary Log)** format is designed for recording *and replay* —
   see the SDK docs for working with EBL programmatically.

## Analysing / replaying

- **Replay** an EBL log back through the SDK to feed recorded data into software as if it were
  live — ideal for developing and testing without the boat.
- **Decode** logs to inspect specific PGNs/sentences when chasing a fault.

## Ideas to extend it

- Script a decoder in Python (via the SDK) to extract just the PGNs you care about to CSV.
- Correlate an intermittent dropout in the log with the
  [power & termination](../troubleshooting/nmea-2000-power-and-termination.md) checks.

## Related

- [NGX-1 with your own application (SDK)](../integration-guides/ngx-1-sdk-getting-started.md)
- [Actisense SDK](https://github.com/Actisense/SDK) — BST, PGN, and EBL documentation
- [SD Card Guidance](../faq/faq-1.md)

## Support

- 📖 **Documentation:** [actisense.com/downloads](https://actisense.com/downloads/)
- 🐛 **Report issues:** Open an issue in this repository
- 📧 **Contact us:** [actisense.com/contact](https://actisense.com/contact/)
