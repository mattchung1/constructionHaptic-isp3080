# constructionHaptic-isp3080

A hardware project using the InsightSiP ISP3080 UWB/BLE module to create a haptic-feedback device.  
The system delivers directional or event-based haptic cues to a wearer based on the position or movement of a paired tag device.

---

## Repository Structure

```
root/
├── altiumDocs/ # Altium Designer PCB + schematic source files
├── autoCadDocs/ # Board outline, mechanical drawings, DXF files
├── exampleLayout/ # Example board layout exports, previews, gerber illustrations
└── README.md
```

---

## Project Overview

This repository contains the hardware design for a wearable haptic device that uses UWB positioning to notify the user through vibration patterns. A remote tag device transmits UWB signals, and the wearable unit interprets relative movement or proximity, generating haptic feedback accordingly.

### Key Features (In Progress)
- **ISP3080-UX integration** for compact UWB + BLE communication  
- **DRV8837 and similar H-bridge drivers** for multiple vibration actuators  
- **TPS63802 buck-boost power regulation** for stable VMOT and logic rails  
- **Optional IMU support** for on-device motion awareness (BNO085/BMI270 variants)  
- **Flexible PCB (FPCB) layout** with stiffener considerations for high-current haptics  
- **Modular antenna tuning footprint** for UWB monopole optimization  

The project is currently under active development.

---

## Hardware Stack

- **Main MCU/Radio:** InsightSiP ISP3080-UX  
- **Actuation:** Multiple haptic motors driven through DRV8837 H-bridges  
- **Power:**  
  - TPS63802 buck-boost converter for system power  
  - TPS7A02 linear regulator for logic rails  
- **Sensors (optional):**  
  - BNO085 IMU (I²C) or BMI270 IMU  
- **PCB:**  
  - Flex PCB with stiffeners  
  - Custom board outline from AutoCAD DXF import  
  - Tested under Altium DRC for mask, drill, and copper constraints  

---

## Current Status

- [x] Electrical schematic drafted  
- [x] Initial PCB layout complete  
- [x] Board outline finalized through AutoCAD  
- [x] Gerber and NC drill export verified (PCBWay-ready)  
- [ ] Prototype fabrication & assembly  
- [ ] Firmware integration with UWB tag device  
- [ ] Haptic feedback patterns + motion rules  
- [ ] Final device enclosure and mechanical integration  

---

## Example Layouts

Example exported images, gerbers, or previews are stored under:

```
exampleLayout/
```

This includes representative snapshots of the PCB routing, mechanical outline, mask layers, and silkscreens for documentation and review.

---

## Tools Used

- **Altium Designer** (schematics + PCB)
- **AutoCAD 2026** (board outline generation)
- **InsightSiP SDK + Nordic nRF Connect** (firmware development, works in progress)
- **PCBWay** (fabrication pipeline)
