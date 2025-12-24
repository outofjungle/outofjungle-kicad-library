# outofjungle-kicad-library

A custom KiCad component library for M5Stack microcontroller modules and supporting components, designed for IoT and embedded systems projects.

## Components

### Symbol Libraries

| Library | Symbol | Description |
|---------|--------|-------------|
| M5Stack | M5Atom | Compact ESP32-based module (9 pins) |
| M5Stack | M5StampS3 | ESP32-S3 stamp module (28 pins) |
| 74xx_custom | 74HCT125D | Quad buffer with 3-state outputs (SOIC-14) |
| Switch_SPST | SparkFun_COM-08720 | SMD tactile pushbutton switch |

### Footprint Libraries

| Library | Footprint | Type | Description |
|---------|-----------|------|-------------|
| M5Stack_SMD | M5StampS3 | SMD | ESP32-S3 stamp module footprint |
| M5Stack_THT | M5Atom | Through-hole | M5Atom module pin header footprint |
| Connector_Custom | BarrelJack_Horizontal_Custom | Through-hole | DC barrel jack power connector |
| Switch_SMD | SparkFun_COM-08720 | SMD | Tactile pushbutton switch |
| Logo | Cat1-Logo_15x8.7mm_SilkScreen | Silkscreen | Decorative logo artwork |

## Installation

### KiCad 7.x / 8.x

1. Clone this repository:
   ```bash
   git clone https://github.com/outofjungle/outofjungle-kicad-library.git
   ```

2. In KiCad, open **Preferences > Manage Symbol Libraries**
   - Click the folder icon to add a library
   - Navigate to the cloned directory and select the `.kicad_sym` files

3. In KiCad, open **Preferences > Manage Footprint Libraries**
   - Click the folder icon to add a library
   - Navigate to the cloned directory and select the `.pretty` folders

### Using Environment Variables (Recommended)

1. In KiCad, open **Preferences > Configure Paths**
2. Add a new path variable:
   - Name: `OUTOFJUNGLE_KICAD_LIB`
   - Path: `/path/to/outofjungle-kicad-library`
3. Reference libraries using `${OUTOFJUNGLE_KICAD_LIB}/LibraryName.kicad_sym`

## Directory Structure

```
outofjungle-kicad-library/
├── M5Stack.kicad_sym           # M5Stack module symbols
├── 74xx_custom.kicad_sym       # Custom 74xx logic symbols
├── Switch_SPST.kicad_sym       # Switch symbols
├── M5Stack_SMD.pretty/         # SMD footprints for M5Stack
├── M5Stack_THT.pretty/         # Through-hole footprints for M5Stack
├── Connector_Custom.pretty/    # Custom connector footprints
├── Switch_SMD.pretty/          # SMD switch footprints
└── Logo.pretty/                # Silkscreen logos and artwork
```

## Component Details

### M5Atom
- **Pins**: G19, G21, G22, G23, G25, G33, 3V3, 5V, GND
- **Footprint**: Through-hole pin headers
- **Note**: Includes antenna keepout zone marking

### M5StampS3
- **Pins**: G0-G15, G39-G46, EN, RXD/G44, TXD/G43, 3V3, 5V, GND (28 total)
- **Footprint**: SMD castellated pads
- **Note**: Includes antenna keepout zone marking

### 74HCT125D
- **Package**: SOIC-14
- **Function**: Quad buffer/line driver with 3-state outputs
- **Pins**: 4 channels (1A/1Y/1OE, 2A/2Y/2OE, 3A/3Y/3OE, 4A/4Y/4OE) + VCC/GND

## License

This library is provided as-is for use in personal and commercial projects.

## Contributing

Contributions are welcome! Please submit pull requests for new components or improvements.
