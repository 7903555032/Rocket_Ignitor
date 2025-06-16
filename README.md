# Rocket_Ignitor
# ESP8266 Rocket Ignitor (Blynk-controlled)

🚀 **Remote rocket ignitor system using ESP8266, Blynk app, NPN transistor (2N2222), and IRF510 MOSFET**

## 📌 Features
- Remote ignition using Blynk app
- Status LED indicator
- 2N2222 used to drive IRF510 safely
- Safe boot state (ignitor OFF)

## ⚡ Hardware
- ESP8266 NodeMCU
- 2N2222 NPN transistor
- IRF510 MOSFET
- 1kΩ resistor (base current limit)
- Status LED + resistor
- Ignitor load

## 🛠️ Circuit Summary
- NodeMCU D1 → 1kΩ → 2N2222 base  
- 2N2222 collector → IRF510 gate  
- IRF510 source → GND  
- IRF510 drain → Ignitor negative  
- Ignitor positive → Power (via battery/supply)

## 🐍 Code highlights
- Blynk Virtual Pin V0 controls ignitor
- Logic inverted: D1 LOW = ignitor ON
- Safe start with ignitor OFF on boot

## 🚀 How to use
- Connect hardware as above
- Flash code to ESP8266
- Open Blynk app and press button (V0)
