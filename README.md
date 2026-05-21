# Split PCB Gamepad

A custom gamepad built on a split PCB design, with two halves connected via a 14-pin ribbon cable connector on each side.

![PCB Preview](./images/preview.jpg)

## Features

- Split PCB — left and right halves connected via ribbon cable
- 14-pin connector on each half
- Compact and ergonomic layout
- USB-C connection to host

## Bill of Materials

| Ref | Component | Value / Model | Qty |
|-----|-----------|---------------|-----|
| U1 | Microcontroller | Pro Micro (ATmega32U4) or RP2040 | 1 |
| SW1–SWn | Mechanical / Tactile Switch | Cherry MX or tactile equiv. | n |
| D1–Dn | Switching Diode | 1N4148 SOD-123 | n |
| J1 | Ribbon Cable Connector (Left) | 14-pin FFC/FPC or IDC | 1 |
| J2 | Ribbon Cable Connector (Right) | 14-pin FFC/FPC or IDC | 1 |
| CABLE1 | Ribbon Cable | 14-pin, length as needed | 1 |
| C1 | Decoupling Capacitor | 100nF 0402 | 1 |

> Update quantities (n) based on your final button layout. Part numbers are suggestions.

## PCB Design

The gamepad is split into two PCBs:
- **Left half** — connected to the host via USB, handles all logic
- **Right half** — communicates to the left half via the 14-pin ribbon cable

Both halves share the same connector footprint on the inner edges.

## Fabrication

Gerber files for both halves are in the `/gerbers` folder.

Recommended specs:
- Layers: 2
- Thickness: 1.6mm
- Surface finish: HASL or ENIG

## Firmware

Compatible with [QMK](https://qmk.fm/) or [KMK](https://github.com/KMKfw/kmk_firmware) with split keyboard support.

## Project Files

| File | Description |
|------|-------------|
| `gamepad.kicad_sch` | Schematic |
| `gamepad.kicad_pcb` | PCB layout |
| `/gerbers` | Fabrication files for both halves |

## License

Open source hardware — feel free to modify and build your own.