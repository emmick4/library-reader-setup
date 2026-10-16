# Library Reader Setup redistribution

This standalone installer is GPL-3.0-or-later. Its scope is only
`tools/reader-installer`; no Library server/client/account code or personal device
backup is part of this distribution. The complete license is in `LICENSE`.

The build collects the exact installed dependency license texts and versions into
the app's `library_installer/resources/licenses` directory, including CPython's
license. Qt libraries remain separate shared libraries in the application bundle.
The Qt wheels omit their full component attribution texts. The packaging license
directory therefore retains 236 original license/copyright/attribution files from
the exact hash-pinned Qt6.12.0/PySide source archives. Their provenance binds every
file and all four source archives; the build checks them and Qt's runtime version
before copying. Matching full sources can be included in the source companion.

| Component | Pinned version | License / upstream source |
|---|---|---|
| esptool | 5.6.0 | GPL-2.0-or-later; <https://github.com/espressif/esptool/tree/v5.6.0> |
| PySide6-Essentials and shiboken6 | 6.12.0 | LGPL-3.0 / GPL / Qt commercial terms; <https://code.qt.io/cgit/pyside/pyside-setup.git/> |
| Qt runtime | 6.12.0 | Module-specific licenses retained from the wheel; <https://code.qt.io/cgit/qt/> |
| PyInstaller | 6.22.3 | GPL-2.0-or-later with bootloader exception; <https://github.com/pyinstaller/pyinstaller/tree/v6.22.3> |
| pyserial | 3.5 | BSD-3-Clause; <https://github.com/pyserial/pyserial/tree/v3.5> |
| Library firmware / CrossInk | release manifest | Preserve its source archive, upstream commit/submodules, patch, SDK/font notices and build provenance. |

Every candidate includes `corresponding-source.zip` containing the standalone
installer source and packaging scripts. A distributable release must additionally
include the exact firmware, Qt/PySide and hash-verified Python dependency source
archives, and make corresponding sources and required notices available beside the
public download. A candidate missing them is not marked distribution-ready.

No signing certificate, private key, credential, NVS, SD contents or personal
reading data may be included. Local backup/receipt directories are created by the
running app outside the signed bundle and are never build inputs.
