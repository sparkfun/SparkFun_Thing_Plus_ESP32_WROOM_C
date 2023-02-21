!!! info

    This guide is specific to the <a href="https://www.sparkfun.com/products/20168">ESP32 Thing Plus (USB-C)</a> board variant. For the variants with the USB micro-B connector, please refer to the <a href="https://learn.sparkfun.com/tutorials/852">ESP32 Thing Plus hookup guide</a>.

<p class="pdf" align="center">
  <a href="https://github.com/sparkfun/SparkFun_Thing_Plus_ESP32_WROOM_C/issues" alt="Issues">
    <img src="https://img.shields.io/github/issues/sparkfun/SparkFun_Thing_Plus_ESP32_WROOM_C.svg" /></a>
  <a href="https://github.com/sparkfun/SparkFun_Thing_Plus_ESP32_WROOM_C/blob/master/LICENSE.md" alt="License">
    <img src="https://img.shields.io/badge/license-CC%20BY--SA%204.0-EF9421.svg" /></a>
  <a href="https://twitter.com/intent/follow?screen_name=sparkfun">
    <img src="https://img.shields.io/twitter/follow/sparkfun.svg?style=social&logo=twitter" alt="follow on Twitter"></a>
</p>

# SparkFun Thing Plus - ESP32 WROOM (USB-C)

<div class="grid cards desc" markdown>

