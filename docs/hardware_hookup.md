### Connecting via Qwiic

By default, the sensor can be read through I<sup>2</sup>C. Insert a Qwiic cable between the SparkFun Qwiic Air Quality Sensor and your microcontroller. Then connect a compatible USB cable between the microcontroller and your computer's USB port.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Qwiic Cable, Air Quality Sensor, ESP32 IoT RedBoard, and USB Cable Connected"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Qwiic Cable, Air Quality Sensor, ESP32 IoT RedBoard, and USB Cable Connected</i></td>
    </tr>
  </table>
</div>

For users looking to display the current air quality readings in real time without a computer, we recommend getting an additional Qwiic cable and OLED display. The example in this tutorial uses the Qwiic OLED Display (1.3in., 128x64).

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Qwiic Cables, Air Quality Sensor, Qwiic OLED, ESP32 IoT RedBoard, and USB Cable Connected"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Qwiic Cables, Air Quality Sensor, Qwiic OLED, ESP32 IoT RedBoard, and USB Cable Connected</i></td>
    </tr>
  </table>
</div>



### Removing the BMV080 from the enclosure

For users that need to remove the BMV080 when soldering to the PTHs, you will need to remove the board from the enclosure. You may also want to remove sensor from the enclsoure when modifying the jumpers as well to avoid damaging the material when cutting or soldering the jumper pads. This section will go over how to remove the sensor from the enclosure.

    insert here



    parts spread out on table


Using a precision flathead with 0.1mm tip, slide the flathead in the slot and under the tab. Rock the precision flathead's handle toward the mounting hole so that the tab pops out.

    insert here




    flathead under tab and popping out the inner shell

 There is a rubber O-ring and lens between enclosure's inner and outer shell. You will want to carefully remove the inner shell holding the BMV080 over a clean, flat surface to avoid losing the small parts.

    insert here




    carefully removing inner shell showing the o-ring and lens

Slide the sensor out from the inner shell's slot. At this point, you should be able to solder male header pins from the top side so that you can access the longer mating pins from the bottom side. Depending on your preference, you can also solder jumper wires to the PTHs as well depending on your setup. Carefully clean the solder joints to remove any flux residue left on the board using isopropyl alcohol and a precision Q-tip.

!!! note
    When soldering make sure to not add too much solder. This may prevent your from being able to slide the breakout board back into the inner shell. For users soldering header pins, ensure that the header's plastic spacer is flush against the breakout board and not at an angle. For users soldering wire, ensure that the stripped wire is short.



### Reassembling the Enclosure

Now that we are done modifying the breakout board, it is time to place the sensor back in the enclosure! This section will go over how to reassemble the parts.

    insert here




    sensor back in enclosure

Slide the BMV080's breakout board into the inner shell so that the sensor aligns with the hole and the Qwiic connector aligns with the slot on the side of the inner shell's enclosure.

    insert here




    slide the BMV080 with headers back into the inner shell

Turn the board over on a clean, flat surface. Using tweezers, place the lens over the hole where the BMV080's sensor is located. Then place the o-ring over lens. Ensure that the parts are in their respective square and circular slots.

    insert here




    inner shell facing away from table with lens and o-ring placed on top

With the outer shell, align the hole for the lens and the slot for the Qwiic connector. Slide the outer shell in over the inner shell.

    insert here



    outer shell over the inner shell

Push down until you hear the tabs pop in.

    insert here



    push down on outer shell until the tabs pop in



### Connecting via PTH

!!! note
    When soldering directly to the PTHs, you will need to be careful of the 3D printed enclosure! You will want to carefully remove the board from the enclosure when soldering.

For temporary connections to the PTHs, you could use IC hooks to test out the pins. However, you'll need to solder headers or wires of your choice to the board for a secure connection. You can choose between a combination of [header pins and jumper wires](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all), or [stripping wire and soldering the wire](https://learn.sparkfun.com/tutorials/working-with-wire/all) directly to the board.

<div class="grid cards col-2" markdown>

-   <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/5/Soldering_Action-01.jpg"style="width:264px; height:148px; object-fit:contain;" alt="How to Solder: Through Hole Soldering">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all">
      <b>How to Solder: Through Hole Soldering</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->

-   <a href="https://learn.sparkfun.com/tutorials/working-with-wire/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/0/5/0/0/f/5138de3cce395fbb1b000002.JPG" style="width:264px; height:148px; object-fit:contain;" alt="Working with Wire">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/working-with-wire/all">
      <b>Working with Wire</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
</div>



### Interrupt

The following table shows the connection that is required between an ESP32 and the SparkFUn Qwiic Air Quality Sensor when using I<sup>2</sup>C as the communication interface with interrupts.

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; border: solid 1px #cccccc;">ESP32 Pinout<br />(i.e. IoT RedBoard - ESP32, ESP32 Thing Plus C, etc.)
            </th>
            <th style="text-align: center; border: solid 1px #cccccc;">SparkFun Qwiic Air Quality Sensor<br />BMV080
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">3.3V</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">3V3</font>
            </td>
        </tr>
        <tr>        
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">SDA</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">SDA (PICO)</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#fff3cd"><font color="#000000">SCL</font>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#fff3cd"><font color="#000000">SCL (SCK)</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">14</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">IRQ</font>
            </td>
        </tr>
    </table>
</div>



### SPI

The following tables shows the connection that is required between between an ESP32 and the SparkFun Qwiic Air Quality Sensor when using SPI as the communication interface. You will need to cut the MODE jumper between the center pad and the pad labeled as I2C. Then add solder between the center pad and the pad labeled as SPI. Make sure to also leave the AB0 jumper open (i.e. both sides of the jumper are not connected).

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; border: solid 1px #cccccc;">ESP32 Pinout<br />(i.e. IoT RedBoard - ESP32, ESP32 Thing Plus C, etc.)
            </th>
            <th style="text-align: center; border: solid 1px #cccccc;">SparkFun Qwiic Air Quality Sensor<br />BMV080
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">3.3V</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">3V3</font>
            </td>
        </tr>
        <tr>        
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">PICO</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">PICO (SDA)</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">POCI</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">POCI (AB0)</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#fff3cd"><font color="#000000">SCK</font>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#fff3cd"><font color="#000000">SCK (SCL)</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">CS</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">CS (AB1)</font>
            </td>
        </tr>
    </table>
</div>
