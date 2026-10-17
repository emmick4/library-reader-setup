# Library Reader Setup

Connect your Xteink. The app identifies it, keeps a backup, and installs the matching Library firmware.

| Download | |
| --- | --- |
| [Mac (Apple silicon)](https://github.com/emmick4/library-reader-setup/releases/latest/download/Library-Reader-Setup-0.1.0-Mac-Apple-silicon.zip) | M-series Macs |
| [Mac (Intel)](https://github.com/emmick4/library-reader-setup/releases/latest/download/Library-Reader-Setup-0.1.0-Mac-Intel.zip) | Intel Macs |
| [Windows](https://github.com/emmick4/library-reader-setup/releases/latest/download/Library-Reader-Setup-0.1.0-Windows.exe) | One EXE; intentionally unsigned |

1. Connect the reader with a USB **data** cable.
2. Open **Library Reader Setup** and choose **Check reader**.
3. Choose **Back up and install**. Wait for **Library is ready**.

No Python or terminal is needed. Connect the reader to Wi-Fi, scan its QR code with your phone, and tap **Add reader**. Updating a connected reader keeps its pairing.

The app recognizes **X4 Pro**, **X4 Classic**, and the **original X4** automatically. You never select a model or firmware file. Unrecognized firmware stops safely without flash writes.

<details>
<summary>Supported factory firmware</summary>

| Reader | Recognized factory baseline |
| --- | --- |
| X4 Pro | English XT 7.5.11 |
| X4 Classic (X4 V2) | Manufacturer English XT/Licorice V1013 |
| Original X4 (ESP32-C3) | Manufacturer English XT V6.3.27 |

Reviewed Library installations are also recognized automatically. Matching checks include the actual chip and stock firmware fingerprints; a version label alone is insufficient. X3 and unfamiliar layouts are not supported.

X4 Pro has been tested on hardware. Classic and original X4 factory profiles are validated against manufacturer firmware; physical testing is pending.

</details>

Mac apps are signed and notarized. Windows is unsigned by choice. Complete [corresponding source](https://github.com/emmick4/library-reader-setup/releases/latest/download/Library-Reader-Setup-0.1.0-Sources.zip), [license](LICENSE), and [third-party notices](THIRD_PARTY_NOTICES.md) accompany the release. Downloads contain no Library account data or device backups.
