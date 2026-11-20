# Design calculations: Thing Plus ESP32 WROOM (USB-C) v5.0

Revision of v4.0 (Eagle). Only the circuits that changed are calculated here; everything else is unchanged from v4.0.

## U2: ESP32-WROOM-32E-N16R2 (IC-29557)

- 16 MB flash, 2 MB PSRAM in the ESP32-D0WDR2-V3 package. Same module outline and land pattern as the ESP32-WROOM-32E used on v4.0, so the footprint and placement don't change.
- The in-package PSRAM uses IO16 (module pin 27). Pin 27 is left unconnected (no-connect flag). Source: Espressif ESP32-WROOM-32E/32UE datasheet, pin definitions, note on variants with embedded PSRAM.
- On v4.0, IO16 was the header RX pin. That function moves (next section).

## Header UART (J5 RX/TX)

| Header pin | v4.0 | v5.0 |
|---|---|---|
| RX | IO16 | IO17 (net `ESP_17/TP_RX`) |
| TX | IO17 | IO1 = UART0 TX, through R1 (net `Net-(J5-TX)`) |

Every other ESP32 GPIO is already broken out, so these are the only two pins available.

### R1 = 1k (RES-14342), series resistor between IO1 and header TX

IO1 also drives the CH340C RXD (USB serial), so header TX carries the same UART0 output. R1 protects IO1 when something else drives the TX pin:

- External 3.3 V push-pull output fighting IO1 low: I = 3.3 V / 1 kOhm = 3.3 mA. That is within the ESP32 GPIO drive rating, so neither side is damaged.
- Edge rate: R1 x (header and cable capacitance, about 20 pF) = 20 ns. A UART bit at 921600 baud is 1.08 us, so the delay is under 2 % of a bit.
- R1 is not in the CH340C path, so USB programming and the auto-reset circuit are unchanged.

The value is the same 1k already used on the board (R3, R4, R34): no new PROD_ID.

## Regulator input range

The schematic note states VIN (U3 input) 3.7 V - 6.0 V:

- max 6.0 V: AP2112K maximum recommended input voltage.
- min 3.7 V: 3.3 V output + 0.4 V maximum dropout at 600 mA.

These values come from the AP2112K datasheet but don't yet have page references; add them before the P7 review.

## Firmware requirements

- FW-1: the module has 2 MB PSRAM. Enable PSRAM in the board definition through a new board entry or menu option. Don't change the defaults of the existing Thing Plus C entry, which still has to build for v4.0 boards in the field.
- FW-2: IO16 is not available. Nothing may configure GPIO16 (for example a default Serial2 RX pin of 16).
- FW-3: the header pins map to RX = GPIO17 and TX = GPIO1. GPIO1 is UART0 TX, shared with the USB serial console. A sketch that uses the header TX pin as a separate UART has to give up UART0 TX.
