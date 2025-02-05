This example shows how to read the BMV080 via Qwiic when the sensor is configured in continuous mode. The output will show the amount of particulate matter that is detected.

Head to the example 1 from the Arduino IDE's menu (located in **File** **Examples** > **SparkFun BMV080 Arduino Library** > **Example_01_BasicReadings**).

If you have not already, select your Board (in this case the **SparkFun ESP32 IoT RedBoard**), and associated COM port. Upload the code to the board and set the [Arduino Serial Monitor](https://learn.sparkfun.com/tutorials/terminal-basics/all#arduino-serial-monitor-windows-mac-linux) to **115200** baud. The Arduino should begin outputting the sensor readings. If the air in front of the sensor is void of particulate matter, you should see `0.00` for each size.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="BMV080 Arduino Output"></a></td>
    </tr>
  </table>
</div>

Try placing a scented candle or spray some air freshener across the sensor. You should see the sensor readings jump up depending on the PM size.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="BMV080 Arduino Output"></a></td>
    </tr>
  </table>
</div>

When the sensor detects an object in front of the it, the output will indicate that the sensor is `obstructed`."

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="BMV080 Arduino Output"></a></td>
    </tr>
  </table>
</div>
