Wifi-Pixels
===========
Overview
~~~~~~~~
.. image:: /images/wifi_pixel/WifiPixels_Top.jpg

WifiPixels are 16 addressable RGB LED's that can be controlled via WIFI or even connected to the internet. It uses the popular ESP8266 Wifi unit that is compatible with the Arduino IDE.

.. image:: /images/wifi_pixel/WifiPixel_Buttons.jpg
 :width: 200
.. image:: /images/wifi_pixel/WifiPixels_Back.jpg
 :width: 200
.. image:: /images/wifi_pixel/WifiPixels_Back2.jpg
 :width: 200


Installation and Configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Connecting a FTDI-compatible USB to Serial programmer
-----------------------------------------------------
=============== ======================
WifiPixels Pins Serial Programmer Pins
=============== ======================
GND             GND
VIN             5V
RX              TX
TX              RX
=============== ======================


Using WifiPixels with Arduino IDE
---------------------------------
To use WifiPixels with Arduino the ESP8266 board needs to be added to the board manager. Installation instructions are available form the `Official Arduino/ESP8266 codebase <https://github.com/esp8266/Arduino#installing-with-boards-manager>`_

Putting the board into Boot-Loading mode
----------------------------------------
To put the device in boot-loader mode hold the BOOT button down and press the RESET button. The RED status led should stay on at half brightness indicating that the device is in Boot-loader mode.

Uploading Arduino Code
----------------------
From the board selector make sure to select the "Generic ESP8266 board" and the correct Serial port number(Programmers Serial Port). With the board in Boot-Loader mode, code can be uploaded to the device in the normal Arduino way by pressing the "Upload" button.

Adafruit has done an amazing job with documenting the ESP8266 Wifi units, `this link shows how to upload firmware <https://learn.adafruit.com/adafruit-huzzah-esp8266-breakout/overview>`_ and the other firmware options that are available.




Software
~~~~~~~~

Standard WifiPixel Firmware - [https://github.com/Protoneer/WifiPixels GitHub-WifiPixels]

Compatible Libraries
--------------------
* `Arduino Port for ESP8266 Wifi units <https://github.com/esp8266/Arduino>`_
* `NeoPixel <https://github.com/Makuna/NeoPixelBus>`_
* `PubSubClient - MQTT <https://github.com/Imroy/pubsubclient>`_



Hardware
~~~~~~~~
Version 1.10
------------
* Initial Version 
* 16 x WS2812B RGB Addressable Led's
* ESP8266 Wifi Unit compatible with Adafruit's ESP8266 Huzzah breakout