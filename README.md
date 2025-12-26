# 🚗 Vehicle Accident Detection and Alert System

An **IoT-based embedded safety system** that automatically detects vehicle accidents using motion sensors and instantly alerts emergency contacts with precise GPS location via GSM communication.

---

## 📌 Problem Statement

Road accidents often result in **delayed medical assistance**, especially in remote or low-visibility areas where victims cannot call for help. Traditional accident reporting relies on human intervention, which may not always be possible during severe crashes.

This project addresses this challenge by **automatically detecting accidents** and **triggering emergency alerts without human involvement**, ensuring that help reaches victims within the critical *golden hour*.

---

## 🎯 Objectives

- Automatically detect vehicle accidents using real-time sensor data  
- Identify impact, rollover, tilt, and abnormal vehicle orientation  
- Fetch accurate GPS coordinates immediately after detection  
- Send SMS alerts with Google Maps location link  
- Initiate an automatic emergency call as a fail-safe mechanism  

---

## 🧠 System Overview

The system continuously monitors vehicle motion using an **MPU6050 accelerometer and gyroscope** connected to an **ESP32 microcontroller**.

When an abnormal event is detected:
1. Accident conditions are validated using threshold-based logic  
2. GPS coordinates are acquired from the Neo-6M GPS module  
3. Emergency SMS with location is sent via GSM  
4. An automated phone call is initiated  

---

## 🧩 Hardware Components

| Component | Description |
|---------|------------|
| **ESP32** | Main microcontroller and control unit |
| **MPU6050** | Detects acceleration and angular velocity |
| **Neo-6M GPS** | Provides real-time latitude and longitude |
| **SIM800A GSM** | Sends SMS alerts and initiates calls |
| Breadboard & Wires | Circuit connections |

---

## 🔧 Software & Tools

- Arduino IDE  
- Embedded C / C++  
- TinyGPS++ Library  
- Wire (I2C) Library  
- AT Commands for GSM  

---

## ⚙️ Working Principle

### 1️⃣ Continuous Monitoring
The MPU6050 continuously measures acceleration and rotation along all three axes.

### 2️⃣ Accident Detection Logic
An accident is detected based on:
- Sudden acceleration spikes  
- Abnormal tilt or rollover angles  
- High angular rotation  

False triggers caused by road bumps are minimized using debounce logic.

### 3️⃣ GPS Location Acquisition
GPS coordinates are parsed and converted into a Google Maps link.

### 4️⃣ Emergency Alert Mechanism
- SMS alert with location link  
- Automated emergency phone call  

---

## 📊 Accident Detection Thresholds

| Event | Typical g-Force |
|-----|---------------|
| Minor collision | 5–10 g |
| Moderate collision | 10–30 g |
| Severe crash | > 30 g |

---

## 🌍 Applications

- Vehicle safety systems  
- Fleet monitoring  
- Emergency response solutions  
- Smart transportation systems  

---

## 🚀 Future Enhancements

- Mobile application integration  
- Cloud data logging  
- AI-based crash severity analysis  
- Emergency service auto-dispatch  

---

## 🧑‍💻 Contributors

- **B. Lohitha**
- P. Ramtej  
- P. A. Ravi Tejaswini  
- M. Lisa Jennet  

Department of Electronics & Communication Engineering  
RGUKT – RK Valley

---

## ⭐ Show Your Support

If you found this project useful, **star ⭐ the repository** and feel free to fork or contribute!
