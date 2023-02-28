---
title: "Multi-Material Pliers Project"
excerpt: "These pliers show the capabilities of multi-material printing with print in place techniques"
header:
  image: assets/img/Syring e Pump Pic 1.jpg
  teaser: assets/img/Syring e Pump Pic 1.jpg
gallery:
  - image_path: assets/img/Syring e Pump Pic 2.jpg
  - image_path: assets/img/Syring e Pump Pic 3.jpg
  - image_path: assets/img/Syring e Pump Pic 5.jpg
   
---

# Purpose

This project was to show the capabilities of modern 3D printers to be able to print in place designs. This means the 3D printer can print parts that rotate, hinge, or slide with other parts on a design without any manual assembly required. This has allowed companies to create revolutionary parts that would otherwise be impossible to create. Furthermore, the use of a multi-material 3D printer can take this process to the next level. A design can now be printed in place without any manual assembly needed and multiple types of filaments can be used. 

This project is an example of how a design can be leveraged to use print in place techniques along with a multi-material 3D printer. The pliers were able to be printed on a regular 3D printer in multiple pieces due to the simplicity of the CAD design. A more complex design would have been very difficult to print in multiple pieces, with varying types of filaments, and still achieve accurate clearance. This same design is capable of being printed at one time with all components already assembled using print in place techniques. If done correctly, the pliers would still open and close like normal, and the TPU spring would adhere to the PLA pliers while remaining fully operational. This is just one example of how print in place 3D printing can build designs that would otherwise be impossible. 




# Features

* **Adjustable Flow Rate.** The flow rate of the fluid being pushed through the syringe pumps can also be easily changed so that this syringe pump may be used to administer a wide variety of drugs to patients. The flow rate can range from 0.012–300 mL/min.
* **Compatible with Multiple Syringe Sizes** This syringe pump can hold a 5mL syringe and a 20mL syringe. Both syringes can be run individually or at the same time. 
* **Minimal User Input** The syringe pump requires minimal user input in order to function. The user must load and unload the syringes before after after each use. The user must also start and stop the machine. The syringe pump will automatically stop once the syringe is empty. There is also a LED to warn the user when the pump is running, when the pump is stopped, and when the pump is out of fluid.


# Off the Shelf Materials Required 

* 200 mm lead screw with 2 mm pitch and 2 mm lead
* 1/4" x 8mm Flexible Coupling
* 200 mm linear rod with 8 mm diameter
* LM8UU Linear bearing for 8 mm diameter rod
* 2040 Aluminum Extrusion 1' Length
* Nema 17 Stepper Motor
* MEAN WELL RQ-65D AC-DC Power Supply Quad Output 5V 12V 24V 12V 4 Amp
* Arduino Uno
* A4988 Stepper Driver
* Small Breadboard
* Panel Mount Latching Push Buttons
* Limit Switch
* RGB Common Cathode LED
   
# 3D Printed Materials Required 

* Motor Mount
* Electrical Components Enclosure
* Electrical Components Enclosure Lid 
* Rear Syringe Holder 
* Middle Syringe Holder
* Front Syringe Holder 

# How To Operate Syringe Pump 
1. Load the desired syringe into its appropriate holder mounts. Ensure that the syringe is locked into the hole for the tip of the syringe. Additionally, verify that the back of the syringe is snugly fit into the back mount and that the plunger is slotted into its respective hole piece.  
2. Plug in the power supply to provide power to the system. The LED should turn yellow.
3. To begin operation, press buttons to move the lead screw in either direction. In doing so, the LED should turn green.
4. To stop the syringe pump, press down the limit switch. This will immediately stop all movement of the system, and the LED will turn red. 
5. To begin movement again, release the limit switch and follow step #3 to begin operation again.
6. Once syringe is fully dispensed, stop operation and replace syringe using protocol of step #1. 
7. When completely finished with operation, unplug the power supply and store in a safe location. 


# CAD Model

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH35dfcQT936092f0e430375ce53587cdfce?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


{% include gallery caption="" %} 
