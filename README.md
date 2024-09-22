# Arduino Robot Arm Project
This project demonstrates how to create a fully functional Arduino-controlled robotic arm, wirelessly operated and programmed using a custom-built Android application. The robot arm can be controlled manually or through predefined automated steps using Bluetooth communication with the Android app.

# Overview
This project includes everything needed to assemble, control, and customize the Arduino robot arm:

3D models for printing the robot parts
Circuit diagram for assembling the electronic components
Arduino code to control the servos and handle Bluetooth communication
Android app for wireless control and automation

# Features
Manual Control: Adjust each servo/axis using sliders on the Android app.
Automated Movement: Record multiple steps and have the arm repeat them in sequence.
Pause/Reset: Pause automatic actions or reset the recorded steps.
Speed Control: Adjust the speed of the servo motors directly from the app.

# Components Needed
3x MG996R Servo Motors (for the waist, shoulder, and elbow)
3x SG90 Micro Servo Motors (for the wrist and gripper)
Arduino Board (Uno, Mega, etc.)
HC-05 Bluetooth Module
5V 2A Power Supply
3D printed parts for the robot arm (files included in the repository)

# 3D Printing
All parts for the robotic arm were modeled using SolidWorks and are available as STL files. These can be printed with any standard 3D printer (tested on the Creality CR-10).

# Assembly
Assemble the robot arm step by step using the provided 3D-printed parts.
Use screws, bolts, and a rubber band (to assist the shoulder servo) for assembly.
Attach the servo motors in their respective positions (waist, shoulder, elbow, wrist, gripper).

# Circuit Diagram
The servos are connected to the digital pins of the Arduino, and the Bluetooth module is connected for communication with the Android app. Power the servos using an external 5V power supply (as Arduino cannot handle the current needed by all servos).

# Code
The Arduino code includes:

Bluetooth communication: Handles data received from the Android app.
Servo control: Allows manual control and automatic operation of the servos based on saved steps.
Speed control: Adjusts the speed of the servos through the app.
The code is structured to control each servo motor and store recorded steps for automatic playback.

Example Arduino Code Snippet:
#include <Servo.h>
#include <SoftwareSerial.h>

Servo servo01, servo02, servo03, servo04, servo05, servo06;
SoftwareSerial Bluetooth(3, 4);

void setup() {
  servo01.attach(5);
  servo02.attach(6);
  // Attach the remaining servos
  Bluetooth.begin(38400);
}

# Android App
The Android app, created using MIT App Inventor, allows:

Manual control of the robot arm using sliders for each axis.
Saving and running automated sequences of movements.
Controlling servo speed and resetting recorded steps.
The APK and project file for the app are included in the repository.

# Installation and Setup
Arduino IDE
Download and install the Arduino IDE.
Open the provided Arduino code (robot_arm.ino).
Upload the code to the Arduino board.

Android App
Download the APK file from the repository.
Install the app on your Android device.
Connect your smartphone to the HC-05 Bluetooth module on the robot.

Power Supply
Make sure to use an external 5V 2A power supply to power the servos as the Arduino cannot handle the current draw.

# © All rights reserved by Ghindă Vadim.

Instagram : https://www.instagram.com/ghinda_vadim/
Linkedin : https://www.linkedin.com/in/vadimghinda/
