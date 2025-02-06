Below are the instructions to quickly get started Qwiic Air Quality Sensor with an Arduino! For more in depth information about the sensor and examples, make sure to check out the rest of the tutorial!

1.) Connect a Qwiic cable between the Qwiic Air Quality Sensor and the SparkFun IoT RedBoard - ESP32.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Qwiic Air Quality Sensor Connected to SparkFun IoT RedBoard - ESP32"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Qwiic Air Quality Sensor Connected to SparkFun IoT RedBoard - ESP32</i></td>
    </tr>
  </table>
</div>

2.) Connect a USB cable between your computer and the SparkFun IoT RedBoard.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="USB Cable to SparkFun IoT RedBoard"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>USB Cable to SparkFun IoT RedBoard</i></td>
    </tr>
  </table>
</div>

3.) Select the board definition (in this case, it was **SparkFun ESP32 IoT RedBoard**).

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Select Board Definition from Arduino IDE"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Select Board Definition from Arduino IDE</i></td>
    </tr>
  </table>
</div>

4.) Select the COM port (in this case, it was **COM13**).

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Select COM Port from Arduino IDE"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Select COM Port from Arduino IDE</i></td>
    </tr>
  </table>
</div>

5.) In the Arduino Library Manager, search for the "**SparkFun BMV080**" to  install the [SparkFun BMV080 Arduino Library](https://github.com/sparkfun/SparkFun_BMV080_Arduino_Library).

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Install Arduino Library"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Install Arduino Library</i></td>
    </tr>
  </table>
</div>

6.) Open example 1 through the Arduino IDE's menu: **File** > **Examples** > **SparkFun BMV080 Arduino Library** > **Example_01_BasicReadings**.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Open Example 1"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Open Example 1</i></td>
    </tr>
  </table>
</div>

7.) Upload example code.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="Upload example code"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Upload example code</i></td>
    </tr>
  </table>
</div>

8.) Open Arduino Serial Monitor at **115200** to begin detecting particulate matter!

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="BMV080 Arduino Output"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>BMV080 Arduino Output</i></td>
    </tr>
  </table>
</div>
