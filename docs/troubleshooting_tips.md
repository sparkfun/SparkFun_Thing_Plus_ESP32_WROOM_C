# Troubleshooting Tips

<div class="alert alert-info" role="alert">
    <p><span class="glyphicon glyphicon-question-sign" aria-hidden="true"></span> <strong>Not working as expected and need help? </strong></p>
    <p>If you need technical assistance and more information on a product that is not working as you expected, we recommend heading on over to the <a href="https://www.sparkfun.com/technical_assistance">SparkFun Technical Assistance</a> page for some initial troubleshooting.</p>
-> <!-- button(SparkFun Technical Assistance Page, https://www.sparkfun.com/technical_assistance) --> <-
    <p>If you can't find what you need there, you'll need a <a href="https://forum.sparkfun.com/ucp.php?mode=register">Forum Account</a> to search product forums and post questions.<p>
</div>


### Upload Issues
If users are have issues during the uploading process, they can try to manually force the board into the <a href="https://docs.espressif.com/projects/esptool/en/latest/esp32/advanced-topics/boot-mode-selection.html#select-bootloader-mode">serial bootloader</a> with the <kbd>BOOT</kbd> button. Holding down the <kbd>BOOT</kbd> button, while connecting the board to a computer through its USB-C connector or resetting the board will cause the MCU to enter the <a href="https://docs.espressif.com/projects/esptool/en/latest/esp32/advanced-topics/boot-mode-selection.html#manual-bootloader">Firmware Download mode</a> and its serial bootloader. The board will remain in this mode until it power cycles (happens automatically after uploading new firmware) or the <kbd>RST</kbd> button is pressed.

1. Hold the <kbd>BOOT</kbd> button down.
2. Reset the MCU.
    * While unpowered, connect the board to a computer with through the USB-C connection.
    * While powered, press the <kbd>RST</kbd> button.
3. Release the <kbd>BOOT</kbd> button.
4. After programming is completed, reboot the MCU.
    * Press the <kbd>RST</kbd> button.
    * Power cycle the board. 

[![Boot Button](https://cdn.sparkfun.com/r/350-350/assets/learn_tutorials/2/3/5/3/button_boot.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/2/3/5/3/button_boot.jpg)<br>
*<kbd>BOOT</kbd> button on the ESP32-WROOM Thing Plus. (Click to enlarge)*


### COM Port Not Shown
If the board doesn&apos;t appear on a COM port, double check the correct driver has been installed. Unlike previous versions of the ESP32 Thing Plus, this variant requires the [CH340 driver](https://www.sparkfun.com/ch340) to be installed. *For more information, check out our [How to Install CH340 Drivers Tutorial](https://www.sparkfun.com/ch340).*

<!-- tutorial_big(908) -->

Users can also check their USB cable; some cables are power only. Try testing the cable with a smart phone or tablet to see if it appears as a device on the computer. If the phone/tablet doesn't appear, then the USB cable is power only.

### `Serial` Stream Difficulties
We have noticed that with the ESP32 Arduino core, `Serial.available()` does not operate instantaneously. This is due to an interrupt triggered by the UART, to empty the FIFO when the **`RX`** pin is inactive for two byte periods:

* At 9600 baud, `hwAvailable` takes [`number of bytes received` + 2] x 1 ms = **11 ms** before the UART indicates that data was received from: `\r\nERROR\r\n`.
* At 115200 baud, `hwAvailable` takes [`number of bytes received` +2] x .087 ms = **~1 ms** before the UART indicates that data was received from: `\r\nERROR\r\n`.

*For more information, please refer to this <a href="https://gitter.im/espressif/arduino-esp32?at=5e25d6370a1cf54144909c85">chatroom discussion</a>.*


### &micro;SD Card
Make sure that the &micro;SD card is compatible with the Arduino library being used for it.   For example, the default [SD Arduino library](https://www.arduino.cc/reference/en/libraries/sd/) is only compatible with `FAT16` or `FAT32` file systems; therefore, the card capacity is limited to **16GB** or **32GB** and smaller. Another consideration is that the library was also written to only handle [short 8.3 names for files](https://en.wikipedia.org/wiki/8.3_filename).


### Qwiic Connector Power
For users having issues with the power to their Qwiic devices, don't forget that <code>GPIO 0</code> controls the power output from the XC6222 LDO regulator to the Qwiic connector. Users must toggle <code>GPIO 0</code> high to enable power for the Qwiic connector. In order to conserve battery power or in low power applications, users will can toggle <code>GPIO 0</code> low, to disable the power to the Qwiic connector.

<div class="alert alert-info"><b>Note:</b> <code>GPIO 0</code> is also connected to the <kbd>BOOT</kbd> button. Therefore, pressing the <kbd>BOOT</kbd> button will momentarily disable power to the Qwiic connector.</div>


### Current Consumption
For ultra low power projects, these are the current consumption of the individual components, as specified in their datasheet:

<div class="row">
    <div class="col-md-6">
        <ul>
            <li><a href="https://cdn.sparkfun.com/assets/0/3/b/e/f/XC6222.pdf">XC6222 LDO Regulator</a>:
                <ul>
                    <li>Supply Current: 100 - 220 &micro;A</li>
                </ul>
            </li>
            <li><a href="https://cdn.sparkfun.com/assets/1/c/4/2/3/MCP73831.pdf">MCP73831 Charger Controller</a>:
                <ul>
                    <li>Supply Current:
                        <ul>
                            <li>510 - 1500 &micro;A (Charging)</li>
                            <li>53 - 200 &micro;A (Charge complete; no battery)</li>
                        </ul>
                    </li>
                    <li>Constant-Voltage Mode
                        <ul>
                            <li>Line/Load regulation: 100 - 50 mA</li>
                        </ul>
                    </li>
                    <li>Fast Charge Constant-Current Mode
                        <ul>
                            <li>Fast Charge Current: 450 - 550 mA</li>
                        </ul>
                    </li>
                    <li>Battery Detection Current: 6 &micro;A</li>
                    <li>Leakage Current: up to 2&micro;A</li>
                    <li>Status Indicator:
                        <ul>
                            <li>Sink Current: 25 mA</li>
                        </ul>
                    </li>
                </ul>
            </li>
            <li><a href="https://cdn.sparkfun.com/assets/b/b/2/c/b/MAX17048.pdf">MAX17048 Fuel Gauge</a>:
                <ul>
                    <li>Supply Current:
                        <ul>
                            <li>Sleep: 0.5 - 2 &micro;A</li>
                            <li>Hibernate: 3 - 5 &micro;A</li>
                            <li>Active: 23 - 40 &micro;A</li>
                        </ul>
                    </li>
                    <li>I<sup>2</sup>C: 0.2 - 0.4 &micro;A</li>
                </ul>
            </li>
        </ul>
    </div>
    <div class="col-md-6">
        <ul>
            <li><a href="https://cdn.sparkfun.com/assets/5/0/a/8/5/CH340DS1.PDF">CH340C Serial-to-UART Bridge</a>:
                <ul>
                    <li>Supply Current: 4 - 12 mA
                        <ul>
                            <li>USB Suspended: 0.04 - 0.15 mA</li>
                        </ul>
                    </li>
                </ul>
            </li>
            <li><a href="https://cdn.sparkfun.com/assets/a/1/8/4/4/esp32_soc_datasheet_en.pdf">ESP32 SoC</a>:
                <ul>
                    <li>Rec Supply current: 500 mA</li>
                    <li>Active: 95 - 240 mA
                        <ul>
                            <li>w/ RF Transceiver:
                                <ul>
                                    <li>TX: up to 380 mA</li>
                                    <li>RX: Up to 118 mA</li>
                                </ul>
                            </li>
                        </ul>
                    </li>
                    <li>Sleep Modes:
                        <ul>
                            <li>Modem: 20 - 68 mA</li>
                            <li>Light: .8 mA</li>
                            <li>Deep: 10 - 150 &micro;A</li>
                            <li>Hibernation: 5 &micro;A</li>
                            <li>Off: 1&micro;A</li>
                        </ul>
                    </li>
                </ul>
            </li>
            <li><a href="https://cdn.sparkfun.com/assets/7/0/3/c/9/WS2812C-2020.pdf">WS2812 RGB LED</a>:
                <ul>
                    <li>Supply Current: 1&micro;A (@5V)</li>
                    <li>LEDs: 5mA each (@5V)</li>
                </ul>
            </li>
        </ul>
    </div>
</div>