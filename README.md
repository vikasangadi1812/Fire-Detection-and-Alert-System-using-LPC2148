# 🔥 LPC2148 Fire Detection and Alert System

## 📌 Project Overview

→ The **LPC2148 Fire Detection and Alert System** is an embedded system designed to detect fire using a flame sensor.  
→ The system uses the **LPC2148 ARM7 microcontroller** to continuously monitor the sensor output.  
→ When fire is detected, the system activates a **red LED and buzzer** to provide an immediate alert.  
→ During normal conditions, a **green LED** indicates that the system is safe.  
→ A **16×2 LCD display** shows the current status of the system.  

---

## 🎯 Objectives

→ Detect fire using a flame/fire sensor  
→ Process the sensor signal using the **LPC2148 ARM7 microcontroller**  
→ Provide visual indication using red and green LEDs  
→ Provide an audible warning using a buzzer  
→ Display the fire detection status on a 16×2 LCD  
→ Continuously monitor the surroundings for fire conditions  

---

## 🧰 Components Used

→ LPC2148 ARM7 Microcontroller  
→ LPC2148 Trainer Board  
→ Flame/Fire Sensor Module  
→ 16×2 LCD Display  
→ Red LED  
→ Green LED  
→ Buzzer  
→ Resistors  
→ Connecting Wires  
→ Power Supply  

---

## 🔌 Pin Connections

### Flame Sensor

→ Flame Sensor DO → **LPC2148 P0.16**

### Alert Indicators

→ Red LED → **P0.17**  
→ Buzzer → **P0.18**  
→ Green LED → **P0.19**

### LCD

→ LCD RS → **P0.20**  
→ LCD EN → **P0.21**  
→ LCD D4 → **P0.22**  
→ LCD D5 → **P0.23**  
→ LCD D6 → **P0.24**  
→ LCD D7 → **P0.25**

### LCD Power

→ LCD VSS → GND  
→ LCD VDD → +5V  
→ LCD RW → GND  
→ LCD V0 → Contrast adjustment  

---

## 🔄 System Flow


START
  ↓
Power ON
  ↓
Initialize LPC2148
  ↓
Configure GPIO Pins
  ↓
Initialize 16×2 LCD
  ↓
Initialize Flame Sensor
  ↓
Read Flame Sensor
  ↓
Check Fire Condition
  ↓
Fire Detected?
  ↓
 ┌───────────────────────┐
 │                       │
 YES                     NO
 │                       │
 ↓                       ↓
Red LED ON          Green LED ON
 │                       │
 ↓                       ↓
Buzzer ON            Red LED OFF
 │                       │
 ↓                       ↓
Green LED OFF        Buzzer OFF
 │                       │
 ↓                       ↓
LCD → FIRE           LCD → SAFE
DETECTED             CONDITION
 │                       │
 └───────────┬───────────┘
             ↓
      Continue Monitoring
             ↓
       Read Sensor Again
             ↓
            LOOP
