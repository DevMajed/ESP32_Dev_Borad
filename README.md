# Custom ESP32 Development Board

**KiCad-based ESP32-WROOM-32 development board with onboard USB-to-UART and regulated 3.3 V power**

![ESP32](https://img.shields.io/badge/MCU-ESP32--WROOM--32-blue)
![KiCad](https://img.shields.io/badge/EDA-KiCad-blue)
![USB](https://img.shields.io/badge/USB--UART-CP2102N-lightgrey)

## Overview

This project explores the design of a **custom ESP32 development board** from schematic capture through PCB design in KiCad.

Rather than using a commercial dev kit, the board integrates the essential support circuitry directly on the PCB:

- **ESP32-WROOM-32** module
- **CP2102N USB-to-UART bridge** for programming and serial communication
- **Micro-USB interface**
- **AMS1117-3.3 regulator** for the 3.3 V rail
- Supporting passives, reset/boot circuitry, and GPIO breakout

The goal was to practice practical embedded-hardware design: power, programming, USB/UART interfacing, component selection, schematic capture, and PCB layout.

## Architecture

```text
Micro USB
   │
   ├── 5 V power ──> 3.3 V regulator ──> ESP32-WROOM-32
   │
   └── USB D+/D− ──> CP2102N ──> UART ──> ESP32

ESP32 GPIO ──────────────────────────────> External interfaces
```

## Design Files

The repository contains the native KiCad project files so the design can be inspected or modified directly:

- `ESP32_Dev_Borad.kicad_sch` — schematic
- `ESP32_Dev_Borad.kicad_pcb` — PCB layout
- `ESP32_Dev_Borad.kicad_pro` — KiCad project
- `libraries/` — project-specific symbols/footprints

## What This Project Demonstrates

- Custom microcontroller board design
- ESP32 hardware integration
- USB-to-UART programming/debug interface
- 5 V to 3.3 V power regulation
- KiCad schematic capture
- PCB layout workflow
- Component and footprint integration

## Status

This is an earlier hardware-design project and is kept as part of my embedded/PCB portfolio. Future revisions could modernize the connector, power architecture, and expansion interfaces.

---

**Author:** [Majed / DevMajed](https://github.com/DevMajed)
