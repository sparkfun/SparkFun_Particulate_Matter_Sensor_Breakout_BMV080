In this section, we will highlight the hardware and pins that are broken out on the SparkFun Qwiic Air Quality PM1/PM2.5/PM10 Sensor - BMV080. For more information, check out our [Resources and Going Further](../resources/) on the components used for the sensor.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Top View"></a></td>
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Bottom View"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Top View</i></td>
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Bottom View</i></td>
    </tr>
  </table>
</div>



### BMV080

The breakout board comes with Bosch's BMV080 populated and takes advantage of its flexible cable with the FPC 13-pin 0.33mm connector. The sensor is an ultra-small, fan-less air quality sensor for sensing PM1, PM2.5, and PM10 concentrations. A special lens allows the laser to pass through the enclosure to take measurements.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="BMV080"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>BMV080</i></td>
    </tr>
  </table>
</div>

!!! Note
    This is a [CLASS 1](https://en.wikipedia.org/wiki/Laser_safety#Class_1) LASER PRODUCT CLASSIFIED IEC 60825-1 2014.



### Power

To power the board, you will need **3.3V**. You can connect a Qwiic cable to the Qwiic connector. Or you could solder directly to the PTHs. Below are the power pins that are broken out on the edge of the board.

* **3V3** &mdash; This pin is the voltage input for the board. The recommended input voltage for this pin is 3.3V.
* **GND** &mdash; Of course, is the common, ground voltage (0V reference) for the system.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
      <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Power and Ground Highlighted - Top View"></a></td>
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Power, Ground, and Qwiic Connector Highlighted - Bottom View"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
      <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Power and Ground Highlighted - Top View</i></td>
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Power, Ground, and Qwiic Connector Highlighted - Bottom View</i></td>
    </tr>
  </table>
</div>



### Qwiic and I<sup>2</sup>C

By default, the communication interface is set to I<sup>2</sup>C with the MODE jumper. The board includes one horizontal Qwiic connector to connect to other Qwiic-enabled I<sup>2</sup>C devices. However, the board still breaks out 0.1"-spaced pins for users who prefer a soldered connection.

* **SCL/SCK** &mdash; On the top side, the pin is labeled as SCL. On the bottom side, the pin is labeled as SCK. Thus the pin is used for the I<sup>2</sup>C clock.
* **SDA/PICO** &mdash; On the top side, the pin is labeled as SDA. On the bottom side, the pin is labeled as PICO. Thus the pin is used for the I<sup>2</sup>C data.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Qwiic Connector and I2C Highlighted - Top View"></a></td>
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Qwiic Connector and I2C Highlighted - Bottom View"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Qwiic Connector and I<sup>2</sup>C Highlighted - Top View</i></td>
      <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>I<sup>2</sup>C Highlighted - Bottom View</i></td>
    </tr>
  </table>
</div>

The default address of the BMV080 is set to **0x57** by default. By configuring AB1 and AB0 jumpers, you can adjust the I<sup>2</sup>C address to an alternative address. For more information, check below under the jumpers.



### Interrupt Pin

The board includes an interrupt pin when the board is set to I<sup>2</sup>C mode.

* **IRQ** &mdash; Short for interrupt. This pin sends an interrupt signal to a microcontroller.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Interrupt Pin Highlighted - Top View"></a></td>
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Interrupt Pin Highlighted - Bottom View"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Interrupt Pin Highlighted - Top View</i></td>
      <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Interrupt Pin Highlighted - Bottom View</i></td>
    </tr>
  </table>
</div>

!!! note
    The hardware interrupt of the BMV080 sensor unit cannot be used as trigger
    in duty cycling mode.



### SPI

The BMV080 can also be set to SPI as the communication interface by adjusting the MODE jumper on the back.

* **PICO/SDA** &mdash; On the bottom side, the pin is labeled as PICO (i.e. Peripheral In, Controller Out). On the top side, the pin is labeled as SDA.
* **POCI/AB0** &mdash; On the bottom side, the pin is labeled as POCI (i.e. Peripheral Out, Controller In). On the top side, the pin is labeled as AB0. When set to SPI mode, make sure to leave AB0 (POCI) open!
* **SCK/SCL** &mdash; On the bottom side, the pin is labeled as SCK for the clock. On the tip side, the pin is labeled as SCL.
* <b><span style="text-decoration: overline">CS</span></b> &mdash; On the bottom side, the pin is labeled as <span style="text-decoration: overline">CS</span> (i.e. chip select). On the top side, the pin is labeled as AB1. This pin is active low. When set to SPI mode, make sure to leave AB1 (<span style="text-decoration: overline">CS</span>) open!

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="SPI Pins Highlighted - Top View"></a></td>
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="SPI Pins Highlighted - Bottom View"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>SPI Pins Highlighted - Top View</i></td>
      <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>SPI Pins Highlighted - Bottom View</i></td>
    </tr>
  </table>
</div>

### Jumpers

!!!note
    If this is your first time working with jumpers, check out the [How to Work with Jumper Pads and PCB Traces](https://learn.sparkfun.com/tutorials/how-to-work-with-jumper-pads-and-pcb-traces/all) tutorial for more information.

The back of the board includes jumpers to configure the board.

* **I<sup>2</sup>C** &mdash; By default, this three-pad jumper is closed. The three way jumper labeled I<sup>2</sup>C connects 3.3V to two 2.2k&ohm; pull-up resistors and to the I<sup>2</sup>C data and clock lines. If multiple devices are connected to the bus with the pull-up resistors enabled, the parallel equivalent resistance will create too strong of a pull-up for the bus to operate correctly. As a general rule of thumb, [disable all but one pair of pull-up resistors](https://learn.sparkfun.com/tutorials/i2c/all#i2c-at-the-hardware-level) if multiple devices are connected to the bus.
* **AB0** &mdash; Address jumper 0 when the BMV080 is set to I<sup>2</sup>C mode. This is a multifunctional pin. This is also connected to POCI. By default, the three-pad jumper's center pad is connected to the `1` side
* **AB1** &mdash; Address jumper 1 when the BMV080 is set to I<sup>2</sup>C mode. This is a multifunctional pin. This is also connected to <span style="text-decoration: overline">CS</span>. By default, the three-pad jumper's center pad is connected to the `1` side
* **MODE** &mdash; By default, this three-pad jumper is closed between the center pad and the pad labeled as I2C. Thus, the communication interface is set to I<sup>2</sup>C. Cutting this trace and adding solder between the center pad and the pad labeled as SPI will configure the communication interface as SPI.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Jumpers Highlighted - Bottom View"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Jumpers Highlighted - Bottom View</i></td>
    </tr>
  </table>
</div>

When the SparkFun Qwiic Air Quality Sensor is configured in I2C mode, users have the ability to configure the default address using AB0 and AB1 jumpers. The following table shows the possible I<sup>2</sup>C address based on the jumper configuration.

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; border: solid 1px #cccccc;">AB1
            </th>
            <th style="text-align: center; border: solid 1px #cccccc;">AB0
            </th>
            <th style="text-align: center; border: solid 1px #cccccc;">I<sup>2</sup>C Address
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;">0
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;">0
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;">0x54
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;">0
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;">1
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;">0x55
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;">1
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;">0
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;">0x56
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;">1
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;">1
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;"><b>0x57 (default)</b>
            </td>
        </tr>
    </table>
</div>

!!! note
    AB0 is a multifunctional pin! When the SparkFun Qwiic Air Quality Sensor is configured for SPI, make sure to leave AB0 (POCI) open!



### 3D Model

A 3D model of the board and components was exported to a STEP file using KiCad.

<!-- Import the component -->
<script type="module" src="https://ajax.googleapis.com/ajax/libs/model-viewer/3.5.0/model-viewer.min.js"></script>

<center>
    <model-viewer src="../assets/3d_model/SparkFun_BMV080_v10_3D_model.glb" camera-controls poster="../assets/3d_model/SparkFun_BMV080_v10_3D_image.jpg" environment-image="legacy" shadow-intensity="1.58" exposure="0.64" shadow-softness="0.24" tone-mapping="neutral" camera-orbit="-46.67deg 57.14deg 153.3m" field-of-view="30deg" style="width: 750px; height: 500px;">
    </model-viewer>
</center>
<br />
<div style="text-align: center">
    <a href="../assets/3d_model/SparkFun_BMV080_v10_3D_model.step" target="stp_file" class="md-button">Click Here for the STEP File</a>
</div>



### Board Dimensions

The board is 0.5" x 0.95" (12.70mm x 24.13mm). To make the board as small as possible, there are no mounting holes.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/SparkFun_Particulate_Matter_Sensor_Breakout_BMV080_Board_Dimensions.png"><img src="../assets/img/SparkFun_Particulate_Matter_Sensor_Breakout_BMV080_Board_Dimensions.png" width="600px" height="600px" alt="Board Dimensions"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Board Dimensions</i></td>
    </tr>
  </table>
</div>
