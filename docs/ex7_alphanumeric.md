This example shows how to read the BMV080 via Qwiic when the sensor is configured in duty cycle mode and outputs the readings to display them on a Qwiic Alphanumeric display connected over a Qwiic daisy-chain. You'll need a [Qwii Alphanumeric Display](https://www.sparkfun.com/sparkfun-qwiic-alphanumeric-display-red.html) to run this example.

Head to the example 7 from the Arduino IDE's menu (located in **File** **Examples** > **SparkFun BMV080 Arduino Library** > **Example_07_Demo_Alphanumeric**).

If you have not already, select your Board and associated COM port. Upload the code to the board and set the [Arduino Serial Monitor](https://learn.sparkfun.com/tutorials/terminal-basics/all#arduino-serial-monitor-windows-mac-linux) to **115200** baud. The Arduino should begin outputting the sensor readings through the Arduino Serial Monitor and the Qwiic Alphanumeric display. For simplicity, we will only display PM2.5.
