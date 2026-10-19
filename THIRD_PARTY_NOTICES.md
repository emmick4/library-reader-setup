# Library Reader Setup redistribution

This standalone installer is GPL-3.0-or-later. Its scope is only
`tools/reader-installer`; no Library server/client/account code or personal device
backup is part of this distribution. The complete license is in `LICENSE`.

The build collects the exact installed dependency license texts and versions into
the app's `library_installer/resources/licenses` directory, including CPython's
license. Qt libraries remain separate shared libraries in the application bundle.
The Qt wheels omit their full component attribution texts. The packaging license
directory therefore retains original license/copyright/attribution files from
the exact hash-pinned Qt/PySide source archives. Mac uses Qt/PySide 6.9.3;
Windows uses 6.12.0. Their provenance binds the retained files and source archives;
the build checks them and Qt's runtime version before copying. The source companion
contains both platform versions, with maps for reconstructing each installer.
The Mac package also retains CPython 3.13.3's original incorporated-software notices
and corresponding source.

| Component | Pinned version | License / upstream source |
|---|---|---|
| esptool | 5.6.0 | GPL-2.0-or-later; <https://github.com/espressif/esptool/tree/v5.6.0> |
| PySide6-Essentials and shiboken6 | Mac 6.9.3; Windows 6.12.0 | LGPL-3.0 / GPL / Qt commercial terms; <https://code.qt.io/cgit/pyside/pyside-setup.git/> |
| Qt runtime | Mac 6.9.3; Windows 6.12.0 | Module-specific licenses and upstream notices retained; <https://code.qt.io/cgit/qt/> |
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
