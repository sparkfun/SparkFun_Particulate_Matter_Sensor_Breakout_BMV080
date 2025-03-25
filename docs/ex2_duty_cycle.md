This example shows how to read the BMV080 via Qwiic when the sensor is configured in duty cycle mode. Similar to the first example, the output will show the amount of particulate matter that is detected. However, it will show the readings every 20 seconds.

Head to the example 2 from the Arduino IDE's menu (located in **File** **Examples** > **SparkFun BMV080 Arduino Library** > **Example_02_DutyCycle**).

If you have not already, select your Board and associated COM port. Upload the code to the board and set the [Arduino Serial Monitor](https://learn.sparkfun.com/tutorials/terminal-basics/all#arduino-serial-monitor-windows-mac-linux) to **115200** baud. The Arduino should begin outputting the sensor readings every 20 seconds.
