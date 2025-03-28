
!!! arduino
    This example assumes you are using the latest version of the Arduino IDE on your desktop. If this is your first time using Arduino IDE, library, or board add-on, please review the following tutorials.

    - [Installing the Arduino IDE](https://learn.sparkfun.com/tutorials/installing-arduino-ide)
    - [Installing an Arduino Library](https://learn.sparkfun.com/tutorials/installing-an-arduino-library)
    - [Installing Board Definitions in the Arduino IDE](https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide)

!!! note
    If you've never connected an CH340 device to your computer before, you may need to install drivers for the USB-to-serial converter. Check out our section on "[How to Install CH340 Drivers](https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers)" for help with the installation.

    - [How to Install CH340 Drivers](https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all)

SparkFun has written a library using Bosch's API to work with the BMV080! You can obtain this library through the Arduino Library Manager by searching for "**SparkFun BMV080**". Find the one written by SparkFun Electronics and install the latest version. Users who prefer to manually install the library can get it from the [GitHub Repository](https://github.com/sparkfun/SparkFun_BMV080_Arduino_Library) or download the .ZIP by clicking the button below:

<div style="text-align: center"><a href="https://github.com/sparkfun/SparkFun_BMV080_Arduino_Library/archive/refs/heads/main.zip" class="md-button">SparkFun BMV080 Arduino Library (ZIP)</a></div>

!!! note
    The SparkFun BMV080 Arduino Library uses the [SparkFun Toolkit](https://github.com/sparkfun/SparkFun_Toolkit) as a dependency. This should automatically download when installing the library using the Arduino Library Manager. For users that are installing the BMV080 library manually, make sure to download the SparkFun Toolkit as well. At the time of writing, we were using the following Arduino Libraries, firmware binaries, board add-ons.


     * Arduino Libraries
        * **SparkFun BMV080 Arduino Library**
        * **SparkFun Toolkit v1.0.0**
     * Board Definitions
        * **esp32 by Espressif v3.0.1** for the IoT RedBoard - ESP32.


Now that we have our library and board add-on installed, we can start experimenting with the breakout board. For the scope of this tutorial, we will highlight the examples to get started. From there we will be able to build our own custom code to integrate the development board into a project.
