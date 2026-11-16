# Third-party notices — SideB Remote firmware (SideB Labs)

The SideB Remote firmware (all models) contains the third-party software listed
below. Each item keeps its own licence. The full licence texts are in the
[`licenses/`](licenses/) folder; ship this file and that folder (for example in
the box, in the manual, or on the product web page) with every firmware build
that is distributed.

The rest of the firmware (`src/`, `lib/ThaiText/`) is the author's own code and
is not covered by these licences.

Versions are the ones pinned in `platformio.ini` (`platform = espressif32@7.1.3`,
Arduino-ESP32 2.0.17 on ESP-IDF v4.4.7).

## Libraries compiled into the firmware

| Component | Version | Licence | Copyright | Text |
|---|---|---|---|---|
| ArduinoJson | 6.18.0 | MIT | Copyright © 2014-2021 Benoit Blanchon | `licenses/ArduinoJson-MIT.txt` |
| Adafruit GFX Library | 1.10.12 | BSD (2-clause style) | Copyright (c) 2012 Adafruit Industries | `licenses/Adafruit-GFX-BSD.txt` |
| Adafruit SSD1306 | 2.5.7 | BSD (2-clause style) | Copyright (c) 2012, Adafruit Industries | `licenses/Adafruit-SSD1306-BSD.txt` |
| Adafruit BusIO | 1.9.6 | MIT | Copyright (c) 2017 Adafruit Industries | `licenses/Adafruit-BusIO-MIT.txt` |
| U8g2 (code) | 2.32.10 | BSD 2-clause | Copyright (c) 2016, olikraus@gmail.com | `licenses/U8g2-BSD.txt` |
| WiFiManager | 2.0.17 | MIT | Copyright (c) 2015 tzapu | `licenses/WiFiManager-MIT.txt` |
| LovyanGFX (colour models only) | 1.1.16 | FreeBSD, with MIT/BSD parts from Adafruit and others listed in its licence file | Copyright (c) lovyan03 and contributors | `licenses/LovyanGFX.txt` |
| JPEGDEC (progressive JPEG covers) | 1.8.4 | Apache License 2.0 | Copyright 2020 BitBank Software, Inc. | `licenses/JPEGDEC-Apache-2.0.txt` |

## Fonts compiled into the firmware

| Font | Used for | Licence | Text |
|---|---|---|---|
| ETL fixed Thai 14/16 (`u8g2_font_etl14thai_t`, `u8g2_font_etl16thai_t`, via U8g2) | Thai text on the OLED | Public domain ("Public domain font. Share and enjoy.") | — |
| efont Biwidth 12 (`u8g2_font_b12_t_japanese3`, via U8g2) | Japanese / kanji fallback | BSD 3-clause, (c) 2000-2003 /efont/ The Electronic Font Open Laboratory; 12-px source bitmaps are public domain (K12, shinonome, 6x12) or under the Baekmuk notice (Hwan Design Inc.) | `licenses/efont-BSD.txt` |
| Adafruit GFX built-in 5x7 font (`glcdfont`) | small ASCII text | BSD, as Adafruit GFX | `licenses/Adafruit-GFX-BSD.txt` |
| Sarabun (converted to bitmaps in `src/font_th20.h`, `src/font_th24.h`; colour models) | Thai text on the colour screen | SIL Open Font License 1.1, Copyright 2018 The Sarabun Project Authors | `licenses/Sarabun-OFL-1.1.txt` |

## Platform: Arduino-ESP32 core and ESP-IDF

| Component | Licence | Text |
|---|---|---|
| Arduino-ESP32 core 2.0.17 (cores/esp32 and the bundled libraries WiFi, WiFiClient, HTTPClient, ArduinoOTA, Update, Preferences, SPIFFS/FS, Wire, SPI, ESPmDNS) | **GNU LGPL 2.1** (see the offer below) | `licenses/LGPL-2.1.txt` |
| ESP-IDF v4.4.7 (precompiled in the Arduino-ESP32 SDK) | Apache License 2.0 | `licenses/Apache-2.0.txt` |
| mbed TLS (part of ESP-IDF; SHA-1 and Base64 are called directly) | Apache License 2.0 | `licenses/Apache-2.0.txt` |
| FreeRTOS (part of ESP-IDF), Copyright (C) 2017 Amazon.com, Inc. or its affiliates | MIT | `licenses/FreeRTOS-MIT.txt` |
| lwIP TCP/IP stack (part of ESP-IDF), Copyright (c) 2001, 2002 Swedish Institute of Computer Science | BSD 3-clause | `licenses/lwIP-BSD.txt` |
| wpa_supplicant (part of ESP-IDF Wi-Fi), Copyright (c) 2002-2016 Jouni Malinen and contributors | BSD 3-clause | `licenses/wpa_supplicant-BSD.txt` |
| TJpgDec by ChaN (ESP32 ROM, `esp32/rom/tjpgd.h`, album covers), Copyright (C) 2011 ChaN | ChaN free licence | `licenses/TJpgDec-ChaN.txt` |
| newlib C library (toolchain) | BSD-style collection | `licenses/newlib.txt` |
| libgcc / libstdc++ (toolchain) | GPL 3 with the GCC Runtime Library Exception (allows non-GPL programs) | `licenses/GCC-runtime-exception.txt`, `licenses/GPL-3.0-for-GCC-runtime.txt` |

ESP-IDF contains more components than listed here. Its own list of third-party
copyrights for v4.4.7 is copied unchanged to `licenses/ESP-IDF-v4.4.7-COPYRIGHT.rst`
(Apache-2.0 documentation of ESP-IDF). Arduino-ESP32 2.0.17 is built on
ESP-IDF v4.4.7 (commit 38eeba213a, from the SDK's `versions.txt`).

## Offer for the LGPL-2.1 parts (Arduino-ESP32 core)

The firmware is linked with the Arduino-ESP32 core, which is licensed under the
GNU Lesser General Public License version 2.1. You may modify the core and
relink the firmware with your modified version. On request, for at least three
years from the date you received the device, we will provide for each firmware
version we have distributed:

- the object files and libraries of the firmware (everything except the
  Arduino-ESP32 core), and
- the exact link command and the `platformio.ini` used,

so that you can relink the firmware with a modified core. The source code of
the Arduino-ESP32 core itself is available from
https://github.com/espressif/arduino-esp32 (tag 2.0.17).

Contact: SideB Labs — sideblabs@gmail.com

## Not included

Earlier development versions linked GPL code (the Volumio, SocketIO, JSON,
Inflate, CharStream, LibDebug and UiElements libraries, ClickButton, GKScroll,
the GNU FreeFont FreeMono font and the WenQuanYi Chinese font) and the unused
MIT library LinkedList. None of these are part of the current firmware.
