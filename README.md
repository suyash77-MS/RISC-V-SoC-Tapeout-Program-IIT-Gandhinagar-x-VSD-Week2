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

SoC stands for System On Chip. It is a small integrated chip that contains all the required components and circuits of a particular system. The components of SoC include CPU, GPU, Memory, I/O devices, etc. SoC is used in various devices such as smartphones, Internet of Things appliances, tablets, and embedded system applications. In this article, we are going to see the architecture and architectural features of SoC.

Features of SoC:

Integration: Combines CPU, memory, I/O interfaces, GPU, and more on a single chip.

Compact Design: Enables small, space-efficient devices.

Power Efficiency: Reduces energy use by optimizing internal communication.

Performance: Faster operation due to low-latency connections.

Customizable & Flexible: Parts can be selected per application.

Low Latency & Simplified Interconnect: Shorter data paths and easier communication management.

Advanced Packaging: Uses techniques like 3D stacking and system-in-package.

Multicore & Heterogeneous Computing: Supports multiple cores and diverse processors for optimized tasks.

Advantages

Small size, low power, cost-effective, flexible, mass-producible, all-in-one chip.

Disadvantages

Long design time (6–12 months), hard to replace faulty components, limited visibility.

Uses

Smartphones, tablets, smartwatches, computers

IoT and home automation

Embedded systems with microcontrollers

### 🔹 Components of a Typical SoC

The diagram below shows the components present on SOC

<img width="447" height="413" alt="image" src="https://github.com/user-attachments/assets/3902c873-3538-49b1-9216-f5b6b102b2ea" />

The basic architecture of SoC is shown in the above figure which includes a processor, DSP, memory, network interface card, CPU, multimedia encoder/decoder, DMA, etc.

Processor:  It is the heart of SoC, usually SoC contains at least one or more than one coprocessor. It can be a microcontroller, microprocessor, or DSP. Most of the time DSP is used in every SoC as a processor.

DSP: DSP stands for Digital Signal Processor. It is included in SoC to perform signal processing operations such as data collection, data processing, etc. it is also used for the purpose of decoding the images.

Memory: Memory is used in SoC for the purpose of storage. It may be a volatile or non-volatile memory. Volatile memory includes RAM there are two types of RAM one is SRAM and another is DRAM. The non-volatile memory includes ROM.

Encoder/Decoder: Used for the purpose of interrupting information and converting it into codes.

Network Interface card: SoC has an internal interface or bus or network to connect all individual blocks. Basically, the Network interface card provides a connection of the network to the system.

GPU: GPU stands for Graphical Processing Unit, used in SoC to visualize the interface. GPU is specially designed to speed up the operations related to image calculations. The basic blocks of the GPU are the Bus interface, Power Management Unit, Video Processing unit, Graphics Memory Controller, Display interface, etc.

Peripheral devices: Externally connected devices/interfaces such as USB, HDMI, Wi-Fi, and Bluetooth are included in peripheral devices. This device is used in SoC to perform various operations.

UART: Universal Asynchronous Receiver Transmitter is included in SoC which is used to transmit or receive serial data. Voltage regulators, Oscillators, clocks, and ADC/DAC are also part of SoC.


### 🔹 Why BabySoC?

1. Baby SoC – Overview (In Depth)

A Baby SoC is a miniaturized System on Chip, designed primarily as a learning, experimental, and prototyping platform for students, engineers, and researchers to understand SoC design from RTL to silicon.

Definition:
A SoC integrates all major components of a computer or embedded system—CPU, memory, peripherals—onto a single chip. A Baby SoC simplifies this by including only the essential components, typically one CPU core, small memories, and basic peripherals, while still demonstrating real SoC concepts like instruction execution, memory access, and peripheral interfacing.

The Figuare below shows how baby SOC look like 

<img width="1033" height="560" alt="image" src="https://github.com/user-attachments/assets/2c963d5c-a33f-4b2f-8c42-6ac8f302a8c7" />

Purpose and Goals:

Educational: Helps students grasp concepts like RTL design, bus protocols, CPU-memory-peripheral interaction, and verification.

Hands-on Design Experience: Enables simulation, synthesis, and optionally FPGA implementation or ASIC tapeout.

Proof-of-Concept Platform: Demonstrates integration of CPU, memory, and peripherals without the complexity of a full-scale commercial SoC.

Exploration of RTL-to-GDSII Flow: Users can learn end-to-end chip design, including:

RTL Design: Writing Verilog/SystemVerilog for CPU, memory, bus, and peripherals.

Functional Verification: Testbenches, simulation, waveform analysis, assertion-based verification.

Synthesis: Converting RTL into gate-level netlist using tools like Yosys.

Place-and-Route: Mapping netlist onto FPGA or ASIC standard cells.

Timing Analysis: Ensuring the design meets target frequency using STA (Static Timing Analysis).

Tapeout (Optional): Using open-source PDKs like Sky130 for real silicon fabrication.

Architecture Philosophy:

Keep it small but representative: Demonstrates the entire SoC design lifecycle.

Focus on modularity: Each component (CPU, memory, peripherals) is a standalone RTL block with well-defined interfaces.

