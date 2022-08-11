!!! note

    This guide is specific to the <a href="https://www.sparkfun.com/products/20168">ESP32 Thing Plus (USB-C)</a> board variant. For the variants with the USB micro-B connector, please refer to the <a href="https://learn.sparkfun.com/tutorials/852">ESP32 Thing Plus hookup guide</a>.

<p align="center">
  <a href="https://github.com/sparkfun/SparkFun_Thing_Plus_ESP32_WROOM_C/issues" alt="Issues">
    <img src="https://img.shields.io/github/issues/sparkfun/SparkFun_Thing_Plus_ESP32_WROOM_C.svg" /></a>
  <a href="https://github.com/sparkfun/SparkFun_Thing_Plus_ESP32_WROOM_C/blob/master/LICENSE.md" alt="License">
    <img src="https://img.shields.io/badge/license-CC%20BY--SA%204.0-EF9421.svg" /></a>
  <a href="https://twitter.com/intent/follow?screen_name=sparkfun">
    <img src="https://img.shields.io/twitter/follow/sparkfun.svg?style=social&logo=twitter" alt="follow on Twitter"></a>
</p>

# SparkFun Thing Plus - ESP32 WROOM (USB-C)
The [SparkFun ESP32-WROOM Thing Plus (USB-C)](https://www.sparkfun.com/products/20168) enjoys all the features of our previous [ESP32 Thing Plus (Micro-B) boards](https://learn.sparkfun.com/tutorials/852), but with a few improvements. For this variant, we have included a SD card slot, upgraded to a USB-C connector, integrated a RGB status LED and battery fuel gauge, and provided two voltage regulators; offering separate 700mA current sources for the board and Qwiic connector. The board still retains its standardized 28-pin Feather footprint, 2-pin JST battery connector, and Qwiic connector like our other [Thing Plus boards](https://www.sparkfun.com/thing_plus).

<center>
![SparkFun Thing Plus - ESP32 WROOM (USB-C)](https://cdn.sparkfun.com/r/500-500/assets/parts/1/9/9/6/8/20168Diagonal.jpg)
<br>
### [SparkFun Thing Plus - ESP32 WROOM (USB-C)](https://www.sparkfun.com/products/20168)
(WRL-20168)
</center>

## youtube

The ESP32-WROOM module on the board provides a rich set of peripherals, ranging from capacitive touch sensors, Hall sensors, SD card interface, Ethernet, high-speed SPI, UART, I<sup>2</sup>S, and I<sup>2</sup>C. With [Espressif's ESP32](https://espressif.com/en/products/hardware/esp32/overview) comprehensive development platform and **Bluetooth low-energy** support (i.e BLE, BT4.0, Bluetooth Smart) these boards are jam packed with possibilities!


!!! note
    The CH340C serial-to-UART bridge is used on this board. Therefore, a different driver installation is required from previous versions of the ESP32 Thing Plus.

!!! warning
    <p><b>Not Yet Implemented</b>: The Arduino core for the ESP32 microcontroller are still a work in progress. There are a handful of <a href="https://docs.espressif.com/projects/arduino-esp32/en/latest/libraries.html">peripherals and features</a> that have yet to be implemented, including:</p>
    <p><ul>
        <li>Analog Ouptut (<code>analogWrite([pin], [value])</code>)
            <ul>
                <li>Alternative: <a href="https://espressif-docs.readthedocs-hosted.com/projects/arduino-esp32/en/latest/api/ledc.html">LED Control API</a></li>
            </ul>
        </li>
        <li>Pulse Counter</li>
        <li>SDIO</li>
        <li><s>Timer/</s>Real-Time Clock
            <ul>
                <li>Alternative: <a href="https://github.com/fbiego/ESP32Time"><b>ESP32Time</b> Arduino library</a></li>
            </ul>
        </li>
        <li>TWAI</s>
    </ul></p>
    <p>The peripherals are available (if, also, still in their infancy) in the <a href="https://github.com/espressif/esp-idf">IoT Development Framework</a> for the ESP32. If your application requires any of the features above, consider giving the <a href="https://github.com/espressif/esp-idf">ESP-IDF</a> a try! <i>(Updated:</b> June 2022.)</i></p>