Gabi Acosta and Dylan Robichaud. 
Title of Project: Embedded Microcontroller Alarm Clock Date: 03/10/23
Summary of behavior: change !!!
The user is allowed to set the alarm date and time using their PC keyboard and serial monitor. The current time and the alarm date and time are compared, if they are equal, the alarmState is set to ON. When the alarmState is ON, the buzzer, IR sensor, LDR sensor and servo motor are all activated. If the LDR sensor detects too little light in the room, the RGB LED is turned ON. When the alarm is activated, the servo motor is turned on to remove the blanket off the bed. The servo motor stays on for 20 straight seconds then it stops moving. The IR sensor has to detect motion for 20 straight seconds, after the alarm is deactived and the buzzer stops ringing.

List of Modules:
Alarm Clock System - This module calls the inital functions of the hardware components as well as the update functions. This module is the only system. This combines all the modules. This code was based from the textbook. 

Alarm - This modules initializes and activates the hardware components when the alarm time is set. The module also deactivates the alarm and the buzzzer. This code was partially written from scratch and the textbook. 

Date and Time - This allows the user to set the current date and time and the alarm date and time. It does this using the RTC peripheral. This code was based from the textbook. This code was influenced from the textbook. 

Display - This module programs the LCD display. It can clear the screen and set the cursor the screen. This code was based on the textbook code.


Ir Sensor - When the alarm is activated, the IR sensor is activated. To deactivate the alarm the IR sensor is programmed to detect 20 straight seconds of motion. If motion is not detected the IR sensor waits to detect motion. If motion is detected for less than 20 seconds then the time is restarted. This code was partially writted from scratch and online. 

LDR sensor - to detect if there is enough light in the room. The voltage of the LDR is used. IF the voltage read is less than 0.6V then the RGB led turns on. This code is based on the an exercise we did in Chapter 5. cahnge!!!

PC Serial Com - This module controls the PC monitor. The monitor is programmed to show the alarm state, the alarm time, the current date and time and available commands. The user is also able to set the current date and time and also the alarm time using the PC keyboard. This code was influenced by the textbook code.

RGB LED - When the LDR voltage detects less than 0.6V, the red LED, blue LED and green LED are turned on by sending a high to each lead of the LED

Servo motor - When the alarmState = ON, the servo motor turns on and removes the blanket from the bed. After twenty seconds the servo motor turns off. This code was based from scratch.

Siren - When the alarmState is activated, the buzzer is sent a low signal. The buzzer begins ringing. The buzzer only stops ringing when the alarmState is deactivated. This code was based from the textbook.

User Interface - The user interface activates the alarm if the current time is equal to the alarm time. It also shows the current time and the alarm time on the LCD display. There is also a welcome message that directs the user to the PC serial monitor.  This code was influenced from online and written from scratch. 

List of Hardware components coneected to the Nucleo board and their pins
Buzzer - PC8
Servo Motor - PF9
IR Sensor Receptor - PD14
RGB LED - redLED - PA7 blueLED - PA6 greenLED - PA5
LDR Sensor - PC3
LCD Display:
Pin 4 - PF9
Pin 6 - PF12
Pin 7 - PG9
Pin 8 - PG14
Pin 9 - PF15
Pin 10 - PE13
Pin 11 - PF14
Pin 12 - PE11
Pin 13 - PE9
Pin 14 - PF13

A description of the tests you performed on the system, and the results.

Any other details that will help the reader understand your code.