Emphasize interconnectivity: The bus/interconnect is central, showing how data and instructions flow across the chip.

Introduce verification mindset: Even a Baby SoC requires testbenches, monitors, scoreboards, and assertions for functional correctness.

2. Baby SoC – Components 

Let’s break down all components with their purpose, design considerations, and interaction with other blocks.

a) CPU Core (RISC-V or similar)

Role: Brain of the SoC; executes instructions from program memory.

Key Features in Baby SoC:

Typically 32-bit RISC-V RV32I, a simple integer-only core.

Supports basic instructions: arithmetic, logic, load/store, branches, jumps.

Often single pipeline stage or a simple 3-stage pipeline for educational purposes (fetch-decode-execute).

Design Considerations:

Instruction fetch from IMEM.

Data read/write via DMEM or memory-mapped peripherals.

Simple control logic: instruction decoding, ALU control, program counter update.

Interfaces:

IMEM interface: fetch instructions.

DMEM interface: read/write data.

Bus interface: communicates with peripherals.

Optional interrupt lines: respond to external events.

b) Instruction Memory (IMEM)

Role: Stores program instructions for CPU execution.

Characteristics:

Small size (e.g., 4–16 KB for a Baby SoC).

Can be implemented as ROM or SRAM for FPGA.

Design Considerations:

Word-aligned access (32-bit).

Supports synchronous read (read on clock edge).

Often loaded at boot via memory initialization file (.hex/.mem).

c) Data Memory (DMEM)

Role: Stores runtime data for CPU operations.

Characteristics:

Small SRAM block (4–16 KB).

Word-aligned access with read/write support.

May implement byte-enable signals for partial word writes.

Design Considerations:

Handle simultaneous CPU read/write requests.

Ensure correct timing for synchronous access.

d) Bus / Interconnect

Role: Connects CPU, memories, and peripherals. Acts as the communication backbone.

Common Choices for Baby SoC:

Simple bus: Single master (CPU), multiple slaves (IMEM, DMEM, peripherals).

Protocol examples: Wishbone, AHB-Lite.

Design Considerations:

Address decoding logic for slave selection.

Support read/write operations.

Optional handshaking for ready/valid signals.

e) Peripherals

Role: Provide interfaces to the external world.

Common Peripherals:

UART: Serial communication for debugging/output.

GPIO: Simple digital input/output pins.

Timer / PWM: Basic timing functions.

Design Considerations:

Memory-mapped access: CPU reads/writes specific addresses.

Interrupt generation for events like timer overflow or UART data ready.

Simple state machines for peripheral control.

f) Clock and Reset

Role: Synchronizes all components and ensures proper startup.

Details:

Single global clock for synchronous design.

Reset line initializes CPU, memory, and peripherals.

Optional asynchronous reset to handle FPGA or ASIC startup conditions.

g) Interrupt Controller 

Role: Handles external or peripheral interrupts.

Details:

Assigns priorities to interrupts.

Signals CPU to jump to interrupt service routine.

Helps teach asynchronous event handling in SoCs.

h) Debug Interface 

Role: Helps in verifying CPU execution and peripheral interaction.

Details:

Can be UART-based debug prints.

Or a simple JTAG/SWD interface for step-by-step execution.

Monitors instruction fetch, data read/write, and peripheral activity.

i) Optional Enhancements

Simple caches for instruction/data.

Low-power mode or clock gating demonstration.

Scan chains for DFT (Design for Testability).

Minimal ALU extensions: multiply/divide instructions

### 🔹 Role of Functional Modelling in Baby SOC

Functional Modelling (FM) creates a high-level simulation of the SoC before RTL or hardware implementation. It is crucial for early verification, error detection, and design exploration.

Key Points:

Early Verification: Simulates CPU, memory, bus, and peripherals to catch design flaws before RTL.

Faster Development: FM in Python/SystemC/MATLAB is quicker than RTL synthesis or FPGA testing.

Design Exploration: Allows testing different configurations (memory size, bus width, instruction set) efficiently.

Error Detection: Detects instruction execution, memory access, and communication issues early.

Educational & Learning Tool: Helps understand SoC component interactions without low-level hardware details.

Supports Co-Simulation: FM can integrate with RTL or FPGA simulations to validate functionality and timing together.

Components Modeled:

CPU: Executes instructions; checks pipelines.

Instruction & Data Memory (IMEM & DMEM): Verifies read/write operations.

Peripherals (UART, GPIO, Timers): Ensures correct I/O interaction.

Bus/Interconnect: Validates communication and arbitration.

Clock & Reset: Checks synchronous operation and system reset.

### 📖 Reference Notes

- **Fundamentals of SoC Design**  
  A comprehensive guide covering the basics of System on Chip (SoC) design, including architecture, components, and design methodologies.

- **[VSDBabySoC GitHub Repository](https://github.com/manili/VSDBabySoC)**  
  An open-source project showcasing a small mixed-signal SoC featuring a RISC-V processor (RVMYTH), Phase-Locked Loop (PLL), and Digital-to-Analog Converter (DAC).


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
