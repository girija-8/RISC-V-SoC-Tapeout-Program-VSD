# ⚡ VLSI Open-Source EDA Tools Setup

This repository contains the **setup, configuration, and verification** of open-source **EDA tools** that power digital and analog SoC design.  
The goal is to create a ready-to-use environment for RTL design, simulation, synthesis, and physical design.

---

## 🔧 Installed Tools & Purpose

| 🛠️ Tool | 💡 Why It’s Used | 🔍 Verification | 
|---------|------------------|-----------------|
| **Yosys** | Logic synthesis (convert RTL → gate-level netlist). | `yosys -V` |
| **Icarus Verilog** | Verilog simulation & functional verification. | `iverilog -V` |
| **GTKWave** | View waveforms from simulation (`.vcd` files). | `gtkwave --version` | 
| **Ngspice** | Analog & mixed-signal SPICE-level simulation. | `ngspice -v` | 
| **Magic** | Layout editor for VLSI design. | `magic -version` |
| **OpenLANE** | Complete RTL → GDSII flow (synthesis, placement, routing). | `docker --version` <br> `make test` | 

---

## ⚙️ Setup & Installation
👉 Full installation commands and step-by-step instructions are available here: [Installation.md](./Installation.md)

---

## 🖥️ Environment Details
- **OS:** Ubuntu 20.04 LTS (running in VirtualBox) 🐧  
- **CPU:** 4 vCPUs  
- **RAM:** 6 GB  
- **Disk:** 50 GB HDD  

(Also works with **WSL** or a dedicated Ubuntu installation.)

---

## 🌟 Highlights
- Verified installation of **six essential open-source EDA tools**.  
- Environment is now ready for **RTL design, simulation, and chip layout workflows**.  
- Documentation can be reused by anyone setting up the same flow.  

---

## 🙌 Credits
A big thanks to:  
- **IIT Gandhinagar** 🏫  
- **VSD Team & Kunal Ghosh Sir** 👨‍🏫  
- The global **Open-Source EDA Community** 🌍  

for making VLSI learning accessible and free.

---

## 🏷️ Tech Tags
![Linux](https://img.shields.io/badge/Linux-Ubuntu_20.04-blue?logo=ubuntu&style=for-the-badge)
![Yosys](https://img.shields.io/badge/Yosys-Synthesis-purple?style=for-the-badge)
![Verilog](https://img.shields.io/badge/Icarus-Verilog-orange?style=for-the-badge)
![GTKWave](https://img.shields.io/badge/GTKWave-Waveforms-green?style=for-the-badge)
![Ngspice](https://img.shields.io/badge/Ngspice-SPICE-red?style=for-the-badge)
![Magic](https://img.shields.io/badge/Magic-Layout-lightgrey?style=for-the-badge)
![OpenLANE](https://img.shields.io/badge/OpenLANE-RTL--to--GDSII-yellow?style=for-the-badge)

