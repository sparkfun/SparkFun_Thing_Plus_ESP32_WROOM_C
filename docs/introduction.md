<div class="well"><b>Note:</b> This guide is specific to the <a href="https://www.sparkfun.com/products/20168">ESP32 Thing Plus (USB-C)</a> board variant. For the variants with the USB micro-B connector, please refer to the <a href="https://learn.sparkfun.com/tutorials/852">ESP32 Thing Plus hookup guide</a>.</div>

# Introduction

The [SparkFun ESP32-WROOM Thing Plus (USB-C)](https://www.sparkfun.com/products/20168) enjoys all the features of our previous [ESP32 Thing Plus (Micro-B) boards](https://learn.sparkfun.com/tutorials/852), but with a few improvements. For this variant, we have included a SD card slot, upgraded to a USB-C connector, integrated a RGB status LED and battery fuel gauge, and provided two voltage regulators; offering separate 700mA current sources for the board and Qwiic connector. The board still retains its standardized 28-pin Feather footprint, 2-pin JST battery connector, and Qwiic connector like our other [Thing Plus boards](https://www.sparkfun.com/thing_plus).


-> ![SparkFun Thing Plus - ESP32 WROOM (USB-C)](https://cdn.sparkfun.com/r/500-500/assets/parts/1/7/2/3/9/20168-Thing_Plus_C_-_ESP32_WROOM-01.jpg)
<br>
SparkFun Thing Plus - ESP32 WROOM (USB-C) (WRL-20168) <-

<!-- youtube() -->

The ESP32-WROOM module on the board provides a rich set of peripherals, ranging from capacitive touch sensors, Hall sensors, SD card interface, Ethernet, high-speed SPI, UART, I<sup>2</sup>S, and I<sup>2</sup>C. With [Espressif's ESP32](https://espressif.com/en/products/hardware/esp32/overview) comprehensive development platform and **Bluetooth low-energy** support (i.e BLE, BT4.0, Bluetooth Smart) these boards are jam packed with possibilities!


<div class="alert alert-info"><b>Note:</b> The CH340C serial-to-UART bridge is used on this board. Therefore, a different driver installation is required from previous versions of the ESP32 Thing Plus.</div>

<div class="alert alert-warning"><p><b>Not Yet Implemented</b>: The Arduino core for the ESP32 microcontroller are still a work in progress. There are a handful of <a href="https://docs.espressif.com/projects/arduino-esp32/en/latest/libraries.html">peripherals and features</a> that have yet to be implemented, including:</p>

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

</div>

### Required Materials
To get started, users will need a few items. Now some users may have a few of these items, feel free to modify your cart accordingly.

* [SparkFun Thing Plus - ESP32 WROOM (USB-C)](https://www.sparkfun.com/products/20168)
* [USB 3.1 Cable A to C - 3 Foot](https://www.sparkfun.com/products/14743) - The USB interface serves two purposes: it powers the board and allows users to upload programs. (*\*If your computer doesn't have a USB-A slot, then choose an appropriate cable or adapter.*)
* Computer with the an operating system (OS) that is compatible with all the software installation requirements.

<!-- products_by_id(14743, 20168) -->



<!-- ADDITIONAL MATERIALS -->
<!-- Buttons -->

<p style="text-align:center;">
    <a class="collapsed btn btn-default" role="button" data-toggle="collapse" data-parent="#Introduction" href="#Headers" aria-expanded="false" aria-controls="Headers"><b>Headers</b></a>
    <a class="collapsed btn btn-default" role="button" data-toggle="collapse" data-parent="#Introduction" href="#LiPo" aria-expanded="true" aria-controls="LiPo"><b>Batteries</b></a>
    <a class="collapsed btn btn-default" role="button" data-toggle="collapse" data-parent="#Introduction" href="#Jumper_Materials" aria-expanded="false" aria-controls="Jumper_Materials"><b>Jumper Modification</b></a>
    <a class="collapsed btn btn-default" role="button" data-toggle="collapse" data-parent="#Introduction" href="#JTAG" aria-expanded="false" aria-controls="JTAG"><b>JTAG Functionality</b></a>
</p>

<center><i><b>Click the buttons</b> above to toggle the <b>additional materials</b> based on the options you<br>
wish to use. Feel free to modify the items in your cart to fit your needs.</i></center>


<!-- Content Separation -->
<div class="panel-group" id="Introduction" role="tablist" aria-multiselectable="true"><div class="panel panel-default"><div id="LiPo" class="panel-collapse collapse" role="tabpanel"><div class="panel-body">
<br>
<H4>Li-Po Battery</H4>
<p>For mobile applications, users will want to pick up a <a href="https://www.sparkfun.com/categories/54">single-cell LiPo battery</a> from our catalog. Below, are a few available options:</p>

<!-- products_by_id(13813, 13851, 13853, 13855) -->
</div></div></div>


<!-- Content Separation -->
<div class="panel panel-default"><div id="Jumper_Materials" class="panel-collapse collapse" role="tabpanel"><div class="panel-body">
<br>
<H4>Jumper Modification</H4>
<p>To modify the jumpers, users will need <a href="https://www.sparkfun.com/categories/49">soldering equipment</a> and/or a <a href="https://www.sparkfun.com/categories/379">knife</a>.</p>

<!-- products_by_id(09325, 14228, 14579, 09200) -->

<div class="alert alert-info">
<p>New to soldering? Check out our <a href="https://learn.sparkfun.com/tutorials/664">Jumper Pads and PCB Traces Tutorial</a> for a quick introduction!</p>
<div class="row">
    <div class="col-md-3"></div>
    <div class="col-md-6">
        <!-- tutorial_big(664) -->
    </div>
    <div class="col-md-3"></div>
</div>
</div>
</div></div></div>


<!-- Content Separation -->
<div class="panel panel-default"><div id="Headers" class="panel-collapse collapse" role="tabpanel"><div class="panel-body">
<br>
<H4>Headers & Accessories</H4>
<p><a href="https://www.sparkfun.com/categories/381">Headers</a> are great for development purposes, letting users swap parts with just a set of jumper wires. If you would like to add headers to your board, check out some of the options for the Thing Plus or Feather form factor boards below. For a full selection of our available <a href="https://www.sparkfun.com/categories/381"><b>Headers</b></a> or <a href="https://www.sparkfun.com/categories/49"><b>Soldering Tools</b></a>, click on the associated links.</p>

<!-- products_by_id(116, 11895, 14321, 15187, 14681) -->

<div class="alert alert-info">
<p>New to soldering? Check out our <a href="https://learn.sparkfun.com/tutorials/5">Through-Hole Soldering Tutorial</a> for a quick introduction!</p>
<div class="row">
    <div class="col-md-3"></div>
    <div class="col-md-6">
        <!-- tutorial_big(5) -->
    </div>
    <div class="col-md-3"></div>
</div>
</div>

</div></div></div>


<!-- Content Separation -->
<div class="panel panel-default"><div id="JTAG" class="panel-collapse collapse" role="tabpanel"><div class="panel-body">
<br>
<H4>JTAG Functionality</H4>
<p>Users interested in JTAG applications <i>(i.e. programming and debugging the ESP32)</i> will need an <a href="https://www.sparkfun.com/categories/26">JTAG Programmer</a> and need to solder on a <a href="https://www.sparkfun.com/products/15362">JTAG header</a>. We recommend these programmers from our catalog:</p>

<!-- products_by_id(15345, 15346, 15347, 15362, 18421) -->
</div></div></div>


</div>



### Suggested Reading

As a more professionally oriented product, we will skip over the more fundamental tutorials (i.e. [**Ohm's Law**](https://learn.sparkfun.com/tutorials/voltage-current-resistance-and-ohms-law) and [**What is Electricity?**](https://learn.sparkfun.com/tutorials/what-is-electricity)). However, below are a few tutorials that may help users familiarize themselves with various aspects of the board.

<!-- tutorials_by_id(5, 8, 16, 51, 61, 62, 82, 89, 664, 852, 908, 1265) -->

<center>
<div align="center">
    <div style="top:5px;left:5px;background-color:Gray;position:relative">
        <div style="top:-5px;left:-5px;background-color:#ffffff;position:relative;border:1px solid black;">
            <a href="https://www.sparkfun.com/qwiic"><img src="https://cdn.sparkfun.com/assets/custom_pages/2/7/2/qwiic-logo.png" alt="Qwiic Connect System" title="Qwiic Connect System"></a>
        </div>
    </div>
</div>
</center>

One of the new, advanced features of the board is that it takes advantage of the [Qwiic connect system](https://www.sparkfun.com/qwiic). We recommend familiarizing yourself with the **Logic Levels** and **I<sup>2</sup>C** tutorials.  Click on the banner above to learn more about [Qwiic products](https://www.sparkfun.com/qwiic).

<!-- youtube(https://youtu.be/x0RDEHqFIF8) -->