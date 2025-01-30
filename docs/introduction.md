


The [SparkFun Qwiic Air Quality PM1/PM2.5/PM10 Sensor - BMV080]() is an ultra-small, fan-less air quality sensor for sensing PM2.5 particulate matter! Within the enclosure is a breakout board that breaks out Bosch's BMV080, the world's smallest PM2.5 air quality sensor. The sensing element measures merely 4.2mm x 3.5mm x 3.1mm (W x L x H), which is more than 450 times smaller than any comparable device on the market. The innovative design is based on ultra-compact lasers with integrated photodiodes. The sensor applies sophisticated algorithms to measure PM2.5 concentration directly in free space, without requiring an intrusive fan. <!-- PM1 and PM10 concentrations can also be measured as well! -->

<div class="grid cards" style="width:500px; margin: 0 auto;" markdown>

-   <a href="https://www.sparkfun.com/products/26554">
      <figure markdown>
        <img src="" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Qwiic Mini Particulate Matter Sensor Breakout - BMV080">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/26554">
      <b>SparkFun Qwiic Mini Particulate Matter Sensor Breakout - BMV080</b>
      <br />
      SEN-26554
      <br />
      <center>[Purchase from SparkFun :fontawesome-solid-cart-plus:](https://){ .md-button .md-button--primary }</center>
    </a>
</div>


In this tutorial, we'll go over the hardware and how to hookup the sensor to an Arduino. We will also go over examples from the Arduino Library to get started.



### Required Materials

To follow along with this tutorial, you will need the following materials. You may not need everything though depending on what you have. Add it to your cart, read through the guide, and adjust the cart as necessary.



<div class="grid cards col-4" markdown>

<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/usb-3-1-cable-a-to-c-3-foot.html">
      <figure markdown>
        <img src="https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/1/4/14743-USB_3.1_Cable_A_to_C_-_3_Foot-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="USB 3.1 Cable A to C - 3 Foot">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/usb-3-1-cable-a-to-c-3-foot.html">
      <b>USB 3.1 Cable A to C - 3 Foot</b>
      <br />
      CAB-14743
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/sparkfun-iot-redboard-esp32-development-board.html">
      <figure markdown>
        <img src="https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/E/S/ESP32_03.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun IoT RedBoard - ESP32 Development Board">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/sparkfun-iot-redboard-esp32-development-board.html">
      <b>SparkFun IoT RedBoard - ESP32 Development Board</b>
      <br />
      WRL-19177
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="">
      <figure markdown>
        <img src="" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Qwiic Air Quality PM1/PM2.5/PM10 Sensor - BMV080">
      </figure>
    </a>

    ---

    <a href="">
      <b>SparkFun Qwiic Air Quality PM1/PM2.5/PM10 Sensor - BMV080</b>
      <br />
      SEN-26554
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/flexible-qwiic-cable-200mm.html">
      <figure markdown>
        <img src="https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/1/7/17258-Flexible_Qwiic_Cable_-_200mm-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Flexible Qwiic Cable - 200mm">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/flexible-qwiic-cable-200mm.html">
      <b>Flexible Qwiic Cable - 200mm</b>
      <br />
      PRT-17258
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Other Microcontrollers

We recommend using any board with an ESP32 (such as the ESP32-WROOM, ESP32-S2, and ESP32-S3). We'll be using the RedBoard IoT RedBoard - ESP32 Development Board for the examples in this tutorial.

<div class="grid cards col-4" markdown>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/sparkfun-iot-redboard-esp32-development-board.html">
      <figure markdown>
        <img src="https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/E/S/ESP32_03.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun IoT RedBoard - ESP32 Development Board">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/sparkfun-iot-redboard-esp32-development-board.html">
      <b>SparkFun IoT RedBoard - ESP32 Development Board</b>
      <br />
      WRL-19177
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/sparkfun-thing-plus-esp32-wroom-usb-c.html">
      <figure markdown>
        <img src="https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/2/0/20168Diagonal.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Thing Plus - ESP32 WROOM (USB-C)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/sparkfun-thing-plus-esp32-wroom-usb-c.html">
      <b>SparkFun Thing Plus - ESP32 WROOM (USB-C)</b>
      <br />
      WRL-20168
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/sparkfun-thing-plus-esp32-s2-wroom.html">
      <figure markdown>
        <img src="https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/1/7/17743-SparkFun_Thing_Plus_-_ESP32-S2_WROOM-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Thing Plus - ESP32-S2 WROOM">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/sparkfun-thing-plus-esp32-s2-wroom.html">
      <b>SparkFun Thing Plus - ESP32-S2 WROOM</b>
      <br />
      WRL-17743
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/sparkfun-thing-plus-esp32-s3.html">
      <figure markdown>
        <img src="https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/W/R/WRL-24408-ESP-32-S3-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Thing Plus - ESP32-S3">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/sparkfun-thing-plus-esp32-s3.html">
      <b>SparkFun Thing Plus - ESP32-S3</b>
      <br />
      WRL-24408
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Qwiic Cables

For those that want to take advantage of the Qwiic connector, you'll want to grab a Qwiic cable. Besides the one listed earlier, there are a variety of other cable lengths available in the SparkFun catalog to choose from.

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/15081">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/3/4/3/1/15081-_01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Qwiic Cable Kit">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/15081">
      <b>SparkFun Qwiic Cable Kit</b>
      <br />
      KIT-15081
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14427">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/2/4/5/3/14427-Qwiic_Cable_-_100mm-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Qwiic Cable - 100mm">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14427">
      <b>Qwiic Cable - 100mm</b>
      <br>
      PRT-14427
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14429">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/2/4/5/5/14429-Qwiic_Cable_-_500mm-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Qwiic Cable - 500mm">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14429">
      <b>Qwiic Cable - 500mm</b>
      <br />
      PRT-14429
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14425">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/2/4/5/1/14425-Qwiic_Cable_-_Breadboard_Jumper__4-pin_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Qwiic Cable - Breadboard Jumper (4-pin)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14425">
      <b>Qwiic Cable - Breadboard Jumper (4-pin)</b>
      <br />
      PRT-14425
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>


### Tools (Optional)

!!! note
    When soldering directly to the PTHs, you will need to be careful of the 3D printed enclosure! You will want to carefully remove the board from the enclosure when soldering.

You will need a soldering iron, solder, and [general soldering accessories](https://www.sparkfun.com/categories/49) for a secure connection when using the plated through holes.

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/14456">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/1/2/4/9/0/14456-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Soldering Iron - 60W (Adjustable Temperature)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14456">
      <b>Soldering Iron - 60W (Adjustable Temperature)</b>
      <br />
      TOL-14456
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9163">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/5/8/7/09162-02-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Solder Lead Free - 15-gram Tube">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9163">
      <b>Solder Lead Free - 15-gram Tube</b>
      <br>
      TOL-09163
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/11375">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/7/1/2/0/11375-Hook-Up_Wire_-_Assortment__Solid_Core__22_AWG_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Hook-Up Wire - Assortment (Stranded, 22 AWG)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/11375">
      <b>Hook-Up Wire - Assortment (Stranded, 22 AWG)</b>
      <br />
      PRT-11375
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/12630">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/9/3/1/2/12630-Hakko-Wire-Strippers-30AWG-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Wire Strippers - 30AWG (Hakko)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/12630">
      <b>Wire Strippers - 30AWG (Hakko)</b>
      <br />
      TOL-12630
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/11952">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/8/4/2/2/11952-Hakko-Flush-Cutters-feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Flush Cutters - Hakko">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/11952">
      <b>Flush Cutters - Hakko</b>
      <br />
      TOL-11952
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/hobby-knife.html">
      <figure markdown>
        <img src="https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/0/9/09200-Hobby_Knife-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Hobby Knife">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/hobby-knife.html">
      <b>Hobby Knife</b>
      <br />
      TOL-09200
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>


### Prototyping Accessories (Optional)

Depending on your setup, you may want to use IC hooks for a temporary connection. However, you will want to solder header pins to connect devices to the plated through holes for a secure connection. We opted for right angle headers for the SparkFun Qwiic Air Quality PM1/PM2.5/PM10 Sensor - BMV080 as well as M/F jumpers to connect to the RedBoard IoT Development Board to reduce the amount of soldering.

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/12002">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/8/5/0/3/12002-Breadboard_-_Self-Adhesive__White_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Breadboard - Self-Adhesive (White)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/12002">
      <b>Breadboard - Self-Adhesive (White)</b>
      <br />
      PRT-12002
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9741">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/3/6/9/6/09741-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="IC Hook with Pigtail">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9741">
      <b>IC Hook with Pigtail</b>
      <br>
      CAB-09741
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/553">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/3/7/8/00553-03-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Break Away Male Headers - Right Angle">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/553">
      <b>Break Away Male Headers - Right Angle</b>
      <br />
      PRT-00553
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9140">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/2/5/5/7/09140-02-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Jumper Wires Premium 6" M/F Pack of 10">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9140">
      <b>Jumper Wires Premium 6" M/F Pack of 10</b>
      <br />
      PRT-09140
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Suggested Reading

If you aren't familiar with the Qwiic Connection System, we recommend reading [here for an overview](https://www.sparkfun.com/qwiic).

<div style="text-align: center">
  <table style="border-style:none">
    <tr>
     <td style="text-align: center; vertical-align: middle;">
     <div style="text-align: center"><a href="https://www.sparkfun.com/qwiic"><img src="../assets/Qwiic-registered-updated.png" alt="Qwiic Connection System" title="Click to learn more about the Qwiic Connection System!"></a>
     </div>
    </td>
    </tr>
    <tr>
      <td style="text-align: center; vertical-align: middle;"><div style="text-align: center"><i><a href="https://www.sparkfun.com/qwiic">Qwiic Connection System</a></i></div></td>
    </tr>
  </table>
</div>

If you aren’t familiar with the following concepts, we also recommend checking out a few of these tutorials before continuing.

<div class="grid cards col-4" markdown>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/installing-arduino-ide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/6/1/arduinoThumb.jpg" style="width:264px; height:148px; object-fit:contain;" alt="Installing Arduino IDE">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/installing-arduino-ide">
      <b>Installing Arduino IDE</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/1/2/6/5/sparkfun_boards.PNG" style="width:264px; height:148px; object-fit:contain;" alt="Installing Board Definitions in the Arduino IDE">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide">
      <b>Installing Board Definitions in the Arduino IDE</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/iot-redboard-esp32-development-board-hookup-guide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/2/2/5/7/285808434_548438690244031_7008413248633042033_n.jpg" style="width:264px; height:148px; object-fit:contain;" alt="IoT RedBoard ESP32 Development Board Hookup Guide">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/iot-redboard-esp32-development-board-hookup-guide">
      <b>IoT RedBoard ESP32 Development Board Hookup Guide</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/9/0/8/USB-to-serial_converter_CH340-closeup.jpg" style="width:264px; height:148px; object-fit:contain;" alt="How to Install CH340 Drivers">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all">
      <b>How to Install CH340 Drivers</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/i2c">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/8/2/I2C-Block-Diagram.jpg" style="width:264px; height:148px; object-fit:contain;" alt="I2C">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/i2c">
      <b>I2C</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/serial-peripheral-interface-spi">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/1/6/spiThumb_Updated2.png" style="width:264px; height:148px; object-fit:contain;" alt="Serial Peripheral Interface (SPI)">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/serial-peripheral-interface-spi">
      <b>Serial Peripheral Interface (SPI)</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/logic-levels">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/6/2/Input_Output_Logic_Level_Tolerances_tutorial_tile.png" style="width:264px; height:148px; object-fit:contain;" alt="Logic Levels">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/logic-levels">
      <b>Logic Levels</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
</div>
