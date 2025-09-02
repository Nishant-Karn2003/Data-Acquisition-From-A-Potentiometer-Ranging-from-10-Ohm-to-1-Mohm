# Data Acquisition from a Potentiometer (10 Ω – 1 MΩ)

**An Arduino-based system to measure the resistance of a potentiometer and display results in real-time using LEDs, LCD, and Serial Monitor.**

---

## 🎯 Objective
The objective of this project is to measure the resistance of a potentiometer using an **Arduino UNO**.  
By reading analog input from a voltage divider circuit, the Arduino calculates the potentiometer’s resistance (in Ω, kΩ, or MΩ).  
The resistance range is indicated with LEDs and displayed on the Serial Monitor/LCD in real time.

---

## ⚡ Features
- Measures potentiometer resistance ranging from **10 Ω to 1 MΩ**  
- Uses **voltage divider circuit + ADC** principle for measurement  
- Resistance displayed in **ohms, kilo-ohms, or mega-ohms**  
- **LED indicators** show resistance range (Ω, kΩ, MΩ)  
- Real-time monitoring through **Serial Monitor and LCD**

---

## 🛠 Components Required
- Arduino Uno × 1  
- Potentiometer (10 Ω – 1 MΩ) × 1  
- Fixed Resistor (10 kΩ) × 1  
- LEDs × 3 (for resistance range indication)  
- Breadboard × 1  
- Jumper wires (as required)  
- USB cable & 5V regulated power supply  

---

## 🔎 Working Principle
1. **Voltage Divider**  
   - Potentiometer and fixed resistor form a voltage divider.  
   - As the potentiometer’s resistance changes, the output voltage varies proportionally.  

2. **Analog-to-Digital Conversion (ADC)**  
   - Arduino reads the midpoint voltage using `analogRead(A0)` (10-bit ADC, 0–1023).  

3. **Resistance Calculation**  
   - Using the formula:  
     \[
     R_{pot} = \frac{V_{out} \cdot R_{fixed}}{V_{in} - V_{out}}
     \]  
   - Where:  
     - \(R_{fixed} = 10k\Omega\)  
     - \(V_{in} = 5V\)  
     - \(V_{out} =\) voltage at the divider midpoint  

4. **Display**  
   - Resistance value shown in appropriate units (Ω, kΩ, MΩ).  
   - LEDs light up based on the resistance range.  
   - Serial Monitor displays the calculated resistance.  

---

## 📐 Circuit Setup
- Potentiometer wiper connected to **A0** (Arduino analog input)  
- Fixed resistor (10 kΩ) in series with potentiometer  
- LEDs connected to pins **4, 10, 11** to show Ω / kΩ / MΩ ranges  
- USB cable to Arduino for power and programming  

---

## 💻 Software Logic (Arduino)
- Initialize Serial Monitor at 9600 baud and set LED pins as outputs  
- Read potentiometer voltage with `analogRead()`  
- Convert ADC value → Voltage → Resistance using the divider equation  
- Print resistance in correct units  
- Turn on LED based on resistance range  
- Add a small delay (`delay(500)`) for stable output  

---

## 🚀 Applications
- Demonstrates **indirect measurement** using voltage divider principle  
- Practical example of **Ohm’s Law** and circuit analysis  
- Learning tool for **ADC, microcontroller interfacing, and display systems**  
- Ideal beginner project for **electronics and embedded systems**  

---

## 👥 Contributors
- Manjesh Kumar (23UEI144)  
- Nishant Kumar Karn (23UEI133)  
- Nikhil Singh Dhruwe (23UEI142)  
- Aryan Giri (23UEI131)  
- Anjali Patel (23UEI148)  
- Pranjal Pal (23UEI215)  

**Affiliation:** National Institute of Technology, Agartala – Department of Electronics & Instrumentation Engineering  

---

## 📚 References
- M. Morris Mano – *Digital Design with an Introduction to Verilog HDL, VHDL, and SystemVerilog*  
- Thomas L. Floyd – *Digital Fundamentals*  

---
