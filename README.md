# 🌿 ESP32 Garden Management System - Elite Edition

[![ESP32](https://img.shields.io/badge/ESP32-ESP32--WROOM--32-blue)](https://www.espressif.com)
[![Blynk](https://img.shields.io/badge/Blynk-IoT%20Platform-green)](https://blynk.io)
[![Telegram](https://img.shields.io/badge/Telegram-Bot%20API-blue)](https://core.telegram.org/bots/api)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Arduino%20IDE-orange)](https://www.arduino.cc)
[![GitHub stars](https://img.shields.io/github/stars/YOUR_USERNAME/ESP32-Garden-Management?style=social)](https://github.com/YOUR_USERNAME/ESP32-Garden-Management)

> A complete smart garden automation system with auto-watering, intelligent grow lights, weather monitoring, Telegram alerts, Blynk IoT, and a beautiful real-time web dashboard with AI assistant.

---

## 📸 Screenshots

### Web Dashboard - Desktop View
The main dashboard showing real-time sensor data, weather widget, and system controls.

![Dashboard Main](screenshots/<img width="610" height="540" alt="WhatsApp Image 2026-05-19 at 12 37 50 AM" src="https://github.com/user-attachments/assets/28dfdedf-1d26-4d00-82d0-dba007b11d75" />
)

### Telegram Bot - Status Report
Instant garden status reports via Telegram commands.

<img src="screenshots/<img width="720" height="1600" alt="WhatsApp Image 2026-05-25 at 12 13 50 AM" src="https://github.com/user-attachments/assets/22eea1e3-5a2e-4c5a-a5f3-380f069c0e2c" />
" width="400" alt="Telegram Status">
---

## 📌 Features

### 🌱 Core Automation
| Feature | Description |
|---------|-------------|
| 💧 **Smart Irrigation** | Automatic pump control based on soil moisture with configurable dry/wet thresholds |
| 💡 **Grow Lights** | LDR sensor-based auto lighting when ambient light drops below threshold |
| 🛢️ **Tank Monitor** | Ultrasonic water level sensor with visual gauge and low-level alerts |
| 🤖 **Dual Mode** | Fully automatic or manual control via dashboard/Telegram/Blynk |

### 🌤️ Weather Integration
| Parameter | Source |
|-----------|--------|
| Temperature & Feels Like | Open-Meteo API |
| Humidity | Open-Meteo API |
| Wind Speed | Open-Meteo API |
| UV Index | Open-Meteo API |
| Visibility | Open-Meteo API |
| Atmospheric Pressure | Open-Meteo API |
| Dew Point | Calculated |
| Moon Phase | Calculated |
| Rain Probability | Open-Meteo API |
| Sunrise / Sunset | Open-Meteo API |

### 📱 Control Interfaces
| Interface | Capabilities |
|-----------|-------------|
| 🌐 **Web Dashboard** | Real-time monitoring, manual control, threshold settings, charts |
| 📱 **Blynk IoT App** | Remote monitoring, pump/light status, auto mode toggle |
| 💬 **Telegram Bot** | Status reports, weather updates, commands, critical alerts |
| 🤖 **AI Assistant** | Garden advice based on live sensor data |

### 🔔 Smart Alerts (One-Time Only)
- 🛢️ Water tank FULL / EMPTY
- 🌧️ Rain expected (watering paused)
- ❄️ Freeze warning (temperature < 5°C)
- ⚠️ Low water level pump protection

---

## 🛠️ Hardware Requirements

| Component | Quantity | Purpose | Approximate Cost |
|-----------|----------|---------|------------------|
| ESP32 Development Board | 1 | Main controller | $5 - $10 |
| HC-SR04 Ultrasonic Sensor | 1 | Water tank level | $2 - $4 |
| Soil Moisture Sensor | 1 | Soil moisture detection | $2 - $3 |
| LDR Sensor Module | 1 | Ambient light detection | $1 - $2 |
| 5V Relay Module (2-Channel) | 1 | Pump & light control | $2 - $3 |
| 12V DC Water Pump | 1 | Plant watering | $5 - $8 |
| Red LED Strip / LED | 1 | Grow light (red spectrum) | $3 - $5 |
| Blue LED Strip / LED | 1 | Grow light (blue spectrum) | $3 - $5 |
| 12V Power Supply | 1 | Pump power | $5 - $8 |
| Water Tank/Container | 1 | Water reservoir | Varies |
| Jumper Wires | 20+ | Connections | $2 - $3 |
| Breadboard | 1 | Prototyping | $3 |

### Optional Components
| Component | Purpose |
|-----------|---------|
| MOSFET Module | Alternative to relay for LED dimming |
| DHT22 Sensor | Additional temperature/humidity |
| Solar Panel | Off-grid power |

### Total Estimated Cost: **$35 - $55**

---

## 🔌 Pin Connections

### Sensor Connections
| Sensor | Pin | ESP32 GPIO |
|--------|-----|------------|
| **HC-SR04 TRIG** | Trigger | GPIO 5 |
| **HC-SR04 ECHO** | Echo | GPIO 18 |
| **Soil Moisture** | Analog Out | GPIO 34 |
| **LDR Sensor** | Analog Out | GPIO 35 |

### Actuator Connections
| Actuator | Pin | ESP32 GPIO |
|----------|-----|------------|
| **Pump Relay A** | IN1 | GPIO 4 |
| **Pump Relay B** | IN2 | GPIO 16 |
| **Red LED** | Anode (+) | GPIO 13 |
| **Blue LED** | Anode (+) | GPIO 27 |

### Power Connections
| Component | Voltage | Connection |
|-----------|---------|------------|
| ESP32 | 5V | USB or VIN pin |
| Pump | 12V | External supply via relay |
| LEDs | 12V/5V | External supply via relay/resistor |
| Sensors | 3.3V/5V | ESP32 VCC pin |

---

## 📁 Project Structure
