# 🚗✨ Smart Automatic Gate Control System Using Automatic Gate Demo Kit ✨🔧

An **embedded system project** that detects vehicles and opens the gate automatically using an ultrasonic sensor, servo motor, LEDs, and a buzzer — all controlled by an **Arduino** 🧠💡.

---

## 🌟 Overview

Welcome to the **Smart Automatic Gate Control System**! 🏡📡  
This Arduino-powered gate uses an **ultrasonic sensor** to detect nearby cars or objects and opens the gate automatically.  
The gate then **closes after a few seconds** with LED signals and buzzer alerts to provide clear feedback to users. 🎯

---

## 📦 Kit Structure: Components and Circuit

### 🛠️ Hardware Components

| Component        | Description |
|------------------|-------------|
| 🧠 Arduino Uno (or Nano) | Microcontroller board for all logic control |
| 📏 Ultrasonic Sensor | Detects distance to identify car presence |
| ⚙️ Servo Motor (SG90) | Controls gate arm rotation (0° = closed, 90° = open) |
| 🔴 Red LED | Lights up when the gate is **CLOSED** |
| 🔵 Blue LED | Lights up when the gate is **OPEN** |
| 📢 Piezo Buzzer | Beeps to signal gate status |
| 🎧 150Ω Resistors | For LED current limitation |
| 🔗 Breadboard + Jumpers | For circuit connections |
| 🔌 5V USB Power | Supplies power from PC or power bank |
| 🚗 Toy Car/Object | Used to simulate vehicle presence |

---

## 🔌 Circuit Diagram Summary

### Arduino Pin Connections

| Component                  | Pin         |
|----------------------------|-------------|
| Ultrasonic Sensor Trigger  | D3          |
| Ultrasonic Sensor Echo     | D4          |
| Red LED (Gate Closed)      | D5          |
| Blue LED (Gate Open)       | D6          |
| Servo Motor (PWM Signal)   | D7          |
| Buzzer                     | D8          |
| Common Ground              | GND         |
| Power Supply               | 5V          |

---

## 🔄 Data Flow Diagram

```plaintext
[Ultrasonic Sensor] → (Distance Data) → [Microcontroller: Arduino]
→ (Logic Evaluation) → 
    If (Car detected nearby):
        - Turn ON Blue LED
        - Turn OFF Red LED
        - Turn ON Buzzer
        - Rotate Servo Motor (Open Gate)
        - Wait for 5 Seconds
        - Rotate Servo Motor (Close Gate)
        - Turn ON Red LED
        - Turn OFF Blue LED
        - Turn OFF Buzzer
