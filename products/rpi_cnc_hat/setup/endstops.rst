End Stops
=========

End Stops use normally-open push-button type switches. The End-stop socket shares a common ground that connects to each axis end-stop. The pins are pulled high by the micro controller's internal pull-ups and will activate the end-stop when the pin is connected to ground.

Endstops can also be doubled up in parallel.

.. image:: /images/rpi_cnc_hat/EndStopWiring.jpg
 :width: 200

.. image:: /images/rpi_cnc_hat/2xEndstops.png
    :width: 400


.. Hint::

    GRBL v0.9 setting :guilabel:`$21=1` activate hard-limits. 

    Setting :guilabel:`$22=1` activates the Homing functionality.

.. Note:: V2.51 Introduces End-stop and Probe line filters to prevent noise on the lines.
