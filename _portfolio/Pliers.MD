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




# The Design 

The purpose of this design was to function like a regular pair of needle nose pliers. The design was kept simple to show the capabilities of printing in place 3D printing and multi-material 3D printers. The two plier handles are printed using PLA. These were relatively easy to model in CAD as they resemble what real pliers look like. The spring component on this design is made of TPU. This allows the material to bend without breaking while also remaining strong enough to return the jaw of the pliers to the open position when not in use. The spring component was the trickiest part of this project because it is very difficult to create a working model in CAD that can open and close due to the limitations of the CAD software. To overcome this problem, I confirmed the spring would fit each handle individually using CAD, and then 3D printed multiple sizes of the spring to determine which would fit best. Once I had found the best size for the spring in this design, I could 3D print the whole design using print in place techniques on a multi-material 3D printer. 


# Specs 

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
   

# Print Settings 
1. Load the desired syringe into its appropriate holder mounts. Ensure that the syringe is locked into the hole for the tip of the syringe. Additionally, verify that the back of the syringe is snugly fit into the back mount and that the plunger is slotted into its respective hole piece.  
2. Plug in the power supply to provide power to the system. The LED should turn yellow.
3. To begin operation, press buttons to move the lead screw in either direction. In doing so, the LED should turn green.
4. To stop the syringe pump, press down the limit switch. This will immediately stop all movement of the system, and the LED will turn red. 
5. To begin movement again, release the limit switch and follow step #3 to begin operation again.
6. Once syringe is fully dispensed, stop operation and replace syringe using protocol of step #1. 
7. When completely finished with operation, unplug the power supply and store in a safe location. 


# CAD Model




{% include gallery caption="" %} 
