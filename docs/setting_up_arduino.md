
!!! arduino
    This example assumes you are using the latest version of the Arduino IDE on your desktop. If this is your first time using Arduino IDE, library, or board add-on, please review the following tutorials.

    - [Installing the Arduino IDE](https://learn.sparkfun.com/tutorials/installing-arduino-ide)
    - [Installing an Arduino Library](https://learn.sparkfun.com/tutorials/installing-an-arduino-library)
    - [Installing Board Definitions in the Arduino IDE](https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide)


## SparkFun BMV080 Arduino Library Install

SparkFun has written a library using Bosch's API to work with the BMV080! You can obtain this library through the Arduino Library Manager by searching for "**SparkFun BMV080**". Find the one written by SparkFun Electronics and install the latest version. Users who prefer to manually install the library can get it from the [GitHub Repository](https://github.com/sparkfun/SparkFun_BMV080_Arduino_Library) or download the .ZIP by clicking the button below:


[SparkFun BMV080 Arduino Library (ZIP)](https://github.com/sparkfun/SparkFun_BMV080_Arduino_Library/archive/refs/heads/feature/remove-bosch-sdk.zip){ .md-button .md-button--primary }


!!! note
    The SparkFun BMV080 Arduino Library uses the [SparkFun Toolkit](https://github.com/sparkfun/SparkFun_Toolkit) as a dependency. This should automatically download when installing the library using the Arduino Library Manager. For users that are installing the BMV080 library manually, make sure to download the SparkFun Toolkit as well. At the time of writing, we were using the following Arduino Libraries, firmware binaries, board add-ons.


     * Arduino Libraries
        * **SparkFun BMV080 Arduino Library**
        * **SparkFun Toolkit v1.0.0**
     * Board Definitions
        * **esp32 by Espressif v3.0.1** for the IoT RedBoard - ESP32.

## Adding the BMV080 SDK

The SparkFun BMV080 Arduino library requires some manual installation as it does **not** include the required files from BMV080 SDK from Bosch. After installing the SparkFun library, users need to download the SDK from [this page](https://www.bosch-sensortec.com/products/environmental-sensors/particulate-matter-sensor/bmv080/#documents) and then manually place the necessary files in the SparkFun BMV080 Arduino library folder. The tables below outlines where to find the Arduino Libraries folder along with the filepaths and filenames of all SDK files you'll need to copy into the SparkFun BMV080 Arduino folder:

### Library Install Directory

| OS | Directory|
|---|---|
|macOS | $HOME/Documents/Arduino/libraries/SparkFun_BMV080_Arduino_Library|
|Windows | $HOME\Documents\Arduino\libraries\SparkFun_BMV080_Arduino_Library|
|Linux| $HOME/Arduino/libraries/SparkFun_BMV080_Arduino_Library|

### Files to copy and locations to copy to

From the Bosch SDK, the following files are copied into the specified library locations.

|Bosch SDK File | SparkFun BMV080 Arduino Library Directory|
|--|--|
|api/inc/bmv080.h| src/sfTk/bmv080.h|
|api/inc/bmv080_defs.h| src/sfTk/bmv080_defs.h|
|api/api/lib/xtensa_esp32/xtensa_esp32_elf_gcc/release/lib_bmv080.a | src/esp32/lib_bmv080.a|
|api/api/lib/xtensa_esp32/xtensa_esp32_elf_gcc/release/lib_postProcessor.a | src/esp32/lib_postProcessor.a|
|api/api/lib/xtensa_esp32s2/xtensa_esp32s2_elf_gcc/release/lib_postProcessor.a | src/esp32s2/lib_postProcessor.a|
|api/api/lib/xtensa_esp32s2/xtensa_esp32s2_elf_gcc/release/lib_bmv080.a | src/esp32s2/lib_bmv080.a|
|api/api/lib/xtensa_esp32s3/xtensa_esp32s3_elf_gcc/release/lib_postProcessor.a | src/esp32s3/lib_postProcessor.a|
|api/api/lib/xtensa_esp32s3/xtensa_esp32s3_elf_gcc/release/lib_bmv080.a | src/esp32s3/lib_bmv080.a|
|api/api/lib/arm_cortex_m0plus/xarm_none_eabi_gcc/release/lib_postProcessor.a | src/cortex-m0plus/lib_postProcessor.a|
|api/api/lib/arm_cortex_m0plus/arm_none_eabi_gcc/release/lib_bmv080.a | src/cortex-m0plus/lib_bmv080.a|
|api/api/lib/arm_cortex_m33f/xarm_none_eabi_gcc/release/lib_postProcessor.a | src/cortex-m33/lib_postProcessor.a|
|api/api/lib/arm_cortex_m33f/arm_none_eabi_gcc/release/lib_bmv080.a | src/cortex-m33/lib_bmv080.a|
|api/api/lib/arm_cortex_m4/xarm_none_eabi_gcc/release/lib_postProcessor.a | src/cortex-m4/lib_postProcessor.a|
|api/api/lib/arm_cortex_m4/arm_none_eabi_gcc/release/lib_bmv080.a | src/cortex-m4/lib_bmv080.a|
|api/api/lib/arm_cortex_m4f/xarm_none_eabi_gcc/release/lib_postProcessor.a | src/cortex-m4f/lib_postProcessor.a|
|api/api/lib/arm_cortex_m4f/arm_none_eabi_gcc/release/lib_bmv080.a | src/cortex-m4f/lib_bmv080.a|

## BMV080 Board Limitations

The SparkFun BMV080 Arduino Library only works with the following SparkFun boards:

* [IoT RedBoard - ESP32](https://www.sparkfun.com/sparkfun-iot-redboard-esp32-development-board.html)
* [Thing Plus - ESP32 WROOM (USB-C)](https://www.sparkfun.com/sparkfun-thing-plus-esp32-wroom-usb-c.html)
* [Thing Plus - ESP32-S2 WROOM](https://www.sparkfun.com/sparkfun-thing-plus-esp32-s2-wroom.html)
* [Thing Plus - RA6M5](https://www.sparkfun.com/sparkfun-thing-plus-ra6m5.html)

Now that we have our library and board add-on installed, we can start experimenting with the breakout board. For the scope of this tutorial, we will highlight the examples to get started. From there we will be able to build our own custom code to integrate the development board into a project.
