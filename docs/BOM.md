# Bill of Materials (BOM)

## ESP8266 Custom Development Board

**Total Estimated Cost:** ~$3-5 USD per board (excluding PCB)

---

## Main Components

| Ref | Qty | Component | Value/Type | Package | Description | Supplier Link |
|-----|-----|-----------|------------|---------|-------------|---------------|
| U1 | 1 | ESP8266-12E/F | WiFi Module | SMD Module | ESP8266 WiFi SoC | [AliExpress](https://www.aliexpress.com) |
| U2 | 1 | CH340G | USB-UART | SOIC-16 | USB to Serial converter | [LCSC](https://www.lcsc.com) |
| U3 | 1 | AMS1117-3.3 | 3.3V LDO | SOT-223 | 800mA voltage regulator | [LCSC](https://www.lcsc.com) |

## Passive Components

### Resistors (0805 SMD)
| Ref | Qty | Value | Package | Description |
|-----|-----|-------|---------|-------------|
| R1 | 1 | 10kΩ | 0805 | ESP8266 CH_PD pull-up |
| R2 | 1 | 10kΩ | 0805 | ESP8266 RST pull-up |
| R3 | 1 | 10kΩ | 0805 | GPIO0 pull-up |
| R4 | 1 | 10kΩ | 0805 | GPIO15 pull-down |
| R5 | 1 | 470Ω | 0805 | Power LED current limiting |
| R6 | 1 | 470Ω | 0805 | User LED current limiting |
| R7, R8 | 2 | 12kΩ | 0805 | USB D+/D- pull-up |

### Capacitors
| Ref | Qty | Value | Voltage | Package | Description |
|-----|-----|-------|---------|---------|-------------|
| C1 | 1 | 22µF | 16V | 0805/1206 | Power input filter |
| C2 | 1 | 10µF | 16V | 0805 | AMS1117 output |
| C3, C4 | 2 | 100nF | 50V | 0805 | Decoupling caps |
| C5 | 1 | 22pF | 50V | 0805 | USB crystal load |
| C6 | 1 | 22pF | 50V | 0805 | USB crystal load |

## Semiconductors & Active Parts

| Ref | Qty | Component | Package | Description |
|-----|-----|-----------|---------|-------------|
| D1 | 1 | LED (Red) | 0805 | Power indicator |
| D2 | 1 | LED (Blue) | 0805 | User LED (GPIO2) |
| Q1, Q2 | 2 | BSS138 | SOT-23 | N-Channel MOSFET (auto-reset) |
| Y1 | 1 | 12MHz Crystal | HC-49S | CH340G clock |

## Connectors & Mechanical

| Ref | Qty | Component | Type | Description |
|-----|-----|-----------|------|-------------|
| J1 | 1 | USB Connector | Micro-USB / USB-C | Power & programming |
| J2 | 1 | Pin Header | 2.54mm 1x8 | GPIO breakout (left) |
| J3 | 1 | Pin Header | 2.54mm 1x8 | GPIO breakout (right) |
| SW1 | 1 | Tactile Switch | 6x6mm | Reset button |
| SW2 | 1 | Tactile Switch | 6x6mm | Flash/Boot button |

## PCB Manufacturing

| Parameter | Specification |
|-----------|---------------|
| Board Size | ~50mm x 30mm (TBD) |
| Layers | 2-layer |
| Thickness | 1.6mm |
| Copper Weight | 1 oz |
| Surface Finish | HASL / ENIG |
| Silkscreen | White on green |
| Min Trace/Space | 6/6 mil |

---

## Sourcing Notes

### Recommended Suppliers

1. **LCSC / JLCPCB** (China) - Best for full PCBA service
2. **DigiKey / Mouser** (USA/International) - Reliable, fast shipping
3. **AliExpress** (China) - Cheapest for modules and connectors
4. **Arrow / Newark** (Various) - Good for small quantities

### Cost Breakdown (Approximate)

- ESP8266-12E/F: $1.50
- CH340G: $0.30
- AMS1117-3.3: $0.15
- Passives (all): $0.50
- USB Connector: $0.20
- Headers & Switches: $0.30
- Misc (LEDs, transistors): $0.20
- **Total Components:** ~$3.15

- PCB (5 pcs from JLCPCB): ~$2 ($0.40 per board)
- **Grand Total per Board:** ~$3.55

*Prices as of Jan 2025, vary by supplier and quantity*

---

## Assembly Options

### Option 1: Hand Assembly
- Requires: Soldering iron, solder, flux, tweezers
- Skill level: Intermediate (SMD soldering)
- Time: 30-45 minutes per board

### Option 2: PCBA Service
- Upload BOM + Gerber to JLCPCB/PCBWay
- They assemble most components (add $5-10 per board)
- You solder through-hole parts (headers, buttons)

### Option 3: Reflow Oven/Hot Plate
- Apply solder paste, place components
- Reflow with hot plate or toaster oven
- Time: 15-20 minutes per board

---

## Component Substitutions

**Flexible Components:**
- **CH340G** → CH340C, CP2102, FT232RL (update schematic accordingly)
- **AMS1117-3.3** → XC6206P332MR, LD1117V33 (pin-compatible)
- **BSS138** → 2N7002, AO3400 (similar N-MOSFETs)

**Fixed Components:**
- ESP8266-12E/F must be exact module
- USB connector type can vary (Micro vs USB-C)

---

*BOM will be updated as schematic is finalized*
