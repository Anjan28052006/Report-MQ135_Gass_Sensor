#  Report on MQ135 Gas Sensor

## 🔹 Introduction
The **MQ135 gas sensor** is a widely used air quality sensor capable of detecting gases such as **ammonia (NH₃), nitrogen oxides (NOₓ), alcohol, benzene, smoke, and carbon dioxide (CO₂)**. It is commonly used in **air quality monitoring systems, IoT projects, and pollution detection devices** due to its **low cost and sensitivity**.During my study of the MQ135 datasheet, I observed that calibration plays a key role in accuracy and reliable detection of gases.


---

## 🔹 Specifications
- **Sensor Type:** Semiconductor gas sensor  
- **Detectable Gases:** NH₃, NOₓ, alcohol, benzene, smoke, CO₂  
- **Operating Voltage:** 5V DC  
- **Load Resistance (RL):** Adjustable (10kΩ typical)  
- **Heater Resistance (RH):** 31Ω ± 3Ω  
- **Heating Voltage (VH):** 5V ± 0.2V  
- **Power Consumption:** < 800 mW  
- **Concentration Range:** 10 ppm – 1000 ppm  
- **Preheat Time:** 24–48 hours for accurate results  

---

## 🔹 Working Principle
The MQ135 sensor works on the principle of **changes in resistance** of its sensitive layer (**SnO₂ – tin dioxide**) when exposed to target gases.

- In **clean air**, SnO₂ has **higher resistance**.  
- When **pollutant gases** are present, the resistance **drops** due to adsorption of gas molecules on the sensor’s surface.  
- This change is measured as **voltage variation** across the load resistance (RL), which can be calibrated to indicate **gas concentration in ppm**.

---

## 🔹 Calibration
Calibration is essential because different gases produce different responses.

1. Place the sensor in a **known concentration** of target gas.  
2. Record the sensor resistance (**Rs**).  
3. Calculate the ratio **Rs/R₀**, where **R₀** is the sensor resistance in clean air.  

### Example Detectable Levels:
- **Ammonia (NH₃):** Detectable from ~10 ppm  
- **Carbon dioxide (CO₂):** Detectable from ~350 ppm  
- **Benzene:** Detectable from ~10 ppm  
- **Alcohol & Smoke:** Detectable from ~10 ppm  

Each gas has a **characteristic Rs/R₀ vs ppm curve** from the datasheet.

---

## 🔹 Freundlich Absorption Isotherm (Graph)
The sensor’s gas adsorption behavior follows the **Freundlich Absorption Theorem**, expressed as:

$$
\frac{Rs}{R_0} = A \cdot (C)^{-m}
$$


Where:  
- **Rs** = Sensor resistance in gas  
- **R₀** = Resistance in clean air  
- **C** = Gas concentration (ppm)  
- **A, m** = Constants depending on gas type  

The datasheet provides **log-log plots of Rs/R₀ vs ppm** for various gases, showing that sensor sensitivity decreases nonlinearly with increasing gas concentration.

---

## 🔹 Images & Graphs

### MQ135 Sensor Module
![MQ135 Sensor](https://img.joomcdn.net/d93f956af2fc3553b52df8fb7f76563a6ac5f09a_original.jpeg)

### Example Rs/R₀ vs ppm Graph (from Datasheet)
![MQ135 Graph](https://res.utmel.com/Images/UEditor/f60c9b57-5bc2-455e-929a-74a24c95ced4.jpg)

---

## 🔹 Applications
- Air pollution monitoring  
- Indoor air quality control  
- Industrial gas leakage detection  
- Smart IoT air quality devices  
- Smoke and alcohol detection systems  

---

## 🔹 Advantages
- Low cost  
- High sensitivity to multiple gases  
- Easy interface with microcontrollers (Arduino, ESP32, Raspberry Pi)  

---

## 🔹 Limitations
- Requires **long preheating time**  
- **Cross-sensitivity** (reacts to multiple gases, not selective)  
- Requires **calibration** for accuracy  

---

#  Conclusion
The **MQ135 gas sensor** is an effective solution for monitoring air quality due to its **wide gas detection range** and **ease of use**. Although it lacks selectivity for individual gases, it is widely applied in **IoT, environmental monitoring, and safety systems**. Calibration and interpretation of its **Freundlich absorption curves** are essential for accurate measurements.

---
# Reference

- [MQ135 Gas Sensor Datasheet – SparkFun](https://www.electronicoscaldas.com/datasheet/MQ-135_Hanwei.pdf)
