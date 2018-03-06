# adaptivecruisecontrol
Acc using the LPC 2148 controller board with code written in C language in KEIL and simulated in Proteus 

ACC is an optional control system for vehicles that automatically adjusts the vehicle speed to
maintain a safe distance from vehicles ahead. Control system consists of distance sensors like
ultrasonic, radar. Following image provide an overview for ACC.
Figure 1: Overview of Adaptive Cruise Control
User control settings varies depending upon manufacturer, still basic functionalities are as follows:
1) Set max speed to be maintained.
2) Set minimum distance to be allowed with that speed.
3) Start ACC mode
4) Stop ACC mode
5) Store set parameters

I MPLEMENTATION : :
In this project ACC demonstration is done using Photo diode sensor to measure distance and included all
above basic features using tactile switches.
Figure 3: Switches arrangement for demonstration
Operation:
 Press SW1 to go to speed and distance setting mode
 Using SW2 select parameter to select (Even press – Speed selected, Odd press – Distance
selected)
 Using SW3 and SW4 for increment and decrement selected parameters respectively
 Press SW1 again will ask for ACC starting confirmation.
[Note: Set data gets stored at this stage]
 Press SW1 again and ACC will start
[Note: During ACC mode speed will vary according distance between vehicles, this speed
variation is just displayed on LCD and PWM is also generated accordingly]
 Press SW1 to switch off ACC mode if turned ON.
Constraints:
 Speed can be set is range between (40-80 Kmph) and distance (1-10m).
[Note: these are not to the scale]
 If speed falls below 40Kmph ACC mode switched off with 3 beep indications.
[Note: Each key stroke is provided with one beep stroke]
Feature:
 Set values are stored in external EEPROM chip and are recalled during starting ACC mode.
 Per Speed change beep is provide to notify driver.
Following are components used:
1) LPC2148 development board
2) Photo diode sensor
3) UART to USB converter
4) Buzzer
5) LCD
6) EEPROM IC

