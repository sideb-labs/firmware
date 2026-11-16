# SideB Remote firmware

Firmware updates for the SideB Remote by SideB Labs.

The remote downloads these files itself (System › Update). You do not need to download anything
from here. Every image is listed in `manifest.json`, which is signed by SideB Labs; the remote
checks the signature and the SHA-256 of the image before it installs anything.

- `manifest.json`: current version, signed
- `oled-<version>.bin`, `colour-<version>.bin`: firmware images (binaries only; the source code is not public)
- `THIRD_PARTY_NOTICES.md` and `licenses/`: licences of the open-source components inside the firmware,
  including the offer for the LGPL-2.1 parts
