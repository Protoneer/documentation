Quick Start
===========
Overview
--------
The Raspberry Pi CNC board is a simple board that plugs into a Raspberry Pi and turns a Raspberry Pi into a useful little CNC machine controller. (Credit to the GRBL, Arduino, Raspberry Pi and all the wonderful projects on the internet)

A basic understanding of the following is needed... (There are many tutorials online covering these topics):

Raspberry Pi systems
* Arduino Hardware / Serial Interfaces
* Basic computer skills
* GRBL g-code interpreter

What you will need to get started
---------------------------------
* Raspberry Pi CNC Board/Hat
* Raspberry Pi B+ / Raspberry Pi 2 / 3 / 4 (Raspberry Pi with 20x2 pin header) + accessories like screen, keyboard, mouse.....
* 8GB or Bigger Micro SD Card or bigger. (Internet connection to download the pre-configured Raspberry Pi Image)
* CNC Hardware - This will not be covered in this wiki but includes things like Stepper Motors+ Pololu Drivers, Linear rails and all the mechanical bits.

Download the pre-configured Raspberry Pi image
----------------------------------------------
Raspberry Pi's run a full blown Operating system from it's on board SD card. Pre-configured SD card images are available to speed up the setup process. For this project we created a new image that includes a bunch of applications that can interact with the Raspberry Pi CNC board.

Included software:

* Standard Raspberry Pi Image.
* bCNC : A python based user interface application for controlling GRBL Boards.
* CNC.js : A nodeJS web based interface for controlling GRBL boards.
* Added extras's : MiniCom,XRDP and NodeJS

To install the image follow the standard process as documented by the Raspberry Pi website : `Raspberry Pi - INSTALLING OPERATING SYSTEM IMAGES <https://www.raspberrypi.org/documentation/installation/installing-images/README.md>`_

Download the latest pre configured Raspberry Pi SD card images : :ref:`sd_image`

Install the Raspberry Pi CNC board while waiting for the download
-----------------------------------------------------------------
1. Start by attaching the copper spacers to the Raspberry Pi. Depending on the board there will be 3 or 4 spacers

.. image:: /images/rpi_cnc_hat/PiWithSpacersLoose.jpg

Do not over tighten the screws.

.. image:: /images/rpi_cnc_hat/PiWithSpacersInstalled.jpg

2. Plug the Raspberry Pi CNC board into the Raspberry Pi. The pin connector should be aligned properly.

.. image:: /images/rpi_cnc_hat/AlignConnector.jpg

When aligned the mounting holes connecting the Raspberry Pi CNC board should align with the spacers screw holes.

.. image:: /images/rpi_cnc_hat/AlignScrewHole.jpg

3. Screw the Raspberry Pi CNC board in place.

.. image:: /images/rpi_cnc_hat/PiScrewedIn.jpg

G-Code Senders
--------------

Command Line interface
######################
This might seem hard but it is actually the fastest way to get started.

Included with the Raspberry Pi image is a small command line app called `Minicom <https://en.wikipedia.org/wiki/Minicom>`_ . It's a capable Serial terminal application and will be used to connect to the GRBL from a terminal window.

1. Start by opening a new Terminal Window.
2. Open Minicom in setup mode.

.. image:: /images/rpi_cnc_hat/MinicomStart.png

3. Scroll down to "Serial port setup" with the arrow keys and press enter.
4. A Raspberry Pi's hardware serial port is linked to device "/dev/ttyAMA0" and GRBL works at a baud rate of "115200 8N1".

.. image:: /images/rpi_cnc_hat/Minicom_Raspberry_Pi_setup.png

5. Press enter to exit the "Serial port setup" menu and arrow down to "Save setup as dfl". Then down to exit to switch to command mode.
6. If all goes well you will get a window like this :

.. image:: /images/rpi_cnc_hat/Minicom_serial_command_line.png

7. To get a reaction from GRBL press "?". This will return the current machine position :

.. image:: /images/rpi_cnc_hat/Minicom_GRBL_talk.png

8. To exit from Minicom press "Ctrl+A" then "Z" then "Q" then Enter.


bCNC
#################
1. On the Raspberry Pi desktop there is a shortcut for bCNC. Double click on it to start bCNC.

.. image:: /images/rpi_cnc_hat/BCNC_Shortcut.png

2. Once bCNC has loaded it will open in an disconnected state like this :

.. image:: /images/rpi_cnc_hat/BCNC_Started.png

3. Click on the Open button to connect to GRBL :

.. image:: /images/rpi_cnc_hat/BCNC_Click_on_open.png

4. bCNC should now say Connected :

.. image:: /images/rpi_cnc_hat/BCNC_Connected.png

5. To move the machine around, click on the Control tab at the top and use the arrow buttons to move the machine around.

.. image:: /images/rpi_cnc_hat/BCNC_Send_Commands.png

This was a very quick introduction into using bCNC. For information on doing more advanced work refer to the `bCNC Wiki Page <https://github.com/vlachoudis/bCNC/wiki>`_

Playing with CNC.js
###################
CNC.js is a web-based interface for GRBL. It hosts a webpage on the Raspberry Pi that can be accessed from a browser by any computer that's on the same network as the Raspberry Pi.

1. To start the CNC.js service click on the CNC.js shortcut(Only do this once as it needs time to start-up) on the Raspberry Pi desktop.

.. image:: /images/rpi_cnc_hat/Cncjs_shortcut.png

2. A terminal window running the CNC.js server should pop-up and looks like this.

.. image:: /images/rpi_cnc_hat/Cncjs_terminal_window.png

3. You will need the IP of the Raspberry Pi to connect to CNC.js . The easiest way to do this is by running the ifconfig command. In my case my IP was 192.168.1.10

.. image:: /images/rpi_cnc_hat/GetIP.png

4. On a remote computer that is connected to the same local network as the Raspberry Pi open a Chrome Browser and in the address bar enter the Raspberry Pi's IP address with the port number of 8000 added at the end - "192.168.1.10:8000"

.. image:: /images/rpi_cnc_hat/Cncjs_link.png

5. Then all you need to do is open the hosted webpage.

.. image:: /images/rpi_cnc_hat/Cncjs_connecting_to_grbl.png

6. To move the machine, click on the arrow buttons on the right of the screen.

.. image:: /images/rpi_cnc_hat/Cncjs_moving_grbl.png

This was a very quick introduction into using CNC.js. For information on doing more advanced work refer to the `CNC.js website <http://cheton.github.io/cnc.js/>`_.

Links and extra reading
-----------------------
* :ref:`rpi_cnc_hat` - Electronic circuit that connects a Raspberry, GRBL , Stepper Drivers , Steppers.
* `Raspberry Pi <https://www.raspberrypi.org/>`_ - Small Credit Card size computer.
* `Arduino <http://arduino.cc/>`_ - Magic device that connects to sensors and computers.
* `GRBL <https://github.com/gnea/grbl>`_ - GCode Interpreter that runs on an Arduino(Atmel ATMEGA328) Micro-controller
* `bCNC <https://github.com/vlachoudis/bCNC/wiki>`_ - Python Based GCode sender that connects to GRBL
* `CNC <https://github.com/cheton/cnc>`_ - Web based GCode sender that connects to GRBL