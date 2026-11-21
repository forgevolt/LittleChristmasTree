# Bill of materials

## PCB (`hardware/gerber/`, 30.5 × 20 mm)

| Ref | Qty | Part | Manufacturer part | LCSC | Package |
|---|---:|---|---|---|---|
| R1 | 1 | Resistor 33 Ω | KOA RK73H2ATTD33R0F | [C317229](https://www.lcsc.com/product-detail/C317229.html) | 0805 |
| SW1 | 1 | Slide switch ON/OFF | Kinghelm KH-SS12F17-G5 | [C5274464](https://www.lcsc.com/product-detail/C5274464.html) | THT |
| J1–J8 | 8 | Header pin 1×1, 2.54 mm (optional) | — | [C81276](https://www.lcsc.com/product-detail/C81276.html) | THT |

## Tree

| Qty | Part | Specification | Notes |
|---:|---|---|---|
| 11 | Flicker LED | 3 mm, clear lens, warm white / amber, self-flickering | TODO: part number / source |
| 2 × 60 cm | Tin-plated copper wire | Ø 0.8 mm, bare | Length per wire before bending (1.2 m per tree). One wire is + and one is − |

> **Wire tip:** Use **tin-plated copper wire**. Avoid **silver-plated** wire: the plating tends to flake off at the bends and tarnishes (turns dark) over time.

## Power and enclosure

| Qty | Part | Notes |
|---:|---|---|
| 2 | AAA battery | 3 V |
| 1 | Base (`Housing`) | 3D printed, `mechanics/print-profiles/Base-*.3mf` |
| 1 | Battery holder (`Body1`) + cover (`BatteryCover`) | 3D printed, `mechanics/print-profiles/BatteryHolderCover-*.3mf` |
| — | Screws | TODO: size and quantity |
| — | Thin stranded wire | From the battery holder to J1/J5 |

## Electrical notes

- Supply: 3 V (2 × AAA)
- All 11 LEDs are in parallel behind one 33 Ω resistor (R1).
- TODO: measured average current, and from that the battery life (≈ battery capacity in mAh ÷ current in mA).
