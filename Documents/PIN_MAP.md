# Pin map: Thing Plus ESP32 WROOM (USB-C) v5.0

U2 = ESP32-WROOM-32E-N16R2. J5 = Thing Plus header (pin numbers are the header symbol's).

| J5 pin | Header label | ESP32 GPIO | Module pin | Net | Notes |
|---|---|---|---|---|---|
| 1 | SDA | IO21 | 33 | ESP_21/TP_SDA | Qwiic J3, fuel gauge U4 |
| 2 | SCL | IO22 | 36 | ESP_22/TP_SCL | Qwiic J3, fuel gauge U4 |
| 3 | GPIO6 | IO14 | 13 | ESP_14/GPIO6 | |
| 4 | GPIO5 | IO32 | 8 | ESP_32/GPIO5 | |
| 5 | GPIO4 | IO15 | 23 | ESP_15/GPIO4 | strap pin, internal pull-up at POR |
| 6 | GPIO3 | IO33 | 9 | ESP_33/GPIO3 | |
| 7 | GPIO2 | IO27 | 12 | ESP_27/GPIO2 | |
| 8 | GPIO1 | IO12 | 14 | ESP_12/GPIO1 | strap pin: no external pull-up |
| 9 | GPIO0 | IO13 | 16 | ESP_13/GPIO0/LED | blue status LED D3 through R4 |
| 13 | FREEBIE | IO4 | 26 | ESP_4/TP_FB | |
| 14 | TX | IO1 (UART0 TX) | 35 | Net-(J5-TX) via R1 1k | **v5.0: was IO17.** Shared with the CH340C RXD |
| 15 | RX | IO17 | 28 | ESP_17/TP_RX | **v5.0: was IO16** |
| 16 | POCI | IO19 | 31 | ESP_19/TP_POCI | microSD DAT0 |
| 17 | PICO | IO23 | 37 | ESP_23/TP_PICO | microSD CMD |
| 18 | SCK | IO18 | 30 | ESP_18/TP_SCK | microSD CLK |
| 19 | A5 | IO35 | 7 | ESP_35/TP_A5 | input only |
| 20 | A4 | IO36 | 4 | ESP_36/TP_A4 | input only |
| 21 | A3 | IO39 | 5 | ESP_39/TP_A3 | input only |
| 22 | A2 | IO34 | 6 | ESP_34/TP_A2 | input only |
| 23 | A1 | IO25 | 10 | ESP_25/TP_A1 | DAC1 |
| 24 | A0 | IO26 | 11 | ESP_26/TP_A0 | DAC2 |
| 10 / 12 / 27 / 25 | VUSB / VBATT / 3.3V / GND | | | | |
| 11 | EN | | | TP_EN | U3 enable (10k pull-up R8) |
| 26 | AREF/NC | | | | not connected |
| 28 | RESET | EN | 3 | ~{RESET} | 10k pull-up R2, button SW4, auto-reset Q2 |

Not on the header:

| GPIO | Module pin | Net | Use |
|---|---|---|---|
| IO0 | 25 | ESP_0/QPWR | BOOT button SW3, Qwiic regulator U5 enable, auto-reset Q2, TP1 |
| IO2 | 24 | ESP_2/RGB_DI | WS2812B D5 data, TP3 |
| IO5 | 29 | ESP_5/SD_CS | microSD CS, TP4 |
| IO3 | 34 | CH340-TX | UART0 RX from the CH340C |
| IO16 | 27 | (no connect) | used by the module's PSRAM |
