!!! note
    Make sure to configure the board for SPI mode by adjusting the jumpers on the back of the board. You will also need to solder headers to the board and wire to your Arduino's SPI port.

This example shows how to read the BMV080 via SPI when the sensor is configured to continuous mode.

Head to the example 4 from the Arduino IDE's menu (located in **File** **Examples** > **SparkFun BMV080 Arduino Library** > **Example_04_SPI**).

If you have not already, select your Board and associated COM port. Upload the code to the board and set the [Arduino Serial Monitor](https://learn.sparkfun.com/tutorials/terminal-basics/all#arduino-serial-monitor-windows-mac-linux) to **115200** baud. The Arduino should begin outputting the sensor readings.
