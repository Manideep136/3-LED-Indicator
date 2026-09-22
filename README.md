# 3-LED Indicator Circuit PCB

A compact **3-LED indicator circuit PCB** designed in **KiCad**. The board is intended as a simple electronics/PCB-design project for demonstrating LED indication, current limiting, connector interfacing, schematic capture, PCB layout, routing, and design-rule checking.

## Project Overview

The PCB contains three independent LED indicator channels. Each LED is paired with a **1 kΩ current-limiting resistor** and the board includes a **1×4, 2.54 mm pitch pin header** for external connections.

### Main Features

- 3 × 3 mm through-hole LEDs
- 3 × 1 kΩ current-limiting resistors
- 1 × 1×4, 2.54 mm horizontal pin header
- Through-hole component assembly
- KiCad schematic and PCB design
- Suitable for basic status/power indication and PCB-design practice

## Bill of Materials

| Item | Reference | Qty | Value | Description | Footprint |
|---|---|---:|---|---|---|
| 1 | D1, D2, D3 | 3 | LED | 3 mm through-hole LED | `LED_THT:LED_D3.0mm` |
| 2 | J1 | 1 | Conn_01x04_Pin | 1×4 pin header, 2.54 mm, horizontal | `Connector_PinHeader_2.54mm:PinHeader_1x04_P2.54mm_Horizontal` |
| 3 | R1, R2, R3 | 3 | 1 kΩ | Through-hole resistor | `Resistor_THT:R_Axial_DIN0204_L3.6mm_D1.6mm_P5.08mm_Horizontal` |

A detailed procurement-ready BOM is included as `3_LED_Circuit_BOM.xlsx` and `3_LED_Circuit_BOM.csv`.

> **Component-selection note:** The supplied source BOM does not specify LED color, resistor power rating, manufacturer part numbers, or suppliers. These fields are intentionally marked as **To be selected / Not specified** rather than inventing part numbers.

## Circuit Operation

Each LED is connected with its own series resistor. The resistor limits LED current and protects the LED from excessive current.

The approximate resistor value is:

```text
R = (VCC - VF) / I_LED
```

For this project, the schematic uses **1 kΩ** resistors. Confirm the actual supply voltage and LED forward voltage before assembly.

## PCB Design Workflow

The PCB was designed using KiCad following this workflow:

1. Schematic capture
2. Component and footprint selection
3. Electrical connections
4. PCB layout
5. Component placement
6. Track routing
7. Design Rule Check (DRC)
8. Gerber generation

## Project Structure

```text
3-LED-Circuit/
├── 3_LED_Circuit.kicad_pro
├── 3_LED_Circuit.kicad_sch
├── 3_LED_Circuit.kicad_pcb
├── 3_LED_Circuit_BOM.xlsx
├── 3_LED_Circuit_BOM.csv
├── gerbers/
│   ├── copper/
│   ├── soldermask/
│   ├── silkscreen/
│   └── drill/
└── README.md
```

## Applications

- LED status indication
- Power indication
- Embedded-system prototypes
- Basic electronics demonstrations
- PCB design practice
- KiCad learning projects

## Tools Used

- **KiCad**
- Schematic Editor
- PCB Editor
- Design Rules Checker (DRC)
- Gerber Viewer

## Project Status

- Schematic: Completed
- PCB Layout: Completed
- Component placement: Completed
- Routing: Completed
- BOM: Prepared
- Gerber generation: Ready

## Author

**Manideep Kolluri**

Electronics / Embedded Systems
