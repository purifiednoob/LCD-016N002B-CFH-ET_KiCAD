# Vishay LCD-016N002B-CFH-ET KiCAD Library

A KiCAD symbol and footprint for the Vishay LCD-016N002B-CFH-ET 16×2 character LCD module with RGB LED backlight.

## How This Happened

I ordered an LCD kit from Amazon, went and found the Vishay LCD-016N002B-CFH-ET datasheet, made the footprint and symbol for it, and then the actual module that arrived had 16 pins — not 18. Turns out it was a generic HD44780-compatible display, not the Vishay RGB backlight variant I had designed for.

So this library is for a part I don't own and can't test. Use it at your own risk, and maybe check what's actually in your kit before you spin a board.

## Files

```
LCD_016N002B-CFH-ET/
├── LCD_016N002B-CFH-ET.kicad_mod   # Footprint
├── LCD_016N002B-CFH-ET.kicad_sym   # Schematic symbol
└── LCD_016N002B-CFH-ET.step        # 3D model
```

## Pin Reference

| Pin | Symbol | Function |
|-----|--------|----------|
| 1 | VSS | Ground |
| 2 | VDD | +5V logic supply |
| 3 | V0 | Contrast adjustment |
| 4 | RS | Register select (H: data, L: instruction) |
| 5 | R/W | Read/Write (H: read, L: write) |
| 6 | E | Chip enable |
| 7 | DB0 | Data bus bit 0 |
| 8 | DB1 | Data bus bit 1 |
| 9 | DB2 | Data bus bit 2 |
| 10 | DB3 | Data bus bit 3 |
| 11 | DB4 | Data bus bit 4 |
| 12 | DB5 | Data bus bit 5 |
| 13 | DB6 | Data bus bit 6 |
| 14 | DB7 | Data bus bit 7 |
| 15 | A | LED anode (+) |
| 16 | R | Red cathode (−) |
| 17 | G | Green cathode (−) |
| 18 | B | Blue cathode (−) |

## Installation

### Footprint

1. Clone this repo somewhere permanent on your machine.
2. In KiCAD, open **Preferences → Manage Footprint Libraries**.
3. Click the **+** button to add a new entry.
4. Set the format to **KiCAD** and browse to the `LCD_016N002B-CFH-ET` folder.
5. Give it a nickname (e.g. `Vishay_LCD`) and click OK.

### Symbol

1. In KiCAD, open **Preferences → Manage Symbol Libraries**.
2. Click the **+** button to add a new entry.
3. Browse to `LCD_016N002B-CFH-ET/LCD_016N002B-CFH-ET.kicad_sym`.
4. Give it a nickname (e.g. `Vishay_LCD`) and click OK.
5. The symbol will appear in the symbol chooser under that library name.

## Datasheet

[Vishay LCD-016N002B-CFH-ET — Document 37484](https://www.vishay.com/docs/37484/lcd016n002bcfhet.pdf)
