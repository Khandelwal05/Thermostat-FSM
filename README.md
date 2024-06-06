# Thermostat-FSM
Welcome to the Thermostat-FSM repository, a project on Finite State Machine(FSM) and utilizing Tkinter library. The project involves designing a device that can detect temperature of a physical system and execute specific actions to maintain the system's temperature close to desired setpoint.

The Thermostat operates by monitoring the temperature of the system which is user input in this project. In the project, When the temperature exceeds a set threshold, eg 20 degree celcius , it indicates that the system is becoming hot. In response, the thermostat enters in a cooling mode by showing the message. Conversely, if the temperature falls below the threshold temperature, signaling that the system is becoming cold, Now the thermostat enters in heating mode by showing the message of thermostat is heating. Whereas if the temperature of the System is threshold temperature then the thermostat shows the message that thermostat is off.

This repository contains the code of this project.

## Features
+ Temperature Input: Users can input their desired temperature.
+ Heating Mode: Activates if the input temperature is below 20°C.
+ Cooling Mode: Activates if the input temperature is above 25°C.
+ Off Mode: The thermostat turns off when the input temperature is within the range of 20°C to 25°C, or when the "Turn off" button is pressed.
+ Visual Indicator: Displays the current state of the thermostat using text and a colored oval (grey for off, red for heating, and blue for cooling).

## Installation
To run this project, you need to have Python installed on your system. This project uses Tkinter, which is included with Python standard libraries.

1 Clone the repository or download the source code files. <br/>
2 Navigate to the directory containing the source code files.


## Dependecy required
```
pip install tkinter
```
