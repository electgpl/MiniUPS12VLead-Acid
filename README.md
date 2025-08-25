# Mini UPS 12V Lead-Acid | UVP Protector - Buck - Charger - Bypass

This project implements a **mini uninterruptible power supply (UPS)** designed for **12V Lead-Acid AGM/GEL batteries**.  
It integrates a dedicated **CN3767 lead-acid charger**, a **PMOS + Schottky bypass circuit**, a **TPS54360 buck regulator**, and an **undervoltage protection (UVP)** stage to ensure safe battery operation.  

The design focuses on maintaining stable 12V output while protecting the battery from undervoltage damage and ensuring correct charging cycles.  

---

## 🔑 Features

- **Battery chemistry supported:** 12V Lead-Acid (AGM, GEL).  
- **CN3767-based lead-acid charger** with constant-current/constant-voltage (CC/CV) charging.  
- **Bypass system:**  
  - PMOS + Schottky switch circuit.  
  - During charging, disconnects the battery from the load to allow proper charging.  
  - The load is powered instead by a regulated buck supply.  
- **Buck regulator stage:**  
  - Based on **TPS54360** DC/DC converter.  
  - Configured to **13.8V output** for stable system powering during battery charge.  
- **Undervoltage protection (UVP):**  
  - Implemented with **LM393 comparator** and **TL431 reference**.  
  - Controls a **back-to-back PMOS switch**.  
  - Cuts off the battery when voltage falls below **11V**.  
  - Latch-off behavior: system remains disconnected until external power is restored.  
- **2-layer PCB**, designed for compact size, thermal management, and robust operation.  

---

## 📂 Repository structure

- **/schematic/** → Circuit schematic files.  
- **/pcb/** → PCB layout files ready for fabrication.  
- **/doc/** → Technical notes and design explanation.  
- **/img/** → PCB renders and prototype photos.  

---

## 🔧 Typical applications

- DIY 12V backup supply for small systems.  
- Router, modem, or IoT device UPS.  
- Low-power embedded controllers requiring uninterrupted 12V operation.  
- Safe battery-powered test benches.  

---

## 📑 References

- [CN3767 Datasheet (Consonance)](http://www.consonance-elec.com/pdf/datasheet/DSE-CN3767.pdf)  
- [TPS54360 Datasheet (Texas Instruments)](https://www.ti.com/lit/ds/symlink/tps54360.pdf)  
- [LM393 Datasheet (Texas Instruments)](https://www.ti.com/lit/ds/symlink/lm393.pdf)  
- [TL431 Reference Datasheet (Texas Instruments)](https://www.ti.com/lit/ds/symlink/tl431.pdf)  

---

## 📸 Project preview

*(Insert here PCB renders and/or real prototype images)*  

---

## ⚖️ License

This project is released under the **MIT License**.  
You are free to use, modify, and distribute it, provided that proper credit is given.  

---
