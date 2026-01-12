# ESP8266 Custom Development Board

A custom-designed ESP8266 development board with USB programming capability, voltage regulation, and easy GPIO access. Designed in KiCad for learning PCB design and IoT development.

![Board Preview](docs/images/board-preview.png) *(Coming soon)*

## 🎯 Project Goals

- Design a functional ESP8266 development board from scratch
- Learn PCB design workflow in KiCad
- Create a manufacturable, cost-effective IoT development platform
- Build a reusable tool for future projects

## ✨ Features

- **ESP8266-12E/F WiFi Module** - 802.11 b/g/n connectivity
- **USB Programming** - Direct upload via USB with CH340G USB-to-Serial bridge
- **3.3V Power Regulation** - Onboard AMS1117-3.3 regulator
- **Auto-Reset Circuit** - Automatic bootloader entry for seamless programming
- **GPIO Breakout** - All available pins broken out to headers
- **Status LEDs** - Power and user-programmable LED indicators
- **Flash & Reset Buttons** - Manual control for programming mode
- **Compact Design** - Breadboard-friendly form factor

## 📋 Specifications

| Parameter | Value |
|-----------|-------|
| MCU | ESP8266-12E/F |
| Clock Speed | 80/160 MHz |
| Flash Memory | 4MB |
| Operating Voltage | 3.3V |
| Input Voltage | 5V (USB) |
| Digital I/O | 11 GPIO pins |
| Analog Input | 1x 10-bit ADC |
| WiFi | 802.11 b/g/n |
| USB Interface | Micro-USB / USB-C |

## 🛠️ Hardware Design

### Schematic Overview

The board is organized into functional blocks:

1. **Power Supply** - USB 5V to 3.3V regulation with filtering
2. **USB-to-Serial Bridge** - CH340G for USB communication
3. **ESP8266 Module** - Main MCU with supporting components
4. **Programming Interface** - Auto-reset circuit and manual buttons
5. **GPIO Headers** - Pin breakout for prototyping

### Key Components

- **ESP8266-12E/F** - WiFi SoC module
- **CH340G** - USB-to-UART bridge IC
- **AMS1117-3.3** - 800mA LDO voltage regulator
- **Micro-USB/USB-C Connector** - Power and programming interface
- **BSS138** - N-channel MOSFETs for auto-reset circuit
- Supporting passives (resistors, capacitors, LEDs)

### Bill of Materials (BOM)

See [docs/BOM.md](docs/BOM.md) for complete component list with part numbers and suppliers.

**Estimated Cost:** ~$3-5 per board (components only, excluding PCB)

## 📁 Repository Structure

```
├── hardware/
│   ├── schematic/          # KiCad schematic files
│   ├── pcb/                # KiCad PCB layout files
│   └── gerbers/            # Manufacturing files (Gerber + drill)
├── docs/
│   ├── BOM.md              # Bill of Materials
│   ├── assembly-guide.md   # Assembly instructions
│   └── images/             # Photos, renders, diagrams
├── firmware/
│   └── test-sketches/      # Arduino test programs
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- **KiCad 7.0+** - For viewing/editing design files
- **Arduino IDE** or **PlatformIO** - For programming the board

### Manufacturing

1. Download Gerber files from `hardware/gerbers/`
2. Upload to PCB manufacturer (JLCPCB, PCBWay, OSH Park, etc.)
3. Order components from BOM
4. Assemble board (can be done by hand or use PCBA service)

### Programming

1. Install CH340G drivers if needed
2. Connect board via USB
3. Select "Generic ESP8266 Module" in Arduino IDE
4. Upload code!

See [docs/assembly-guide.md](docs/assembly-guide.md) for detailed instructions.

## 📖 Documentation

- **Schematic PDF:** [hardware/schematic/ESP8266-DevBoard-Schematic.pdf](hardware/schematic/)
- **Assembly Guide:** [docs/assembly-guide.md](docs/assembly-guide.md)
- **BOM:** [docs/BOM.md](docs/BOM.md)
- **Design Notes:** [docs/design-notes.md](docs/design-notes.md)

## 🎓 Learning Resources

This project involves:
- PCB design fundamentals
- Power supply design (linear regulation)
- USB communication circuits
- ESP8266 hardware integration
- Manufacturing-ready design practices

## 🔧 Current Status

- [x] Project planning
- [ ] Schematic design
- [ ] PCB layout
- [ ] Design review
- [ ] Prototype order
- [ ] Testing & validation
- [ ] Final revision

## 📝 License

This project is open source under the MIT License. See [LICENSE](LICENSE) for details.

## 🤝 Contributing

Suggestions and improvements are welcome! Feel free to open an issue or submit a pull request.

## 👤 Author

**Naveed Nazir**
- GitHub: [@NaveedNazirAhanger](https://github.com/NaveedNazirAhanger)
- Email: naveednazir901@gmail.com
- LinkedIn: [naveed-nazir-0aa270238](https://www.linkedin.com/in/naveed-nazir-0aa270238)

## 🙏 Acknowledgments

- ESP8266 Community for reference designs
- KiCad development team
- Open source hardware movement

---

*This is a learning project for PCB design and embedded systems development.*
