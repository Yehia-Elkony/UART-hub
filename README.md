# 🔁 UART Hub – 8-Port USB to UART Expansion Board (CH348Q)

This project is a compact, high-efficiency **8-channel UART Hub**, designed around the **CH348Q** USB-to-UART bridge. It allows a host system to communicate with up to **eight UART devices** simultaneously using a single **USB-C connection**.

Built for embedded developers and roboticists, this board is a powerful way to expand UART connectivity for systems that require extensive serial communication — such as sensor arrays, motor controllers, GPS modules, or wireless radios.

---

## 🧠 Key Features

- **🔌 CH348Q Multi-UART Bridge**
  - One **USB-C input**, **eight UART outputs**
  - USB-compliant and driver-compatible (CH34x series)
  - Appears as multiple COM ports on host systems

- **📡 UART Output Headers**
  - 8x 4-pin headers (TX, RX, VCC, GND)
  - Supports direct UART peripherals or modules (e.g., Bluetooth, GPS)

- **🛡️ Robust ESD Protection**
  - On all USB and UART lines
  - TVS diodes (USBLC6-2SC6 and PSM712-ES) ensure long-term reliability

- **⚡ Power Input & Management**
  - **USB-C port** for data and power
  - **DC barrel jack** as an alternative 5V source
  - **TPS2116 smart power switch** chooses between USB and DC input

- **🔋 Voltage Regulation**
  - Onboard **LDO regulator** provides stable 5V system power

- **📶 Bluetooth Ready**
  - Optional pin header for UART-based Bluetooth modules (e.g., HC-05)

- **💡 Status Indicator**
  - Green LED shows board power status

---

## 📦 BOM Summary

| Component         | Description                                  | Qty |
|-------------------|----------------------------------------------|-----|
| **CH348Q**         | 8-port USB-to-UART bridge IC (LQFP-48)       | 1   |
| **USB-C Connector**| 16P USB-C port (power + data)               | 1   |
| **DC Power Jack**  | 2.5mm panel-mount barrel jack               | 1   |
| **TPS2116**        | Power switchover controller                 | 1   |
| **LDO Regulator**  | SOT-223 linear voltage regulator            | 1   |
| **TVS Diodes**     | USBLC6 + PSM712 (USB/UART ESD protection)   | 9   |
| **UART Headers**   | 1x4 UART headers (TX/RX/VCC/GND)            | 8   |
| **LED**            | Green 0805 LED (power indicator)           | 1   |
| **Crystal**        | 8MHz crystal with 22pF caps (for CH348Q)    | 1   |
| **Capacitors**     | 0.1uF, 10uF, 22pF (MLCC SMD)                | 11  |
| **Resistors**      | 330Ω, 1kΩ, 2kΩ, 4.7kΩ, 5kΩ (0603 SMD)       | ~25 |

> Full component list available in the BOM file.

---

## 🔌 Power Configuration

The board can be powered via:

1. **USB-C (Default)**  
   Plug into any USB port for both power and UART communication.

2. **DC Barrel Jack (J11)**  
   Supplies external 5V (up to 2.5A).  
   If both USB-C and DC are connected, **TPS2116** selects the preferred source.

---

## 🔧 How to Use

1. **Connect USB-C to Host PC**  
   - Appears as **multiple COM ports**
   - No firmware required — standard **CH34x driver** works on Windows, macOS, Linux

2. **Connect UART Devices**  
   - Use headers J3–J10 (TX, RX, VCC, GND)
   - Plug in UART modules (e.g., Bluetooth HC-05/HC-06, serial sensors)

3. **Power the Board**  
   - Use USB-C or DC Jack (auto-switched)

---

## 📐 Visuals

### 🧩 Schematic  
_Place schematic image here_  
`schematic.png`

### 🧱 3D PCB Render  
_Place 3D PCB render here_  
`3d.png`

---

## 🔧 Applications

- Debugging multiple embedded systems
- Connecting multiple serial sensors to one PC
- Robotic systems with serial motor controllers or modules
- Wireless communication via UART Bluetooth/WiFi modules

---

## 📄 Datasheets & References

- [CH348Q – WCH](http://www.wch-ic.com/products/CH348.html)
- [TPS2116 – Texas Instruments](https://www.ti.com/product/TPS2116)
- [CH34x Drivers (WCH)](https://www.wch.cn/downloads/CH341SER_EXE.html)

---
