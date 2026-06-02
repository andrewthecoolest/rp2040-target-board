# RP2040 Target Board

A ChipWhisperer-compatible target board built around the Raspberry Pi RP2040 microcontroller, designed for side-channel analysis and fault injection research.

## Overview

This board connects to a ChipWhisperer capture platform via the 20-pin UFO308 target connector. It exposes power measurement shunt traces (TRACED0–3, TRACECLK) for electromagnetic and power side-channel analysis, and includes a QSPI flash chip with a DIP switch to switch the flash data lines in or out of the measurement path.

## Features

- RP2040 dual-core Arm Cortex-M0+ microcontroller
- QSPI flash with switchable trace path (pre/post-DIP measurement points)
- ChipWhisperer 20-pin UFO308 target connector
- Dedicated power trace measurement pads
- 2-layer PCB

## Repository Structure

```
├── hardware/
│   ├── rp2040-target.kicad_pro     KiCad project
│   ├── rp2040-target.kicad_pcb     PCB layout
│   ├── rp2040-target.kicad_sch     Top-level schematic
│   ├── rp2040-target.kicad_wks     Title block template
│   ├── RP2040.kicad_sch            RP2040 sub-sheet
│   ├── Flash.kicad_sch             Flash sub-sheet
│   └── libs/
│       ├── Conn_UFO308.kicad_sym   UFO308 schematic symbol
│       └── UFO308.pretty/          UFO308 footprint
│
├── fab/
│   ├── gerbers/                    Gerber and drill files
│   ├── bom.csv                     Bill of materials
│   └── cpl.csv                     Pick-and-place / CPL
│
└── docs/
    ├── schematic.pdf
    └── images/
```

## Manufacturing

Gerbers, drill files, and the Gerber job file are in `fabrication/`. The board has been fabricated with JLCPCB; JLCPCB part numbers are included in the BOM.

## License

Copyright Attack Research 2026. Licensed under the [CERN Open Hardware Licence Version 2 - Permissive (CERN-OHL-P v2)](LICENSE).
