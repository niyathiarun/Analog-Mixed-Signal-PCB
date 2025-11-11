# ⚙️ Analog–Mixed Signal PCB Project  

## 🧠 Project Overview  
This project focuses on designing and implementing a **mixed-signal printed circuit board (PCB)** that integrates both **analog** and **digital** subsystems on a single platform.  
The design features an **ATmega8L microcontroller** as the digital processing unit and an **operational amplifier (Op-Amp)** for analog signal conditioning.  

This project demonstrates key aspects of **analog–digital interfacing**, **signal conditioning**, **noise isolation**, and **mixed-signal PCB design principles**.  
All schematics, layouts, and fabrication outputs were created using **KiCad EDA**.

---

## 🎯 Objectives  

- To design and simulate a **mixed-signal circuit** combining analog and digital components.  
- To interface an **Op-Amp**-based analog conditioning circuit with a **microcontroller ADC**.  
- To implement effective **ground separation and power filtering** for signal integrity.  
- To generate **Gerber and drill files** for PCB fabrication and validation.  
- To gain hands-on experience in **mixed-signal design workflow** using KiCad.  

---

## 🧩 Key Features  

- **Microcontroller:** ATmega8L-8A (8-bit AVR MCU operating at 8 MHz)  
- **Analog Section:** Op-Amp-based amplifier and filter network  
- **Power Section:** 5V regulated supply with decoupling capacitors and ferrite bead  
- **Ground Planes:** Independent **GNDA** (Analog Ground) and **GNDD** (Digital Ground)  
- **Signal Interface:** Audio connector for analog input/output  
- **Design Tool:** KiCad 9.0.3  
- **Layers:** Two-layer PCB  
- **Fabrication Output:** Gerber and Drill files ready for manufacturing  

---

## 🧠 Circuit Explanation  

### 🔸 1. ATmega8L Microcontroller Section  
- Serves as the **digital control and processing unit**.  
- Reads analog signals from the op-amp through its **ADC pins**.  
- Capable of further processing, control, or display applications.  
- Decoupling capacitors are placed near **VCC** and **AVCC** pins to ensure stable ADC readings.  

### 🔸 2. Op-Amp Signal Conditioning Section  
- Amplifies and filters analog signals before feeding them into the ADC.  
- Provides clean and accurate analog voltages for digital conversion.  
- Includes RC filtering for stability and noise suppression.  
- Powered by the same 5V line as the MCU, isolated using ferrite bead and bypass capacitors.  

### 🔸 3. Power & Ground Separation  
- Power input through a **5V regulated line**.  
- **Ferrite bead** isolates analog and digital power domains.  
- **GNDA** and **GNDD** connected through a single low-impedance point near the power input.  
- This reduces cross-domain noise coupling and ensures better ADC accuracy.  

---

## 📐 PCB Design Highlights  

| Aspect | Description |
|--------|--------------|
| **Board Type** | 2-layer PCB |
| **Track Width** | Optimized based on current requirements |
| **Via Usage** | Minimal, used only for signal transitions |
| **Placement** | Clear separation between analog and digital components |
| **Ground Strategy** | Split ground plane with a single-star connection |
| **Decoupling** | 0.1µF ceramic + 10µF electrolytic capacitors near power pins |
| **Design Checks** | Passed ERC and DRC validation in KiCad |

---

## 📂 Repository Structure  

Analog-Mixed-Signal-PCB/
│
├── Schematic/
│ └── mixed_signal_project.kicad_sch
├── schematic_preview.png
│
├── PCB_Design/
│ └── mixed_signal_project.kicad_pcb
│ └── pcb_layout.png
│
├── Fabrication_Files/
│ ├── Gerber/
│ └── Drill_Files/
│ └── Gerber_drill_layout.png
│
└── README.md

---

## 🧰 Tools and Components  

| Category | Details |
|-----------|----------|
| **EDA Software** | KiCad 9.0.3 |
| **Microcontroller** | ATmega8L-8A |
| **Operational Amplifier** | LM358 / LM741 |
| **Power Source** | 5V DC Regulated Input |
| **Passive Components** | Resistors, capacitors, ferrite bead |
| **Connector** | Audio Jack (Analog I/O) |
| **Capacitors** | 0.1µF (decoupling), 10µF (filtering) |

---

## ⚡ Fabrication Notes  

- **Track Width:** 0.25 mm  
- **Clearance:** 0.2 mm  
- **Hole Diameter:** 0.8 mm  
- **Silkscreen:** Includes all reference designators and pin numbers  
- **Gerber Verification:** Done using Gerber Viewer before upload  
- **Board Type:** Standard FR-4 substrate, 1.6 mm thickness  

---

## 📈 Design Validation  

- ✅ **ERC (Electrical Rules Check):** No unconnected or shorted nets  
- ✅ **DRC (Design Rules Check):** Fully passed in KiCad  
- ✅ **Gerber Verification:** Verified visually for alignment and polarity   

---

## 🧩 Applications  

This mixed-signal PCB design has a wide range of **educational and industrial applications**, such as:  

- 🎛️ **Sensor Interface Systems** – conditioning analog sensor outputs before ADC conversion.  
- 🎚️ **Data Acquisition Systems** – capturing analog signals for processing in microcontrollers.  
- 🔊 **Audio Signal Processing** – amplifying and filtering low-level audio inputs.  
- 🧮 **Embedded Control Units** – combining analog feedback with digital decision logic.  
- 🧠 **Learning Platform** – for understanding mixed-signal PCB layout techniques.  

---

## 🧩 Learning Outcomes  

- Designed a **mixed-signal circuit** with analog–digital coexistence.  
- Implemented **noise isolation** and **power decoupling** techniques.  
- Created a **fabrication-ready PCB** with Gerber and drill files.  
- Practiced **KiCad design workflow** — schematic → layout → Gerber.  
- Gained insight into **real-world PCB manufacturing constraints**.  

---

## 🧑‍💻 Author  

**Niyathi Arun Kurthkoti**  
🎓 Electronics and Communication Engineering Student  
💡 Enthusiastic about Embedded Systems, PCB Design, and IoT  
📍 Passionate about creating real-world hardware solutions  

📫 *Connect with me:*  
[🔗 LinkedIn](www.linkedin.com/in/niyathiarun) 

---
