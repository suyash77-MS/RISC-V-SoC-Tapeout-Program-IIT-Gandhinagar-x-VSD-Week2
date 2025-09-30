🏆 #IIT Gandhinagar – VSD RISC-V SoC Tapeout Program

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/799c16ad-9e69-4c35-8e1e-2be1aaeaadb3" />


🚀 Overview

A silicon-proven, open-source SoC design journey where I learned the complete RTL-to-GDS flow on Sky130 PDK, starting from Verilog RTL, simulation, synthesis, optimizations, GLS, and tapeout methodologies.
This program by VSD and IIIT Gandhinagar gave me hands-on exposure to industry-grade open-source EDA tools and real fabrication-ready workflows.

🔧 Tools & Technologies Used


<img height="28" src="https://img.shields.io/badge/Icarus%20Verilog-FF4500?logo=verilog&logoColor=white"> <img height="28" src="https://img.shields.io/badge/GtkWave-4B8BBE?logo=waveform&logoColor=white"> <img height="28" src="https://img.shields.io/badge/Yosys-FFD700?logo=logic&logoColor=black"> <img height="28" src="https://img.shields.io/badge/OpenSTA-1E90FF?logo=timing&logoColor=white"> <img height="28" src="https://img.shields.io/badge/OpenROAD-228B22?logo=flow&logoColor=white"> <img height="28" src="https://img.shields.io/badge/Magic%20VLSI-6A0DAD?logo=magic&logoColor=white"> <img height="28" src="https://img.shields.io/badge/KLayout-FF0000?logo=layout&logoColor=white"> <img height="28" src="https://img.shields.io/badge/OpenLane-007ACC?logo=eda&logoColor=white"> <img height="28" src="https://img.shields.io/badge/SKY130%20PDK-FF6600?logo=chip&logoColor=white">


📚 Key Concepts Learned

📐 Verilog RTL Design & Simulation

RTL coding best practices (blocking vs non-blocking, sensitivity lists)

Writing testbenches with Icarus Verilog

Waveform analysis & debugging with GTKWave

⚙️ Logic Synthesis & Mapping

RTL → Gate-level mapping using Yosys

Flat vs Hierarchical synthesis

Timing-aware synthesis using Sky130 standard cells

⏱ Timing & Libraries

Understanding .lib files (TT, SS, FF)

Setup, hold, and timing arcs with OpenSTA

Effect of timing constraints on synthesis

🔄 Optimizations

Combinational optimizations → boolean simplification, dead logic removal

Sequential optimizations → retiming, removal of unused flops

Power–delay–area trade-offs with different coding styles

🧩 Simulation Mismatches & GLS

Gate-level simulation with back-annotated netlists

Debugging simulation-synthesis mismatches

Blocking vs Non-blocking pitfalls

🏭 RTL to GDSII Flow

Placement & routing with OpenROAD/OpenLane

Layout vs schematic (LVS) checks with Magic + Netgen

DRC, parasitic extraction, and timing closure

Tapeout preparation (Sky130 PDK signoff flow)

🧪 Lab Work Done

Verilog RTL Labs → designed good_mux, counters, flops with proper coding styles

Yosys Synthesis Labs → synthesized mux, flops, if/case constructs

Timing Labs → analyzed .lib, TT/SS/FF timing variations

Optimization Labs → experimented with combinational + sequential optimizations

GLS Labs → verified gate-level netlists and mismatches

RTL-GDS Flow Labs → ran OpenLane flow on synthesized blocks, viewed layouts in Magic/KLayout



📝 Projects & Contributions

RTL & GLS Verification → clean Verilog + gate-level validated designs

Synthesis Reports → timing, area, and power comparisons

Optimization Studies → coding styles impact on synthesis results

RTL-to-GDSII Demo → complete flow on Sky130 using OpenLane

# RISC-V Tapeout SoC by VSD and IIT Gandhinagar

**Program:** RISC-V Reference SoC Tapeout Program  
**Organized by:** VSD & IIT Gandhinagar  


# 📘 Week 2 – BabySoC Fundamentals & Functional Modelling

## 🎯 Objective

To understand **System-on-Chip (SoC) fundamentals** and perform **functional modelling** of BabySoC using **Icarus Verilog** & **GTKWave**.

---

## 📚 Part 1 – Theory (Conceptual Understanding)

* [🔹 What is a System-on-Chip (SoC)?](#-what-is-a-system-on-chip-soc)
* [🔹 Components of a Typical SoC](#-components-of-a-typical-soc)
* [🔹 Why BabySoC?](#-why-babysoc)
* [🔹 Role of Functional Modelling](#-role-of-functional-modelling)
* [📖 Reference Notes](#-reference-notes)

### 🔹 What is a System-on-Chip (SoC)?

A **System-on-Chip (SoC)** integrates CPU, memory, peripherals, and interconnect into a single silicon die for compact and efficient design.

### 🔹 Components of a Typical SoC

1. **CPU (Core)** – Executes instructions.
2. **Memory** – SRAM, DRAM, caches for program/data.
3. **Peripherals** – UART, I2C, SPI, GPIO, ADC/DAC.
4. **Interconnect** – Bus/NoC (AXI, AHB, Wishbone).

### 🔹 Why BabySoC?

* A **simplified SoC** for learning.
* Includes **minimal CPU, memory, and bus**.
* Focuses on **concept clarity** before complex RTL.

### 🔹 Role of Functional Modelling

* Validates **architecture correctness**.
* Checks **dataflow and control signals**.
* Serves as a **blueprint for RTL & verification**.

### 📖 Reference Notes

[Fundamentals of SoC Design](https://github.com/hemanthkumardm/SFAL-VSD-SoCJourney/tree/main/11.%20Fundamentals%20of%20SoC%20Design)

---

## 🧪 Part 2 – Labs (Hands-on Functional Modelling)

* [🔧 Tools Installation](#-tools-installation)
* [🛠 Lab Steps](#-lab-steps)
* [⚙️ Workflow Summary](#%EF%B8%8F-workflow-summary)

### 🔧 Tools Installation

* [Icarus Verilog](http://iverilog.icarus.com/) → For simulation.
* [GTKWave](http://gtkwave.sourceforge.net/) → For waveform analysis.

### 🛠 Lab Steps

1. [Clone BabySoC Project Repo](https://github.com/hemanthkumardm/SFAL-VSD-SoCJourney/tree/main/12.%20VSDBabySoC%20Project)
2. Compile Verilog modules with `iverilog`.
3. Run simulation with `vvp` to generate `.vcd` waveforms.
4. Open `.vcd` in GTKWave → analyze **reset, clock, dataflow**.
5. Capture screenshots + explain behavior.

### ⚙️ Workflow Summary

* Functional modelling bridges **theory ↔ practice**.
* BabySoC labs teach **simulation flow, debugging, and waveform analysis**.
* Builds base for **RTL, verification, and RTL-to-GDSII**.

---
