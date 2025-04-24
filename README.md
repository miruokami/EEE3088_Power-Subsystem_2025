# EEE3088F 2025 Micro-Mouse Power Subsystem

Welcome to the repository for the **EEE3088F Micro-Mouse Power Subsystem Project**. This project focuses on designing and implementing a compact and efficient power module for a simplified micro-mouse robot. The goal is to meet all electrical and mechanical specifications, stay within a strict budget, and ensure seamless integration with the larger micro-mouse system.

## 👥 Team Members

- Student 1: SDZLIY001
- Student 2: CHGSHA008


## 📁 Repository Structure
```
> Power subsystem folder with 
  ├── gerbers / # Gerber files for PCB production
  ├── bom (PowerSchematic) / # Bill of Materials (.csv)
  ├── pos / # Pick-and-Place (PnP) files
  ├── screenshots / # Screenshots from JLCPCB uploads
  ├── schematics / # Final schematic file
  ├── pcb_layout 
```

## 🧠 Project Overview

This project involves designing the **power module** for the Micro-Mouse. The rest of the system — processor, sensing module, and motherboard — are pre-designed. The role is to design a subsystem that meets the power needs of the full system while adhering to design and budget constraints.

### Key Objectives

- Power 4 bidirectional motors (2x 200mA, 2x 500mA).
- Include battery monitoring with an INA219 over I2C.
- Implement dual-mode battery charging from a 9V input.
- Provide 3.3V (300mA) and 5V (1.5A) regulated outputs.
- Include external load switching (2x 1A High Side).
- Implement a low-power ON/OFF switch (<30µA OFF draw).
- Integrate USB-C (providing 9V out from USB host).
- Fit within 82x60mm PCB dimensions.
- Use correct JST and 2x16 connector footprints.

## 🛠️ Tools & Technologies

- **EDA Software**: EasyEDA / KiCAD / Altium (for PCB design)
- **Simulation**: LTSpice / MATLAB (optional)
- **PCB Manufacturer**: JLCPCB
- **Microcontroller**: STM32L476 (handled on separate processor board)
- **GitHub**: Version control and collaboration

## ✅ Requirements Summary

| Requirement | Description |
|-------------|-------------|
| Power Supply | 3V3 @ 300mA, 5V @ 1.5A |
| Charging | Dual-mode: 200mA and ~600mA |
| Battery Monitoring | INA219 on I2C |
| Motors | 2x 200mA, 2x 500mA |
| USB-C | Must provide 9V out |
| External Loads | 2x 1A, High-Side Switching |
| ON/OFF Switch | <30µA draw in OFF state |
| Budget | $35 per student (includes PCB + components) |

### 🛠️ PCB Ordering  
1. Upload `gerbers/*.zip` to JLCPCB.  
2. Use the provided `bom.csv` and `pos.csv` for assembly.  
3. Ensure components are in stock (check JLCPCB's inventory).
   
## 🧪 Testing Procedure

Testing will be performed using a standardised jig that validates:
- USB-C power output
- Battery charging behavior
- Regulated outputs (5V, 3.3V)
- Motor driver functionality
- INA219 battery monitoring
- ON/OFF switch behavior

## 🔗 Important Links

- [Veritasium Micro-Mouse Inspiration Video](https://www.youtube.com/watch?v=ZMQbHMgK2rw)
- [Micro Robotics Battery](https://www.robotics.org.za/802540)
- [JST Connector Specs](https://www.robotics.org.za/JST-PH-2P-90)
- [JLCPCB](https://jlcpcb.com
