# Relay Controller Board (ESP32)

A relay control board based on an **ESP32-WROOM** module. It runs from **12V**, drives **4x 12V relay outputs**, and can be programmed directly over **USB** using the onboard USB-to-UART converter.

## What’s on the board

- **ESP32-WROOM** microcontroller  
- **4x relay outputs (12V relays)**
- Power regulation:
  - **12V → 5V buck**
  - **5V → 3.3V LDO**
- **3.3V → 5V level shifters** for relay control logic
- **Onboard USB-to-UART** converter for easy programming over USB
- **SPI header** for adding an optional screen / SPI device

## Power

- Supply the board with **12V DC**
- The board generates:
  - **5V** (buck)
  - **3.3V** (LDO)

## Programming

- Plug in **USB**
- Flash the ESP32 using Arduino IDE / PlatformIO / ESP-IDF 

## SPI Expansion

There is an **SPI pinout/header** to connect a display (or other SPI peripherals).
