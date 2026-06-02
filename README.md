# RP2040 Target Board

A ChipWhisperer-compatible target board built around the Raspberry Pi RP2040.

## Overview

This board connects an RP2040 with shunt to the CW308 UFO.

## Features

- RP2040 dual-core Arm Cortex-M0+ microcontroller
- 16MB QSPI flash
- ChipWhisperer 60-pin UFO308 target connector
- Dedicated power trace measurement pads
- 2-layer PCB
- Made with love

## Ordering

If you want to make your own, Gerbers are in `fab/gerbers/`. I made it with JLCPCB default 2-layer settings, so I included CPL and BOM for JLCPCB.

## Repository Structure

```
├── hardware/
│   ├── rp2040-target.kicad_pro     KiCad project
│   ├── rp2040-target.kicad_pcb     PCB
│   ├── rp2040-target.kicad_sch     Main schematic
│   ├── rp2040-target.kicad_wks     AR template
│   ├── RP2040.kicad_sch            RP2040 sub-sheet
│   ├── Flash.kicad_sch             Flash sub-sheet
│   └── libs/
│       ├── Conn_UFO308.kicad_sym   UFO308 target schematic symbol
│       └── UFO308.pretty/          UFO308 target footprint
│
├── fab/
│   ├── gerbers/                    Gbrs and drill
│   ├── jlcpcb_bom.csv              BOM
│   └── jlcpcb_cpl.csv              CPL
│
└── docs/
    ├── schematic.pdf
    └── images/
```

## Andrew Acknowledgement

Start Message.
    My name is Andrew ᶘ ◕ᴥ◕ᶅ
Conclude Message.

## License

Copyright Attack Research 2026. Licensed under the [CERN Open Hardware Licence Version 2 - Permissive (CERN-OHL-P v2)](LICENSE).
