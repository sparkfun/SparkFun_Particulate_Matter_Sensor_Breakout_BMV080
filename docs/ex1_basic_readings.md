This example shows how to read the BMV080 via Qwiic when the sensor is configured in continuous mode. The output will show the amount of particulate matter that is detected.

Head to the example 1 from the Arduino IDE's menu (located in **File** **Examples** > **SparkFun BMV080 Arduino Library** > **Example_01_BasicReadings**).

If you have not already, select your Board (if you're following along with the suggested dev board for this tutorial, select **SparkFun ESP32 IoT RedBoard**), and associated COM port. Upload the code to the board and set the [Arduino Serial Monitor](https://learn.sparkfun.com/tutorials/terminal-basics/all#arduino-serial-monitor-windows-mac-linux) to **115200** baud. The Arduino should begin outputting the sensor readings. If the air in front of the sensor is void of particulate matter, you should see `0.00` for each size.

<center>
[![Screenshot of Example 1 serial printout](./assets/img/BMV080_Arduino_Example_01_Screenshot.png){ width="600"}](./assets/img/BMV080_Arduino_Example_01_Screenshot.png "Click to enlarge")
</center>

Try placing something like a scented candle or other source of particulate matter near the sensor. You should see the sensor readings jump up depending on the PM size. When the sensor detects an object in front of the it, the code prints out `obstructed`.
