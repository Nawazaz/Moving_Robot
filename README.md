# 🤖 Moving_Robot – AVR/Arduino-Based Mobile Robot Control System

A collection of low-level AVR (ATmega) programs to control a mobile robot using direct register-level programming (no Arduino abstraction).  
This project demonstrates motor control, Bluetooth communication, line following, speed control, LED matrix display, ultrasonic obstacle avoidance, and servo control.

---

## 🚀 Project Overview

The **Moving_Robot** project implements multiple robot behaviors using C with AVR libraries, focusing on:

- Direct port manipulation (`PORTx`, `DDRx`)  
- PWM-based motor speed control  
- Interrupt-driven Bluetooth communication  
- Sensor-based autonomous navigation  
- LED matrix visualization  
- Ultrasonic distance measurement  
- Servo motor control  

Each folder/module is standalone and demonstrates a specific robot functionality.

---

## 🧩 Features & Modules

### 🔹 Basic Motor Control
- Forward, backward, left, and right movement  
- Direct motor control using `PORTD`  
- Extra LED control using `PORTB`  

**Key Concepts:** GPIO direction control, bitwise operations

---

### 🔹 Bluetooth Control
- UART-based Bluetooth communication (9600 baud)  
- Interrupt-driven command reception  
- LED control via Bluetooth commands (`F`, `B`)  

**Key Concepts:** UART, interrupts (`USART_RX_vect`), serial communication

---

### 🔹 Bluetooth Line Following
- Bluetooth-triggered line-following mode  
- IR sensor-based navigation  
- PWM motor speed adjustment  
- Emergency stop via Bluetooth command  

**Key Concepts:** PWM, UART, sensor fusion, real-time control

---

### 🔹 Line Following
- Autonomous line-following robot  
- Uses left, center, and right IR sensors  
- Implements straight, left-turn, right-turn, and stop logic  

**Key Concepts:** Digital sensors, decision logic, autonomous navigation

---

### 🔹 Line Following with Speed Control
- Line-following combined with PWM-based motor speed control  
- Sharp and smooth turns handled by varying duty cycle  

**Key Concepts:** Timers, PWM (`OCR0A`, `OCR0B`)

---

### 🔹 Speed Control (PWM)
- Demonstrates motor speed ramp-up and ramp-down  
- Uses Timer0 in Fast PWM mode  

**Key Concepts:** Motor control, PWM duty cycle modulation

---

### 🔹 LED Matrix Panel
- I2C-based LED matrix control  
- Displays patterns (smile, arrows, stop signs)  
- Custom I2C implementation via GPIO (bit-banging)  

**Key Concepts:** I2C protocol, LED matrix driving, visualization

---

### 🔹 Line Following with LED Matrix
- Combines line following + LED matrix feedback  
- Displays direction arrows (left/right/forward)  
- Shows STOP message when line is lost  

**Key Concepts:** Multisensor integration, human-robot interaction

---

### 🔹 Ultrasonic Distance Measurement
- HC-SR04 ultrasonic sensor integration  
- Measures distance in centimeters  
- LED alert when obstacle is within threshold  

**Key Concepts:** Pulse measurement, timing, distance calculation

---

### 🔹 Object Avoidance
- Ultrasonic-based obstacle detection  
- Servo motor scans left and right  
- Robot decides direction based on free space  

**Key Concepts:** Obstacle avoidance, servo control, decision making

---

### 🔹 Servo Motor Control
- Servo angle control from 0° to 180°  
- Pulse-width generation using GPIO timing  

**Key Concepts:** Servo PWM, timing control

---

## 🛠️ Hardware Requirements
- **Microcontroller:** ATmega328P / ATmega series  
- **Motor Driver:** L298N / L293D  
- **Motors:** DC geared motors  
- **Sensors:** IR line sensors, HC-SR04 ultrasonic sensor  
- **Bluetooth Module:** HC-05 / HC-06  
- **LED Matrix Display**  
- **Servo Motor**  
- **Power Supply:** Battery pack (7–12V recommended)

---

## 🧰 Software & Tools
- AVR-GCC  
- Microchip Studio / Atmel Studio  
- AVR libc  
- USBasp / Arduino as ISP  
- Serial Bluetooth Controller (Android)

---

## 📂 Repository Structure

Moving_Robot/
│
├── Basic control/
├── Bluetooth/
├── Bluetooth line following/
├── Line Following/
├── Line following with speed control/
├── Line following with LED matrix/
├── Speed control/
├── LED panel/
├── Ultrasonic/
├── Object avoidance/
├── Servo motor/


Each folder contains an independent AVR program.

---

## ▶️ How to Run
1. Open the project in Microchip Studio / Atmel Studio  
2. Select the correct AVR microcontroller  
3. Connect the programmer (USBasp / ISP)  
4. Compile and flash the code  
5. Power the robot and test the selected module  

---

## 📌 Learning Outcomes
- Low-level embedded programming  
- Register-level motor and sensor control  
- Real-time systems using interrupts  
- Autonomous robotics logic  
- Hardware-software integration  

---

⭐ If you find this repository helpful, give it a star!