-   [**SKU:** DEV-20168](https://www.sparkfun.com/products/20168)
	
	---
	
	<figure markdown>
	[![SparkFun Thing Plus - ESP32 WROOM (USB-C)](https://cdn.sparkfun.com/r/500-500/assets/parts/1/9/9/6/8/20168Diagonal.jpg)](https://cdn.sparkfun.com/assets/parts/1/9/9/6/8/20168Diagonal.jpg)
	</figure>

    <center>
    <section class="video">
	<iframe src="https://www.youtube.com/embed/g2MgO2fjqsw" title="Product Showcase: SparkFun Thing Plus ESP32 WROOM USB-C" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </section>
	</center>


-	The [SparkFun ESP32-WROOM Thing Plus (USB-C)](https://www.sparkfun.com/products/20168) enjoys all the features of our previous [ESP32 Thing Plus (Micro-B) boards](https://learn.sparkfun.com/tutorials/852), but with a few improvements. For this variant, we have included an SD card slot, upgraded to a USB-C connector, integrated an RGB status LED and battery fuel gauge, and provided two voltage regulators; offering separate 700mA current sources for the board and Qwiic connector. The board still retains its standardized 28-pin Feather footprint, 2-pin JST battery connector, and Qwiic connector like our other [Thing Plus boards](https://www.sparkfun.com/thing_plus).

    The ESP32-WROOM module on the board provides a rich set of peripherals, ranging from capacitive touch sensors, Hall sensors, SD card interface, Ethernet, high-speed SPI, UART, I<sup>2</sup>S, and I<sup>2</sup>C. With [Espressif's ESP32](https://espressif.com/en/products/hardware/esp32/overview) comprehensive development platform and **Bluetooth low-energy** support (i.e BLE, BT4.0, Bluetooth Smart) these boards are jam-packed with possibilities!

	<center>
	[Purchase from SparkFun :fontawesome-solid-cart-plus:](https://www.sparkfun.com/products/20168){ .md-button .md-button--primary }
	</center>

</div>

!!! tip
    The CH340C serial-to-UART bridge is used on this board. Therefore, a different driver installation is required from previous versions of the ESP32 Thing Plus.

!!! warning
    <p><b>Not Yet Implemented</b>: The Arduino core for the ESP32 microcontroller is still a work in progress. There are a handful of <a href="https://docs.espressif.com/projects/arduino-esp32/en/latest/libraries.html">peripherals and features</a> that have yet to be implemented, including:</p>
    <p><ul>
        <li>Analog Output (<code>analogWrite([pin], [value])</code>)
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

## Required Materials
To get started, users will need a few items. Now some users may have a few of these items, feel free to modify your cart accordingly.

* [SparkFun Thing Plus - ESP32 WROOM (USB-C)](https://www.sparkfun.com/products/20168)
* [USB 3.1 Cable A to C - 3 Foot](https://www.sparkfun.com/products/14743) - The USB interface serves two purposes: it powers the board and allows users to upload programs. (*\*If your computer doesn't have a USB-A slot, then choose an appropriate cable or adapter.*)
* Computer with an operating system (OS) that is compatible with all the software installation requirements.

<table class="pdf">
    <tr>
        <td>
            <a href="https://www.sparkfun.com/products/14743">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/2/9/7/2/14743-USB_3.1_Cable_A_to_C_-_3_Foot-01.jpg" alt="USB 3.1 Cable A to C - 3 Foot" height="140"></center>
                <h3 class="title">USB 3.1 Cable A to C - 3 Foot</h3>
            </a>
            CAB-14743
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/20168">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/9/9/6/8/20168Diagonal.jpg" alt="SparkFun Thing Plus - ESP32 WROOM (USB-C)" height="140">
                </center>
                <h3 class="title">SparkFun Thing Plus - ESP32 WROOM (USB-C)</h3>
            </a>
            WRL-20168
        </td>
</table>



### Headers & Accessories
<p><a href="https://www.sparkfun.com/categories/381">Headers</a> are great for development purposes, letting users swap parts with just a set of jumper wires. If you would like to add headers to your board, check out some of the options for the Thing Plus or Feather form factor boards below. For a full selection of our available <a href="https://www.sparkfun.com/categories/381"><b>Headers</b></a> or <a href="https://www.sparkfun.com/categories/49"><b>Soldering Tools</b></a>, click on the associated links.</p>

<table class="pdf">
    <tr>
        <td>
            <a href="https://www.sparkfun.com/products/116">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/0/6/00116-02-L.jpg" alt="Break Away Headers - Straight" height="140"></center>
                <h3 class="title">Break Away Headers - Straight</h3>
            </a>
            PRT-00116
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/14681">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/2/8/8/3/14681-SparkFun_Beginner_Tool_Kit.jpg" alt="SparkFun Beginner Tool Kit" height="140">
                </center>
                <h3 class="title">SparkFun Beginner Tool Kit</h3>
            </a>
            TOL-14681
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/15187">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/3/6/0/4/15187-Feather_Stackable_Header_Kit-01.jpg" alt="Feather Stackable Header Kit" height="140">
                </center>
                <h3 class="title">Feather Stackable Header Kit</h3>
            </a>
            PRT-15187
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/14321">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/0/0/3/14321-02.jpg" alt="Photon Header - 12 Pin Female" height="140">
                </center>
                <h3 class="title">Photon Header - 12 Pin Female</h3>
            </a>
            PRT-14321 
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/11895">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/8/9/8/11895-01.jpg" alt="Header - 8-pin Female (PTH, 0.1&quot;)" height="140">
                </center>
                <h3 class="title">Header - 8-pin Female (PTH, 0.1")</h3>
            </a>
            PRT-11895  
        </td>
    </tr>
</table>

!!! tip
    <p>New to soldering? Check out our <a href="https://learn.sparkfun.com/tutorials/5">Through-Hole Soldering Tutorial</a> for a quick introduction!</p>
    <p align="center">
        <a href="https://learn.sparkfun.com/tutorials/5">How to Solder: Through-Hole Soldering<br>
        <img src="https://cdn.sparkfun.com/c/264-148/assets/e/3/9/9/4/51d9fbe1ce395f7a2a000000.jpg"></a>
    </p>



### Li-Po Battery
<p>For mobile applications, users will want to pick up a <a href="https://www.sparkfun.com/categories/54">single-cell LiPo battery</a> from our catalog. Below, are a few available options:</p>

<table class="pdf">
    <tr>
        <td>
            <a href="https://www.sparkfun.com/products/13855">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/4/6/2/13855-01.jpg" alt="Lithium Ion Battery - 2Ah" height="140"></center>
                <h3 class="title">Lithium Ion Battery - 2Ah</h3>
            </a>
            PRT-13855
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/13851">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/4/5/8/13857-01.jpg" alt="Lithium Ion Battery - 400mAh" height="140">
                </center>
                <h3 class="title">Lithium Ion Battery - 400mAh</h3>
            </a>
            PRT-13851
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/13813">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/4/0/1/13813-01.jpg" alt="Lithium Ion Battery - 1Ah" height="140">
                </center>
                <h3 class="title">Lithium Ion Battery - 1Ah</h3>
            </a>
            PRT-13813
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/13853">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/4/6/0/13853-01.jpg" alt="Lithium Ion Battery - 110mAh" height="140">
                </center>
                <h3 class="title">Lithium Ion Battery - 110mAh</h3>
            </a>
            PRT-13853 
        </td>
    </tr>
</table>



### Jumper Modification
<p>To modify the jumpers, users will need <a href="https://www.sparkfun.com/categories/49">soldering equipment</a> and/or a <a href="https://www.sparkfun.com/categories/379">knife</a>.</p>


<table class="pdf">
    <tr>
        <td>
            <a href="https://www.sparkfun.com/products/9325">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/2/8/7/3/09325_9161-Solder_Lead_Free_-_100-gram_Spool-01.jpg" alt="Solder Lead Free - 100-gram Spool" height="140"></center>
                <h3 class="title">Solder Lead Free - 100-gram Spool</h3>
            </a>
            TOL-09325
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/14228">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/2/1/7/3/14228-01.jpg" alt="Weller WLC100 Soldering Station" height="140">
                </center>
                <h3 class="title">Weller WLC100 Soldering Station</h3>
            </a>
            TOL-14228
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/14579">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/2/7/2/5/14579-Chip_Quik_No-Clean_Flux_Pen_-_10mL-01.jpg" alt="Chip Quik No-Clean Flux Pen - 10mL" height="140">
                </center>
                <h3 class="title">Chip Quik No-Clean Flux Pen - 10mL</h3>
            </a>
            TOL-14579
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/9200">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/2/6/4/6/09200-Hobby_Knife-01.jpg" alt="Hobby Knife" height="140">
                </center>
                <h3 class="title">Hobby Knife</h3>
            </a>
            TOL-09200
        </td>
    </tr>
</table>


!!! tip
    <p>New to jumper pads? Check out our <a href="https://learn.sparkfun.com/tutorials/664">Jumper Pads and PCB Traces Tutorial</a> for a quick introduction!</p>
    <p align="center">
        <a href="https://learn.sparkfun.com/tutorials/664">How to Work with Jumper Pads and PCB Traces<br>
        <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg"></a>
    </p>


## Suggested Reading

As a more advanced development board, we will skip over the more fundamental tutorials (i.e. [**Ohm's Law**](https://learn.sparkfun.com/tutorials/voltage-current-resistance-and-ohms-law) and [**What is Electricity?**](https://learn.sparkfun.com/tutorials/what-is-electricity)). However, below are a few tutorials that may help users familiarize themselves with various aspects of the board.


<table class="pdf">
    <tr>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/8">Serial Communication<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/7/d/f/9/9/50d24be7ce395f1f6c000000.jpg"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/89">Analog vs. Digital<br>
<img src="https://cdn.sparkfun.com/c/264-148/assets/3/7/6/6/0/51c48875ce395f745a000000.png"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/51">Pulse Width Modulation<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/f/9/c/8/a/512e869bce395fbc64000002.JPG"></a>
        </td>
    </tr>
    <tr>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/62">Logic Levels<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/2/Input_Output_Logic_Level_Tolerances_tutorial_tile.png"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/82">I2C<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/8/2/I2C-Block-Diagram.jpg"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/16">Serial Peripheral Interface (SPI)<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/6/spiThumb_Updated.jpg"></a>
        </td>
    </tr>
    <tr>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/908">How to Install CH340 Drivers<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/9/0/8/USB-to-serial_converter_CH340-closeup.jpg"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/852">ESP32 Thing Plus Hookup Guide<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/8/5/2/SparkFun_Transparent_Graphical_OLED_Breakout__Qwiic__Hookup_Guide-01.jpg"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/61">Installing the Arduino IDE<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/1/arduinoThumb.jpg"></a>
        </td>
    </tr>
    <tr>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/1265">Installing Board Definitions in the Arduino IDE<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/2/6/5/sparkfun_boards.PNG"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/5">How to Solder: Through-Hole Soldering<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/e/3/9/9/4/51d9fbe1ce395f7a2a000000.jpg"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/664">How to Work with Jumper Pads and PCB Traces<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg"></a>
        </td>
    </tr>
</table>


<center>
![Qwiic Logo - light theme](https://docs.sparkfun.com/SparkFun_Thing_Plus_ESP32_WROOM_C/img/qwiic_logo-light.png#only-light){ width=400 }
![Qwiic Logo - dark theme](https://docs.sparkfun.com/SparkFun_Thing_Plus_ESP32_WROOM_C/img/qwiic_logo-dark.png#only-dark){ width=400 }
</center>

One of the new, advanced features of the board is that it takes advantage of the [Qwiic connect system](https://www.sparkfun.com/qwiic). We recommend familiarizing yourself with the **Logic Levels** and **I<sup>2</sup>C** tutorials.  Click on the banner above to learn more about [Qwiic products](https://www.sparkfun.com/qwiic).

<center>
    <iframe width="600" height="327" src="https://www.youtube.com/embed/x0RDEHqFIF8" title="SparkFun's Qwiic Connect System" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>