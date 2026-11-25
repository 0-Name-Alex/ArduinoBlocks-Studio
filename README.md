<h1 align="center">⚡ ArduinoBlocks Studio</h1>

<p align="center">
  <b>Universal Multi-Board Visual Block Coding IDE &amp; Real-Time Arduino C++ / PlatformIO Transpiler</b>
</p>

<p align="center">
  <a href="https://0-name-alex.github.io/ArduinoBlocks-Studio/"><img src="https://img.shields.io/badge/Launch-Live%20Web%20IDE-00979D?style=for-the-badge&logo=arduino&logoColor=white" alt="Live IDE" /></a>
  <img src="https://img.shields.io/badge/Engine-Blockly%2010.4.3-0284C7?style=for-the-badge" alt="Blockly" />
  <img src="https://img.shields.io/badge/Target-Arduino%20%7C%20ESP32%20%7C%20Pico-7C3AED?style=for-the-badge" alt="Boards" />
  <img src="https://img.shields.io/badge/License-MIT-success?style=for-the-badge" alt="MIT License" />
</p>

---

## 🌐 Use It Online (No Installation Needed)

👉 **Open Live IDE**: [**0-name-alex.github.io/ArduinoBlocks-Studio**](https://0-name-alex.github.io/ArduinoBlocks-Studio/)

Drag-and-drop visual blocks on the left, inspect real-time syntax-highlighted `.ino` C++ or `platformio.ini` on the right, save/load `.ablocks` projects, and stream USB output directly in Chrome/Edge using the built-in **Web Serial Monitor**.

---

## ✨ Key Capabilities

| Feature | Details |
|---|---|
| 🎛️ **6 Target Board Profiles** | Dynamic pinouts, ADC bit-depth, ISR `IRAM_ATTR`, `EEPROM` dialect, and headers for **Arduino Uno/Nano**, **Mega 2560**, **ESP32 DevKit V1**, **ESP8266 NodeMCU**, **Seeed XIAO nRF52840**, and **Raspberry Pi Pico (RP2040)**. |
| 📚 **Library Manager & `.h` Importer** | One-click curated libraries (`Wire`, `SPI`, `LiquidCrystal_I2C`, `MPU6050`, `VL53L0X`, `MFRC522`, `RF24`, `PubSubClient`, `MAX30105`) plus a built-in **C++ `.h` class parser** that turns third-party headers into draggable Action & Value blocks. |
| 🧩 **MIT App Inventor-Style Named Components** | Define named LEDs, Relays, Buzzers, and Push Buttons mapped to active board pins with automatic `pinMode(...)` setup injection. |
| ⚡ **Hardware Interrupts, Custom Functions & Non-Blocking Timers** | Dedicated blocks for `attachInterrupt()`, `volatile` variables, `noInterrupts()`/`interrupts()`, custom C++ functions, structs, arrays, and `millis()` timers. |
| 💾 **Autosave & Shareable `.ablocks` Projects** | Automatic `localStorage` persistence across reloads, plus `.ablocks` Save/Open export, one-click `.ino` / `platformio.ini` download, and Undo/Redo. |
| 🖥️ **USB Web Serial Monitor** | Built-in live Serial console (`9600` / `57600` / `115200` baud) in Chromium browsers via `navigator.serial`. |

---

## 🚀 Run Locally

Open [`index.html`](index.html) directly in any modern browser, or serve locally:

```powershell
python -m http.server 8080
```

Then visit `http://localhost:8080`.

---

## 👤 Author & License

Maintained by **Dhayananth J ([`@0-Name-Alex`](https://github.com/0-Name-Alex))** • [dhayananth.me](https://dhayananth.me)

Licensed under the [MIT License](LICENSE).
