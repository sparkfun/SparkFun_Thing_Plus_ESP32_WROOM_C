# Software Overview

### CH340 Driver
Users will need to install the appropriate driver for their computer to recognize the serial-to-UART chip on their board/adapter. Most of the latest operating systems will recognize CH340C chip on the board and automatically install the required driver.

*To manually install the CH340 driver on their computer, users can download it from the [WCH website](http://www.wch-ic.com/products/CH340.html?). For more information, check out our [How to Install CH340 Drivers Tutorial](https://www.sparkfun.com/ch340).*

<!-- tutorial_big(908) -->


### Arduino IDE
<div class="alert alert-info"><b>Note:</b> For first-time users, who have never programmed before and are looking to use the Arduino IDE, we recommend beginning with the <a href="https://www.sparkfun.com/products/15631">SparkFun Inventor's Kit (SIK)</a>, which includes a simpler board like the <a href="https://www.sparkfun.com/products/11224">Arduino Uno</a> or <a href="https://www.sparkfun.com/products/15123">SparkFun RedBoard</a> and is designed to help users get started programming with the Arduino IDE.</div>

Most users may already be familiar with the Arduino IDE and it's use. However, for those of you who have never heard the name *Arduino* before, feel free to check out the [Arduino website](https://www.arduino.cc/en/Guide/HomePage). To get started with using the Arduino IDE, check out our tutorials below:

<!-- tutorials_by_id(15, 50, 61, 1265) -->

#### Install Board Definition
Install the latest <b>ESP32</b> board definitions in the Arduino IDE.

<!-- tutorial_big(1265) -->
<div class="alert alert-info">
    <p><b>Note:</b> For more instructions, users can follow this tutorial on <a href="https://www.arduino.cc/en/guide/cores">Installing Additional Cores</a> provided by Arduino. Users will also need the <code>.json</code> file for the Espressif Arduino core:</p>
    <p><center>
        <a href="https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json"><code>https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json</code></a>
    </center></p>
</div>

When selecting a board to program in the Arduino IDE, users should select the **SparkFun ESP32 Thing Plus C** from the Tools drop down menu *(i.e. **Tools** > **Board** > **ESP32 Arduino** > **SparkFun ESP32 Thing Plus C**)*. Alternatively, users can also select the **ESP32 Dev Module**; however, they may loose some pin assignments (i.e. `LED_BUILTIN`).

[![Board Selection](https://cdn.sparkfun.com/r/600-600/assets/learn_tutorials/2/3/5/3/board_selection.png)](https://cdn.sparkfun.com/assets/learn_tutorials/2/3/5/3/board_selection.png)<br>
*Selecting the **SparkFun ESP32 Thing Plus C** from the Tools drop down menu in the Arduino IDE. (Click to enlarge)*
