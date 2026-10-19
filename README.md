# 🚗 Arduino Ultrasonic Automotive Reverse Parking Assistant

[![Platform: Arduino](https://img.shields.io/badge/Platform-Arduino-00979D.svg?logo=arduino&logoColor=white)](https://www.arduino.cc/)
[![Application: Automotive](https://img.shields.io/badge/Application-Reverse%20Parking%20Sonar-blue.svg)]()
[![Sensors: HC--SR04](https://img.shields.io/badge/Sensors-HC--SR04%20Ultrasonic-orange.svg)]()
[![Language: C++](https://img.shields.io/badge/Language-C%2B%2B-00599C.svg?logo=c%2B%2B&logoColor=white)](https://en.wikipedia.org/wiki/C%2B%2B)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status: Tested](https://img.shields.io/badge/Hardware%20Status-Tested%20%26%20Verified-brightgreen.svg)]()

An automotive ultrasonic reverse parking assist device that provides real-time tri-color visual LED indicators and acoustic proximity alerts. Designed to assist drivers in judging distance to walls, pillars, and rear obstacles in garages and parking bays.

---

## 🛠️ Hardware Requirements & Bill of Materials (BOM)

| Component | Specification | Quantity |
| :--- | :--- | :--- |
| **Microcontroller** | Arduino Uno, Nano, or compatible board | 1 |
| **Ultrasonic Sensor** | HC-SR04 Transducer Module | 1 |
| **Green LED** | 5mm LED (Safe Zone: Distance > 30cm) | 1 |
| **Yellow LED** | 5mm LED (Caution Zone: 15cm - 30cm) | 1 |
| **Red LED** | 5mm LED (Stop Zone: Distance < 15cm) | 1 |
| **Piezo Buzzer** | 5V Active Piezo Buzzer (Hazard Alarm) | 1 |
| **Resistors** | 220Ω, 1/4W, 5% carbon film | 3 |
| **Breadboard & Jumpers** | Half-size breadboard with Dupont jumpers | 1 set |

---

## 🔌 Circuit Pinout & Wiring

| Arduino Pin | Connected Component | Zone Assignment |
| :--- | :--- | :--- |
| **Pin D9** | HC-SR04 Trig | 10µs ultrasonic pulse trigger |
| **Pin D10** | HC-SR04 Echo | Time-of-flight return signal |
| **Pin D2** | Green LED Anode (via 220Ω) | **SAFE**: Distance > 30 cm |
| **Pin D3** | Yellow LED Anode (via 220Ω) | **CAUTION**: 15 cm &le; Distance &le; 30 cm |
| **Pin D4** | Red LED Anode (via 220Ω) | **CRITICAL STOP**: Distance < 15 cm |
| **Pin D5** | Piezo Buzzer (+) | Continuous Stop Alarm (< 15 cm) |
| **GND** | LED Cathodes, Buzzer (-), Sensor GND | Common ground rail |

---

## 🚀 Installation & Upload

1. Clone repository:
   ```bash
   git clone https://github.com/youniquestar/arduino-smart-parking-assistant.git
   ```
2. Open [`smart_parking_assistant/smart_parking_assistant.ino`](smart_parking_assistant/smart_parking_assistant.ino) in Arduino IDE.
3. Upload and view live metric distances on Serial Monitor (9600 baud).

---

## 📜 License

Licensed under the [MIT License](LICENSE).
