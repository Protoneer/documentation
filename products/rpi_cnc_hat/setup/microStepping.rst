Micro-Stepping
--------------

.. Tip:: 
    Micro Stepping increasing accuracy at the cost of speed and torque.

    Increasing the micro stepping will reduce stepper motor jitter.

Jumpers number are indicated as below:

.. image:: /images/rpi_cnc_hat/RPi-CNC-Jumper-Numbers.jpg

In the tables below High indicates that a Jumper is inserted and Low indicates that no jumper is inserted.

`Pololu A4988 <https://www.pololu.com/product/1182>`_

========  ========  ========  ====================  
Jumper 1  Jumper 2  Jumper 3  Microstep Resolution
========  ========  ========  ====================
Low       Low       Low	      Full step
High 	  Low	    Low	      1/2 step
Low       High      Low	      1/4 step
High	  High	    Low	      1/8 step
High	  High	    High	  1/16 step
========  ========  ========  ====================


`Pololu DRV8825 <https://www.pololu.com/product/2133>`_

========  ========  ========  ====================  
Jumper 1  Jumper 2  Jumper 3  Microstep Resolution
========  ========  ========  ====================
Low       Low       Low       Full step
High      Low       Low       1/2 step
Low       High      Low       1/4 step
High      High      Low       1/8 step
Low       Low       High      1/16 step
High      Low       High      1/32 step
Low       High      High      1/32 step
High      High      High      1/32 step
========  ========  ========  ====================



* Stepper Coils indicated with A and B

.. image:: /images/rpi_cnc_hat/RPI-CNC-260-StepperConfig.jpg
    :width: 200
