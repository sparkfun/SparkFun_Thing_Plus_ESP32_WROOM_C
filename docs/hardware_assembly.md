## USB Programming
The USB connection is utilized for programming and serial communication. Users only need to plug their ESP32-WROOM Thing Plus into a computer using a USB-C cable.

<center>
[![ESP32-WROOM Thing Plus USB connection](./img/hookup_guide/assembly_usb.jpg){ width="400" }](./img/hookup_guide/assembly_usb.jpg)<br>
*The ESP32-WROOM Thing Plus with USB-C cable attached. (Click to enlarge)*
</center>


## Battery
For remote IoT applications, a Li-Po battery can be connected. Additionally, users may be interested in utilizing a [solar panel](https://www.sparkfun.com/products/16835) and [USB-C cable](https://www.sparkfun.com/products/14743) to recharge their battery.

<table style="border-style:none">
    <tr>
        <td align="center" width="50%">
            <a href="https://github.com/sparkfun/SparkFun_Thing_Plus_ESP32_WROOM_C/docs/img/hookup_guide/assembly_batt.jpg"><img alt="Battery connected to the ESP32-WROOM Thing Plus" src="https://github.com/sparkfun/SparkFun_Thing_Plus_ESP32_WROOM_C/docs/img/hookup_guide/assembly_batt.jpg"></a>
            <br>
            <i>The ESP32-WROOM Thing Plus with a battery connected. (Click to enlarge)</i>
        </td>
        <td align="center">
            <a class="thumb" href="https://www.sparkfun.com/products/16835">
                <center><img src="https://cdn.sparkfun.com/r/500-500/assets/parts/1/5/7/5/6/16835-Solar_Panel_Charger_-_10W-01.jpg" alt="Solar Panel Charger - 10W" height="140">
                </center>
                <h3 class="title">Solar Panel Charger - 10W</h3>
            </a>
            TOL-16835
        </td>
        <td align="center">
            <a class="thumb" href="https://www.sparkfun.com/products/14743">
                <center><img src="https://cdn.sparkfun.com/r/500-500/assets/parts/1/2/9/7/2/14743-USB_3.1_Cable_A_to_C_-_3_Foot-01.jpg" alt="USB 3.1 Cable A to C - 3 Foot" height="140">
                </center>
                <h3 class="title">USB 3.1 Cable A to C - 3 Foot</h3>
            </a>
            TOL-14743
        </td>
    </tr>
</table>

!!! note
    <p><b><span style="color:red">DO <u>NOT</u></span></b> remove batteries by pulling on their wires. Instead, it is recommended that pair of dikes (i.e. diagonal wire cutters), pliers, or tweezers be used to pull on the JST connector housing, to avoid damaging the battery wiring.</p>
    <p><center>
        <a href="https://github.com/sparkfun/SparkFun_Thing_Plus_ESP32_WROOM_C/docs/img/hookup_guide/assembly_batt_removal.jpg"><img alt="Disconnect battery w/ dikes" src="https://github.com/sparkfun/SparkFun_Thing_Plus_ESP32_WROOM_C/docs/img/hookup_guide/assembly_batt_removal.jpg"></a>
        <br>
        <i>Using a pair of dikes to disconnect a battery. (Click to enlarge)</i>
    </center></p>


## Headers
The pins for the ESP32-WROOM Thing Plus are broken out to 0.1"-spaced pins on the outer edges of the board. When selecting headers, be sure you are aware of the functionality you need. If you have never soldered before or need a quick refresher, check out our [How to Solder: Through-Hole Soldering](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering) guide.

<center>
[![Soldering headers](./img/hookup_guide/assembly_headers.jpg){ width="400" }](./img/hookup_guide/assembly_headers.jpg)<br>
*Soldering headers to the ESP32-WROOM Thing Plus. (Click to enlarge)*
</center>

The [Feather Stackable Header Kit](https://www.sparkfun.com/products/15187) is a great option as it allows users to stack shields (*w/ Feather footprint*) or it can be placed on a breadboard; while the pins are still accessible from the female/male headers.


### &micro;SD Card Slot
The ESP32-WROOM Thing Plus (USB-C) includes an &micro;SD card slot on the back of the board. The cardholder functions through a push/pull operation. *(The card slot doesn't include a spring retention mechanism; cards are held in place through friction.)*

<center>
[![Inseting an SD card](./img/hookup_guide/assembly_sd_card.jpg){ width="400" }](./img/hookup_guide/assembly_sd_card.jpg)<br>
*Users can slide-in or pull-out a &micro;SD card from the card holder. (Click to enlarge)*
</center>


### Qwiic Devices
The Qwiic system allows users to effortlessly prototype with a Qwiic compatible I<sup>2</sup>C device without soldering. Users can attach any Qwiic compatible [sensor or board](https://www.sparkfun.com/qwiic#sensors), with just a [Qwiic cable](https://www.sparkfun.com/products/15081). (*\*The example below, is for demonstration purposes and is not pertinent to the board functionality or this tutorial.*)

<center>
[![Qwiic devices connected to ESP32-WROOM Thing Plus](./img/hookup_guide/assembly_qwiic.jpg){ width="400" }](./img/hookup_guide/assembly_qwiic.jpg)<br>
*The [BME688 environmental](https://www.sparkfun.com/products/19096) and [VL53L1X distance](https://www.sparkfun.com/products/14722) Qwiic sensor boards connected to the ESP32-WROOM Thing Plus. (Click to enlarge)*
</center>