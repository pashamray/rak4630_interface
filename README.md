# RAK4630 Interface

An open-source hardware breakout / interface board for the **RAK4630** LoRa module (Nordic nRF52840 + Semtech SX1262), designed in KiCad 9.

## Overview

This board provides a minimal interface around the RAK4630 module, exposing its programming and I/O lines on a header and powering it from a USB-C port. It is intended as a development and flashing carrier for the RAK4630.

## Features

- **RAK4630 module** footprint (nRF52840 MCU + SX1262 LoRa radio)
- **USB-C 2.0 receptacle** for power and data
- **TPD2EUSB30** USB ESD protection
- **TLV62569DBV** step-down DC/DC converter for the 3.3 V rail
- **Reset push button**
- **Solder jumper** for power-rail / option configuration
- **8-pin breakout header** for GPIO / SWD / UART access
- **Test points** for key signals

## Repository layout

```
hardware/
├── kicad/      KiCad 9 project (schematic, PCB, project files)
├── gerber/     Manufacturing outputs (Gerbers + drill files)
└── libs/       Project-specific symbol/footprint/3D libraries (RAK4630)
```

## Manufacturing

Ready-to-fab Gerber and Excellon drill files are provided in `hardware/gerber/`. They follow the standard KiCad naming convention and can be uploaded as-is to most PCB fabrication houses.

## Opening the design

1. Install [KiCad 9](https://www.kicad.org/) or newer.
2. Open `hardware/kicad/rak4630_interface.kicad_pro`.

The RAK4630 symbol, footprint and 3D model are bundled under `hardware/libs/RAK4630/` and are referenced via the project library table — no global library setup is required.

## License

Unless stated otherwise, the hardware design files are released under an open-source hardware license. See repository headers for details.
