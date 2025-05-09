# IoT25-HW03: ESP32 Potentiometer Analog Read

This project uses an ESP32 board to read analog input from a potentiometer and print the values to the Serial Monitor.

---

## 🧾 Objectives

- Read analog input via ADC pin
- Use `analogRead()` on ESP32
- Display the potentiometer values on Serial Monitor

---

## 🧰 Components

- ESP32 DevKit v1  
- Potentiometer module  
- Jumper wires  
- Micro USB cable  

---

## 🔌 Circuit Connection

- **Potentiometer Module → ESP32**
  - V (VCC) → 3.3V  
  - G (GND) → GND  
  - S (Signal) → GPIO 34 (ADC1_CH6)

> 📸 Refer to the wiring photos below for details.

---

## 🧾 Code

```cpp
const int potPin = 34;
int potValue = 0;

void setup() {
  Serial.begin(115200);
  delay(1000);
}

void loop() {
  potValue = analogRead(potPin);
  Serial.println(potValue);
  delay(500);
}
```

---

## 📸 Screenshots

![스크린샷 1](https://github.com/DannyLimDH/IoT25-HW03/blob/main/media/hw3-1.png)
![스크린샷 2](https://github.com/DannyLimDH/IoT25-HW03/blob/main/media/hw3-2.png)

---

## ▶ Demo GIF

![Demo](./media/IoT25-HW03.gif)

---
## References
Rui Santos, VSCode + PlatformIO IDE: ESP32 & ESP8266, Arduino (Random Nerd Tutorials)
(https://randomnerdtutorials.com/esp32-adc-analog-read-arduino-ide/)

---
