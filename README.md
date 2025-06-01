##LoRa Chat (Arduino) 📡💬
This project is a simple LoRa-based serial chat system for Arduino using the RH_RF95 driver from the RadioHead library. It enables two or more devices to exchange messages over long distances via LoRa radios (operating at 950 MHz).

Features
1.Two-way serial communication using LoRa
2.Send messages manually through the Serial Monitor
3.Automatically receive and display incoming LoRa messages
4.Configurable frequency and transmission power

🛠 Required Hardware
-Arduino Uno or a compatible board
-LoRa module with RH_RF95 chip (e.g., HopeRF RFM95)
-Jumper wires
-Breadboard or a soldered PCB setup

## 🔌 Pin Configuration

| LoRa Pin | Arduino Pin |
|----------|--------------|
| `NSS`    | `D8` (CS)     |
| `RESET`  | `D4` (RST)    |
| `DIO0`   | `D7` (INT)    |
| `MOSI`   | `D11`         |
| `MISO`   | `D12`         |
| `SCK`    | `D13`         |
| `GND`    | `GND`         |
| `VCC`    | `3.3V` ⚠️ (LoRa module must be 3.3V compatible!) |

---

## 🧪 Software Requirements

- Arduino IDE
- [RadioHead library](http://www.airspayce.com/mikem/arduino/RadioHead/)

Install the RadioHead library by:
1. Going to **Sketch > Include Library > Manage Libraries...**
2. Searching for **RadioHead**
3. Clicking **Install**

---

## ⚙️ Configuration

```cpp
#define RFM95_CS 8
#define RFM95_RST 4
#define RFM95_INT 7
#define RF95_FREQ 950.0 // Change this according to your region and module
