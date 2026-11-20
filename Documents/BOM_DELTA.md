# BOM delta: Thing Plus ESP32 WROOM (USB-C) v4.0 -> v5.0

## Revision changes

| Ref | v4.0 | v5.0 | Change |
|---|---|---|---|
| U2 | IC-15676, ESP32 WROOM module (Eagle `ESP-WROOM-32D-NARROW` land) | **IC-29557**, ESP32-WROOM-32E-N16R2 (16 MB flash, 2 MB PSRAM) | changed |
| R1 | - | **RES-14342**, 1k 0402, back side | added (header TX series resistor) |

## Conversion changes (same value and package, current library PROD_ID)

| Ref | v4.0 PROD_ID | v5.0 PROD_ID | Value |
|---|---|---|---|
| C3, C7, C10 | CAP-12417 | CAP-14969 | 1.0uF 0402 16V |
| C2, C5 | CAP-14993 | CAP-25565 | 0.1uF 0402 16V |
| C15 | CAP-12416 | CAP-25565 | 0.1uF 0402 16V |
| C6 | CAP-14240 | CAP-24988 | 4.7uF 0402 6.3V |
| R2, R7, R8, R17, R18 | RES-14241 | RES-25567 | 10k 0402 |
| D12 | DIO-00819 | DIO-17976 | Red LED 0603 |

## Reference and BOM-flag changes

- S3, S4 renamed SW3, SW4 (KiCad switch prefix). Same parts (SWCH-15606).
- Off the BOM (copper only, nothing purchased): fiducials FD1-FD4, standoffs H1-H2, jumpers JP1-JP3, test points TP1-TP4 and the J5 header footprint. The Eagle BOM listed them with no PROD_ID.

Every other line is unchanged.
