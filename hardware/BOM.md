# Bill of materials

## Board (30.5 × 20 mm)

Order the PCB from `hardware/gerber/`, **or** build it on a piece of perfboard (prototype board): cut it to size, drill the mounting holes and wire it by hand following `hardware/schematic.pdf`. On perfboard, use a through-hole 33 Ω resistor (¼ W) instead of the 0805 SMD part.

| Ref | Qty | Part | Manufacturer part | LCSC | Package |
|---|---:|---|---|---|---|
| R1 | 1 | Resistor 33 Ω | KOA RK73H2ATTD33R0F | [C317229](https://www.lcsc.com/product-detail/C317229.html) | 0805 |
| SW1 | 1 | Mini slide switch ON/OFF, SPDT | Generic, with mounting ears and solder lugs. Not on the PCB: screwed into the base by its mounting ears and wired to J4/J8 (TODO: source link) | — | Panel mount |
| J1–J8 | 8 | Header pin 1×1, 2.54 mm (optional) | — | [C81276](https://www.lcsc.com/product-detail/C81276.html) | THT |

## Tree

| Qty | Part | Specification | Notes |
|---:|---|---|---|
| 11 | Flicker LED | 3 mm, clear lens, yellow, self-flickering | Source: [AliExpress](https://www.aliexpress.com/item/1005007016428728.html), variant 3 mm / yellow. One spare is useful |
| 2 × 60 cm | Tin-plated copper wire | Ø 0.8 mm, bare | Length per wire before bending (1.2 m per tree). One wire is + and one is − |

> **Wire tip:** Use **tin-plated copper wire**. Avoid **silver-plated** wire: the plating tends to flake off at the bends and tarnishes (turns dark) over time.

## Power and enclosure

| Qty | Part | Notes |
|---:|---|---|
| 2 | AAA battery | 3 V |
| 2 | Battery contact, spring plate (−) | 9 × 14 mm, nickel-plated, with solder tab. Source: [AliExpress](https://www.aliexpress.com/item/32884289489.html) |
| 2 | Battery contact, flat plate (+) | 9 × 14 mm, nickel-plated, with solder tab. Same listing |
| — | Short wire link | Connects the two cells in series (− of cell 1 to + of cell 2) |
| 1 | Base (`Housing`) | 3D printed, `mechanics/print-profiles/Base-*.3mf` |
| 1 | Battery holder (`Body1`) + cover (`BatteryCover`) | 3D printed, `mechanics/print-profiles/BatteryHolderCover-*.3mf` |
| 2 | Screw M2 × 8 (or M2 × 12), countersunk, Phillips | Battery cover. DIN 965 / ISO 7046 |
| 2 | Screw | Switch mounting ears. TODO: size |
| — | Screw | PCB. TODO: size and quantity |
| — | Thin stranded wire | From the battery holder to J1/J5 |

## Electrical notes

- Supply: 3 V (2 × AAA)
- All 11 LEDs are in parallel behind one 33 Ω resistor (R1).
- TODO: measured average current, and from that the battery life (≈ battery capacity in mAh ÷ current in mA).
