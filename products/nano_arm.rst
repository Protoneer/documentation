Nano ARM
========
Overview
~~~~~~~~
.. image:: /images/nano_arm/NANO-ARM-Bottom1.jpg

We loved Arduino Nano's but always wanted a bit more performance and memory.

So we decided to create a Arduino Nano compatible board but with an upgrade micro-controller that is 
similar to an Arduino Zero.

.. image:: /images/nano_arm/NANO-ARM-Bottom2.jpg
 :width: 200
.. image:: /images/nano_arm/NANO-ARM-Top1.jpg
 :width: 200
.. image:: /images/nano_arm/NANO-ARM-Top2.jpg
 :width: 200



The NANO-ARM has the following features

* Runs at 48MHz (Atmel SAMD21)
* 256KB FLASH Memory
* 32KB RAM 
* Pin compatible with Arduino Nano but runs at 3.3V
* SAMD21 micro-controller same as used on a Arduino Zero's.
* Built in USB
* Arduino Zero bootloader pre-loaded.
* 20 I/O pins with 5 extra pins that can be used for I2C/SPI or I/O
* 6 Analog Pins(ADC) with 12-bit resolution (4096 resolution point vs Arduino Uno's 1024)
* 1 Digital to Analog(DAC) pin with 10-bit resolution.
* Designed and Manufacture in New Zealand

Availability, Update Notifications and Forums
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Available online : `Protoneer Shop <http://stores.ebay.com/Protoneer>`_

Hardware
~~~~~~~~
Schematic
---------
.. image:: /images/nano_arm/Nano-ARM-schematic.png

Power Management
----------------
3.3V Regulation is done with a NCP551 Low-Dropout Voltage regulator.

* Input Voltage 12V max
* Output currnet 150mA
* Very low quiescent current of 4.0uA(Typical)

Datasheets
----------
* `SAMD21G18 <http://www.microchip.com/wwwproducts/en/ATsamd21g18>`_



Software
~~~~~~~~
Arduino IDE
-----------
Programming a NANO-ARM
______________________
NANO-ARM's are 100% Arduino Zero compatible and the programming process is the same.

This is the guide as provided with the Arduino Zero : `Programming Guide <https://www.arduino.cc/en/Guide/ArduinoZero>`_

Pin Mappings
____________
Pin mappings for Arduino Zero / NANO-ARM is avaialable from the Arduino Github repository at:
`https://github.com/arduino/ArduinoCore-samd/blob/master/variants/arduino_zero/variant.cpp <https://github.com/arduino/ArduinoCore-samd/blob/master/variants/arduino_zero/variant.cpp>`_

Serial Ports
____________
In Arduino the following has changed:

* Serial Object is connected to Pin D0 and D1
* SerialUSB Object is connected to the USB serial port that is visible to computers.

Versions
~~~~~~~~
Version 1.02
------------
Added USB test pads for testing. QFN chip

Version 1.01
------------
Initial release.