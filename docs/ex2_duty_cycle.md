This example shows how to read the BMV080 via Qwiic when the sensor is configured in duty cycle mode. Similar to the first example, the output will show the amount of particulate matter that is detected. However, it will show the readings every 20 seconds.

Head to the example 2 from the Arduino IDE's menu (located in **File** **Examples** > **SparkFun BMV080 Arduino Library** > **Example_02_DutyCycle**).

If you have not already, select your Board (in this case the **SparkFun ESP32 IoT RedBoard**), and associated COM port. Upload the code to the board and set the [Arduino Serial Monitor](https://learn.sparkfun.com/tutorials/terminal-basics/all#arduino-serial-monitor-windows-mac-linux) to **115200** baud. The Arduino should begin outputting the sensor readings every 20 seconds.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle;"><a href="../assets/img/"><img src="../assets/img/" width="600px" height="600px" alt="BMV080 Arduino Output Every 20 Seconds"></a></td>
    </tr>
  </table>
</div>
