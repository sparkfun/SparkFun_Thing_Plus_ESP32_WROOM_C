# Hardware Assembly

### USB Programming
The USB connection is utilized for programming and serial communication. Users only need to plug their ESP32-WROOM Thing Plus into a computer using a USB-C cable.

[![ESP32-WROOM Thing Plus USB connection](https://cdn.sparkfun.com/r/400-400/assets/learn_tutorials/2/3/5/3/assembly_usb.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/2/3/5/3/assembly_usb.jpg)<br>
*The ESP32-WROOM Thing Plus with USB-C cable attached. (Click to enlarge)*


### Battery
For remote IoT applications, a Li-Po battery can be connected. Additionally, users may be interested in utilizing a [solar panel](https://www.sparkfun.com/products/16835) and [USB-C cable](https://www.sparkfun.com/products/14743) to recharge their battery.

<div class="row">
    <div class="col-md-6">
    <center>
        <a href="https://cdn.sparkfun.com/assets/learn_tutorials/2/3/5/3/assembly_batt.jpg"><img alt="Battery connected to the ESP32-WROOM Thing Plus" src="https://cdn.sparkfun.com/r/350-350/assets/learn_tutorials/2/3/5/3/assembly_batt.jpg"></a>
        <br>
        <i>The ESP32-WROOM Thing Plus with a battery connected. (Click to enlarge)</i>
    </center>
    </div>
    <div class="col-md-3">
        <!-- product_big(16835) -->
    </div>
    <div class="col-md-3">
        <!-- product_big(14743) -->
    </div>
</div>

<div class="alert alert-info"><p><b>Note: <span style="color:red">DO <u>NOT</u></span></b> remove batteries by pulling on their wires. Instead, it is recommended that pair of dikes (i.e. diagonal wire cutters), pliers, or tweezers be used to pull on the JST connector housing, to avoid damaging the battery wiring.</p>

<p><center>
<a href="https://cdn.sparkfun.com/assets/learn_tutorials/2/3/5/3/assembly_batt_removal.jpg"><img alt="Disconnect battery w/ dikes" src="https://cdn.sparkfun.com/r/400-400/assets/learn_tutorials/2/3/5/3/assembly_batt_removal.jpg"></a>
<br>
<i>Using a pair of dikes to disconnect a battery. (Click to enlarge)</i>
</center></p>
</div>


### Headers
The pins for the ESP32-WROOM Thing Plus are broken out to 0.1"-spaced pins on the outer edges of the board. When selecting headers, be sure you are aware of the functionality you need. If you have never soldered before or need a quick refresher, check out our [How to Solder: Through-Hole Soldering](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering) guide.

[![Soldering headers](https://cdn.sparkfun.com/r/400-400/assets/learn_tutorials/2/3/5/3/assembly_headers.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/2/3/5/3/assembly_headers.jpg)<br>
*Soldering headers to the ESP32-WROOM Thing Plus. (Click to enlarge)*

The [Feather Stackable Header Kit](https://www.sparkfun.com/products/15187) is a great option as it allows users to stack shields (*w/ Feather footprint*) or it can be placed on the a breadboard; while, the pins are still accessible from the female/male headers.


### &micro;SD Card Slot
The ESP32-WROOM Thing Plus (USB-C) includes a &micro;SD card slot on the back of the board. The card holder functions through a push/pull operation. *(The card slot doesn&apos;t include a spring retention mechanism; cards are held in place through friction.)*

[![Inseting an SD card](https://cdn.sparkfun.com/r/400-400/assets/learn_tutorials/2/3/5/3/assembly_sd_card.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/2/3/5/3/assembly_sd_card.jpg)<br>
*Users can slide-in or pull-out a &micro;SD card from the card holder. (Click to enlarge)*


### Qwiic Devices
The Qwiic system allows users to effortlessly prototype with a Qwiic compatible I<sup>2</sup>C device without soldering. Users can attach any Qwiic compatible [sensor or board](https://www.sparkfun.com/qwiic#sensors), with just a [Qwiic cable](https://www.sparkfun.com/products/15081). (*\*The example below, is for demonstration purposes and is not pertinent to the board functionality or this tutorial.*)

[![Qwiic devices connected to ESP32-WROOM Thing Plus](https://cdn.sparkfun.com/r/400-400/assets/learn_tutorials/2/3/5/3/assembly_qwiic.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/2/3/5/3/assembly_qwiic.jpg)<br>
*The [BME688 environmental](https://www.sparkfun.com/products/19096) and [VL53L1X distance](https://www.sparkfun.com/products/14722) Qwiic sensor boards connected to the ESP32-WROOM Thing Plus. (Click to enlarge)*