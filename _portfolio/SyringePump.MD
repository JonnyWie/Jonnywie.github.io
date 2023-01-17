---
title: "Syringe Pump Project"
excerpt: "This syringe pump will allow users to automate the process of injecting fluids at a relatively inexpensive cost"
header:
  image: assets/img/Syring e Pump Pic 1.jpg
  teaser: assets/img/Syring e Pump Pic 1.jpg
gallery:
  - image_path: assets/img/Syring e Pump Pic 2.jpg
  - image_path: assets/img/Syring e Pump Pic 3.jpg
  - image_path: assets/img/Syring e Pump Pic 5.jpg
   
---

# Purpose

The purpose of this project was to develop a syringe pump assembly that could automate the process of injecting fluids into a patient over a given period of time. This project was done through the use of off the shelf parts and custom made 3D printed parts. This drastically decreased the cost of making an adjutable syringe pump assembly. This project can be easily replicated for anybody else that is trying to improve this product or decrease cost as this project has done. 




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

# Arduino Uno Code

#include <AccelStepper.h>
AccelStepper stepperX(AccelStepper::DRIVER,11,12);

int red_LED_pin=7;
int green_LED_pin=6;
int CWbutton_pin=4;
int CCWbutton_pin=5;
int limitSwitch=2;

double bigSyringeFlowRate=0.00067925;
double smallSyringeFlowRate=.0.0002595;
double flowRate=10;// ml/min
float velocity=(flowRate/60)/bigSyringeFlowRate;// steps/sec

void setup() {
 stepperX.setMaxSpeed(1000); //steps/sec = Max:5 rev/sec
 stepperX.setSpeed(velocity); //50/200= 1/4 rev/sec= 4sec for 1 rev
 //stepperX.moveTo(400); //Moves 400 steps 

 pinMode(red_LED_pin,OUTPUT);
 pinMode(green_LED_pin,OUTPUT);
 pinMode(CWbutton_pin, INPUT_PULLUP);
 pinMode(CCWbutton_pin, INPUT_PULLUP);
 pinMode(limitSwitch, INPUT_PULLUP);
}

void loop() {

if (digitalRead(CWbutton_pin) == HIGH ){
  analogWrite(green_LED_pin, 150);
  analogWrite(red_LED_pin, 150);
 }

if(digitalRead(limitSwitch) == LOW){
  if (digitalRead(CWbutton_pin) == LOW ){
   analogWrite(green_LED_pin, 200);
   analogWrite(red_LED_pin, 0);
   stepperX.setSpeed(velocity);
   stepperX.runSpeed();
    //stepperX.run();
  }
}
 if(digitalRead(limitSwitch) == HIGH) {
  analogWrite(green_LED_pin,0);
  analogWrite(red_LED_pin,200);
 }
if (digitalRead(CCWbutton_pin) == LOW ){
    analogWrite(green_LED_pin, 200);
    analogWrite(red_LED_pin, 0);
    stepperX.setSpeed(-velocity);
    stepperX.runSpeed();
    }
}



