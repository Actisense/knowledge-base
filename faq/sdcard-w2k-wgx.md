# FAQ-1: SD Card Guidance for WGX-1, W2K-1, and W2K-2

## Overview

These devices log to a **FAT32-formatted SD card**. They do **not** support ExFAT.

## Recommended Cards

**SDHC cards of 32 GB or smaller.**

These are pre-formatted as FAT32 from the factory and will work without any preparation.

> **Note:** An SD card sold as "32 GB" will be reported by the device as approximately 29.7 GB. This is the standard difference between the manufacturer's decimal sizing and the binary sizing used by file systems — it is not a fault.

## Supported With Preparation: 64 GB and 128 GB SDXC Cards

Windows ships these cards as ExFAT and will not, by default, let you reformat them as FAT32. To use one of these cards you must reformat it as **FAT32 with a 64 KB allocation unit size**. This requires a third-party utility, for example:

- **FAT32 Format** (guiformat), or
- `format /FS:FAT32 /A:64K` from an elevated command prompt (on some Windows versions).

Once correctly formatted, the card will log normally.

> **Note:** The free-space figure shown on the device's web interface may not match the true free space on these larger cards. Logging itself is unaffected.

## Cards Above 64 GB

Not currently recommended.

## General Advice

- Avoid letting the card fill completely.
- Leave at least a few megabytes free — the web interface may become unresponsive when the card is almost full, even though the underlying device continues to work.

## Notes / Open Items

- Webapp drive-space display on 64 GB / 128 GB cards is still inaccurate — known issue, not addressed by this guidance.
- 128 GB confirmed working on W2K with fw 1.398.3436 with FAT32 formatting
