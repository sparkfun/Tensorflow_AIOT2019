SparkFun Low-Power Machine Learning Examples
============================================

<p align="center" valign="middle">
   <img src="https://cdn.sparkfun.com/assets/custom_pages/3/3/4/dark-logo-red-flame.png"  width=200>  
   <img src="https://www.gstatic.com/devrel-devsite/prod/v0ee3aab4746d30f0d189bec7de9a20f1b6a1e49e000167a7abfdd73e499fffdc/tensorflow/images/lockup.svg"  width=300>   
</p>

<img src="https://cdn.sparkfun.com//assets/parts/1/3/5/6/7/15170-SparkFun_Edge_Development_Board_-_Apollo3_Blue-01a.jpg"  align="right" width=300> 

This repository contains examples that demonstrate the use of [TensorFlow Lite](https://www.tensorflow.org/lite/) based machine learning executing on the [SparkFun Edge Development](https://www.sparkfun.com/products/15170) board. The examples are designed for use within the Arduino development environment, enabling rapid setup and deployment of the examples.

The examples contained in this repository make use of the variety of sensors available on the SparkFun Edge Development board to show the modern capabilities of machine learning executing on a low-power microcontroller-based system.

The following examples are included in the repository:
* micro_speech - Using the on-board microphone to detect a spoken keyword
* person_detection - Using an attached camera to detect the presence of a person in an image. 
* magic_wand - Using the on-board accelerometer to detect gestures (movement of the breakout board) 

Hardware
---------
To run the examples, the following hardware is required:
* [SparkFun Edge Development breakout board](https://www.sparkfun.com/products/15170)
* [Himax CMOS Imaging Camera – HM01B0](https://www.sparkfun.com/products/15570)
* [SparkFun Serial Basic Breakout](https://www.sparkfun.com/products/14050) or [SparkFun Serial Basic Breakout USB-C](https://www.sparkfun.com/products/15096)
* [USB-A to micro-B cable](https://www.sparkfun.com/products/10215) or a cable to connect the Serial Basic to the development computer.

Getting Started
----------------

### Hardware
* Plug USB cable into computer
* Connect CH340C adapter to USB cable
* Plug in Edge board to adpater

### Software
* Install [Arduino](https://www.arduino.cc/en/Main/Software)
* Install SparkFun Apollo3 Arduino Core
  * Add the SparkFun boards ```.json``` file to Arduino board manager URLs
    * Open Arduino preferences (File->Preferences)
    * Copy ```https://raw.githubusercontent.com/sparkfun/Arduino_Boards/master/IDE_Board_Manager/package_sparkfun_index.json```
    * Paste in the ```Additional Boards Manager URLs:``` field
  * Install via Arduino Boards Manager  
    * Open the Boards Manager (Tools->Board->Boards Manager)
    * Search for ```apollo3```
    * Click ```install```
* Install library dependencies
  * Open the Arduino Library Manager (Sketch->Inlude Library->Manage Libraries)
  * ```Arduino_TensorFlowLite``` Arduino library
    * Search for ```Arduino_TensorFlowLite```
    * Install the top result using the version ```Version 1.15.0-ALPHA``` (**not** the *precompiled* option)
  * ```SparkFun Himax HM01B0 Camera``` library
    * Search for ```SparkFun Himax HM01B0 Camera```
    * Install ```v0.0.1```
* Download (or clone) this repo to favorite location
* Open Arduino
* Open an example from this repo through Arduino by clicking on a ```.ino``` file in one of the example directories
  * ```micro_speech```
* Select the ```SparkFun Edge``` board (Tools->Board under 'SparkFun Apollo3')
* Select the proper port to connect with the baord (Tools->Port)
* Change the **Bootloader** from *Ambiq Secure Bootloader (Default)* to *SparkFun Variable Loader (Enable w/ Artemis Bootloader)* (Tools->Bootloader)
  * (Your boards have received the upgraded bootloader already)
* Change the ```SVL Baud Rate``` from *921600* to *460800*

### Upload
* Compile with the ```Verify``` button (checkmark symbol)
* Upload with the ```Upload``` button (arrow symbol)
  * If uploading fails try lowring the bootloader baud rate

### Serial Monitor
* Open the Serial Monitor by clicking on the magnifying glass icon (top right) or (Tools->Serial Monitor)