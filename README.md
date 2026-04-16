
# RFID Attendance System

**Created by Yogesh M**

---

## 🚀 Overview

This project is an **RFID-based Attendance System** designed to automate attendance tracking using RFID cards/tags and a microcontroller (Arduino/ESP-based system).

The system scans RFID cards, identifies users, and records their presence with real-time feedback using display and indicators.

RFID technology is widely used for automation because it enables **fast, contactless identification and tracking** across many applications. ([arXiv][1])

---

## 🧠 Features

* 📡 RFID card scanning
* 🧑 User identification via UID
* ⏱️ Entry and exit tracking
* 📟 LCD display for status messages
* 🔔 Buzzer & LED feedback
* 💾 Data storage (EEPROM / Serial / external system)
* ❌ Invalid card detection

---

## ⚙️ Hardware Requirements

* Arduino / ESP32 / NodeMCU
* RC522 RFID Module
* RFID Cards / Tags
* LCD Display (16x2 or I2C)
* Buzzer
* LEDs (Red/Green)
* Jumper wires & breadboard

---

## 📁 Project Structure

```bash
rfidattendance/
│
├── code/
│   └── main.ino
├── README.md
└── assets/ (optional)
```

---

## 🔌 Wiring Overview

### RC522 → Arduino (SPI)

| RC522 | Arduino |
| ----- | ------- |
| SDA   | D10     |
| SCK   | D13     |
| MOSI  | D11     |
| MISO  | D12     |
| RST   | D9      |
| GND   | GND     |
| 3.3V  | 3.3V    |

---

## 🔄 How It Works

1. System initializes RFID module and display
2. User taps RFID card
3. UID is read from card
4. System checks UID:

   * ✅ Valid → Mark attendance
   * ❌ Invalid → Show error
5. Displays message on LCD
6. Buzzer/LED gives feedback
7. Logs attendance data

---

## 🖥️ Setup & Installation

1. Clone the repository:

```bash
git clone https://github.com/embedwTej/rfidattendance.git
cd rfidattendance
```

2. Open project in **Arduino IDE**

3. Install required libraries:

* MFRC522
* SPI
* LiquidCrystal / LiquidCrystal_I2C

4. Upload code to your board

---

## ▶️ Usage

* Power ON the system
* Tap RFID card on reader
* View status on display
* Monitor logs via Serial Monitor

---

## 📡 Output Example

```bash
Card Detected
Welcome Yogesh
Time: 10:32 AM
```

or

```bash
Invalid Card
Access Denied
```

---

## 🔧 Customization

* Add more RFID UIDs
* Connect to:

  * WiFi (ESP8266/ESP32)
  * Google Sheets
  * Database / Web dashboard
* Add RTC module for accurate time
* Integrate IoT dashboard (ThingsBoard, Firebase)

---

## 💡 Use Cases

* College attendance system
* Office entry tracking
* Smart access control
* IoT-based monitoring systems

---

## 📌 Future Improvements

* Cloud integration (Google Sheets / Firebase)
* Mobile app dashboard
* Face recognition + RFID combo
* Email/SMS alerts
* Real-time analytics

---

## ⚠️ Notes

* RC522 works on **3.3V only**
* Ensure proper wiring (SPI pins)
* Avoid multiple rapid scans (debounce logic recommended)

---

## 🤝 Contribution

Feel free to fork, improve, and submit pull requests.

---

## 📄 License

Open-source project (add license if needed)


