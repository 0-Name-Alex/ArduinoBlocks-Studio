# ArduinoBlocks Studio — AI Agent Guide

Single-file client-side **Google Blockly 10.4.3** visual IDE that transpiles block programs into **Arduino C++ (`.ino`)** and **`platformio.ini`** configurations across 6 microcontroller architectures, deployed on **GitHub Pages** (`0-Name-Alex/ArduinoBlocks-Studio`).

## 1. Architecture ([`index.html`](index.html))
Everything lives cleanly in [`index.html`](index.html) (no build toolchain required):
- **Board Profiles (`BOARD_PROFILES`)**: `uno`, `mega`, `esp32`, `esp8266`, `xiao_nrf52`, `pico` — controls dynamic dropdown pinouts (`digitalPins`, `pwmPins`, `analogPins`, `interruptPins`), `servoHeader`, `wifiHeader`, `baudRate`, and `platformio.ini` metadata.
- **Custom Generator (`ArduinoGenerator`)**: Accumulates deduplicated `#include`s (`includes_`), globals/helpers (`definitions_`), auto `pinMode`/`begin` calls (`setupCode_`), and PlatformIO dependencies (`pioDeps_`) before assembling `void setup()` and `void loop()`.
- **Persistence & Features**: `localStorage` autosave (`arduinoblocks_studio_state_v1`), `.ablocks` JSON project export/import, curated + `.h`-parsed custom libraries, Named Components, and Chromium **Web Serial Monitor** (`navigator.serial`).

## 2. Key Invariants & Rules
- Keep CDN scripts pinned (currently `blockly@10.4.3`) so generator APIs (`ArduinoGenerator.forBlock[...]`) never drift.
- Never apply `platformio.ini` `;` comment highlighting when `activeCodeTab === 'ino'` (semicolons in C++ `for (...)` loops must not highlight as comments).
- Keep board-specific C++ dialects accurate (e.g., `IRAM_ATTR` on ESP32/ESP8266 ISRs, `EEPROM.begin(512)` + `commit()` on ESP32/ESP8266/Pico vs `EEPROM.update()` on AVR, `WiFiClient` + `http.begin(client, url)` on ESP8266).
- Validate all `<xml>` blocks inside `PRESET_EXAMPLES` whenever editing presets.

## 3. Local Preview & Deployment
- **Preview locally**: `py -3.14 -m http.server 8080`
- **Git & GitHub Pages**: Push to `main` (`0-Name-Alex <0-Name-Alex@users.noreply.github.com>`); served automatically at [`https://0-name-alex.github.io/ArduinoBlocks-Studio/`](https://0-name-alex.github.io/ArduinoBlocks-Studio/).
