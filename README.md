## Academic Project
## Introduction
      Air and sound pollution is growing issue these days. It is necessary to monitor air quality for a better future and healthy living for all. We propose an air quality as well as 
sound pollution monitoring system that allows us to monitor and check air quality as well as sound pollution in particular area through IoT.

# 🌫️ NodeMCU Based Air and Noise Monitoring Dashboard Over IoT

This project is an **IoT-based environmental monitoring system** that uses a NodeMCU microcontroller to track **air quality** and **noise levels** in real-time.
The data is pushed to an online dashboard (such as **Adafruit IO**) for remote monitoring and analysis.

---

## 📌 Objective
To develop a low-cost, wireless system capable of monitoring air pollution (gas levels like CO, CO₂, etc.) and noise pollution, sending the data to the cloud for visualization, and triggering alerts if predefined thresholds are exceeded.

---

## ⚙️ Technologies & Components Used

### 🛠️ Hardware
- **NodeMCU (ESP8266 Wi-Fi module)**
- **MQ135 Gas Sensor** (for air quality detection)
- **Microphone Sound Sensor** (for noise level detection)
- **Breadboard and Jumper wires**
- **USB cable**
- **Power Supply**

### 💻 Software
- **Arduino IDE**
- **Adafruit IO (IoT Cloud Platform)**
- **IFTTT (for alerts or automation)**
- **Adafruit MQTT Library**
- **ESP8266WiFi Library**

---

## 🛠️ Components Used

| Component           | Quantity |
|---------------------|----------|
| NodeMCU ESP8266     | 1        |
| MQ135 Gas Sensor    | 1        |
| Sound Sensor Module | 1        |
| Jumper Wires        | ~10      |
| Breadboard          | 1        |
| USB Cable (Micro-B) | 1        |

---
## ⚙️ How It Works

1. MQ135 detects air quality and sends analog signals to NodeMCU.
2. Sound sensor outputs high/low digital values based on noise.
3. NodeMCU publishes data to Adafruit IO using MQTT.
4. Dashboard displays charts/gauges.
5. Alerts are triggered via IFTTT if values cross thresholds.

---

## 🔌 Circuit Diagram

> 📷 daigram.png

## 📊 Cloud Dashboard
The project uses **Adafruit IO** to create a visually rich dashboard:
- Gauge for air quality index (AQI)
- Line chart for noise level trends
- Trigger notifications using IFTTT webhooks

---

## 🔁 Data Flow
Sensors (MQ135 + Sound)
        ↓ 
NodeMCU (Processes & Connects via Wi-Fi)
        ↓ 
Adafruit IO (Dashboard + Storage)
        ↓
IFTTT (Sends alerts)

## 🚀 How to Set Up

1. **Install Arduino IDE and libraries**:
   - ESP8266 Board URL: `http://arduino.esp8266.com/stable/package_esp8266com_index.json`
   - Libraries: `Adafruit MQTT`, `ESP8266WiFi`

2. **Connect sensors** to NodeMCU GPIO pins:
   - MQ135 to analog pin A0
   - Sound sensor to digital pin (e.g., D2)

3. **Upload code** to NodeMCU via Arduino IDE.

4. **Set up Adafruit IO**:
   - Create feeds: `air-quality`, `noise-level`
   - Generate your `AIO Key` and `Username`

5. **Configure IFTTT (optional)**:
   - Create applets to send alerts when feed values exceed limits

## 🧠 Features
- Real-time air and noise monitoring
- Data pushed to Adafruit IO via MQTT protocol
- Custom dashboards with charts and gauges
- Email/SMS alerts using IFTTT if air or noise exceeds threshold
- Lightweight and wireless setup using Wi-Fi

---

