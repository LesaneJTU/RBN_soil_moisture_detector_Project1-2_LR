# RBN_soil_moisture_detector_Project1-2_LR
Building and Coding a Soil Detector P1

This project is a low-cost soil moisture detector built with Arduino. It measures soil moisture, temperature, humidity, and light, then displays the results on an LCD screen and uses LED indicators to signal soil water levels.  
 Repository Structure

```
RBN_soil_moisture_detector_Project1-2_LR/
│── Assembly 1.zip           # CAD / 3D Design files
│── Assembly 1 (1).zip       # Additional design files
│── Bill of Material         # Parts list
│── README.md                # Project documentation
│── Soil Detector.pdf        # Image of materials
│── Soil_Detector.png        # Diagram of design
│── soil_detector.ino        # Arduino code
```
Hardware Components

| Component              | Quantity | Notes                                  |
|------------------------|----------|----------------------------------------|
| Arduino Uno            | 1        | Microcontroller                        |
| Soil Moisture Sensor   | 1        | Analog output to A0                    |
| DHT11 Sensor           | 1        | Temperature & Humidity                 |
| Photoresistor (LDR)    | 1        | For light measurement                  |
| LCD 16x2 (I2C module)  | 1        | For displaying readings                |
| Green LED              | 1        | Soil moisture > 50%                    |
| Orange LED             | 1        | Soil moisture ~30%                     |
| Red LED                | 1        | Soil moisture < 10% (blinking)         |
| Breadboard             | 1        | For prototyping                        |
| Jumper Wires           | 10+      | Male-to-male / Female-to-male          |
| 9V Battery             | 1        | Power supply                           |

---
Software & Libraries

- **Arduino IDE**  
- Required libraries:  
  - `LiquidCrystal_I2C.h`  
  - `DHT.h`  

---
Features

- Displays **Soil Moisture %, Temperature, Humidity, and Light** on LCD.  
- **LED indicators** for soil conditions:  
  - 🟢 Green = Moisture > 50%  
  - 🟠 Orange = Moisture ~30%  
  - 🔴 Red (blinking) = Moisture < 10%  

---
How to Build  

1. Prepare Components  
Gather all items from the Bill of Materials above.  

2. Wiring Connections  

- **Soil Moisture Sensor** → A0 (analog pin)  
- **Photoresistor** → A1 (analog pin)  
- **DHT11 Sensor** → Digital pin 2  
- **LCD 16x2 (I2C)** → SDA (A4), SCL (A5)  
- **LEDs**:  
  - Green → Pin 8  
  - Orange → Pin 9  
  - Red → Pin 10  
- **Power**: 9V battery or USB  

---
ASCII Wiring Diagram  

```
              +----------------------+
              |      Arduino Uno     |
              |                      |
      A0 <----| Soil Moisture Sensor |
      A1 <----| Photoresistor        |
       2 <----| DHT11 Sensor         |
       8 <----| Green LED            |
       9 <----| Orange LED           |
      10 <----| Red LED              |
      SDA <---| LCD SDA (A4)         |
      SCL <---| LCD SCL (A5)         |
              |                      |
     5V ------| VCC (Sensors + LCD)  |
    GND ------| GND (Common Ground)  |
              +----------------------+

        Power Options:
        - USB to PC
        - 9V Battery (Vin + GND)
```
## PICTURE OF THE 
```

<img width="1536" height="632" alt="Soil Detector" src="https://github.com/user-attachments/assets/a44a03af-0a5f-4ba5-b37e-c2a83f15b29b" />
