# Lab 6 Thermal System

## :dart: Task 1 –Introduction


In Lab6, we will study a **first order thermal system**.

Specifically, we will focus the **step response** of this system.

We will also continue to practice the usage of Analog Discovery and Arduino.


### 📌 Task 1.1 Pre Setup
> [!IMPORTANT]  
> you must do this first.

Many Arduino has previously uploaded code. We never know who uploaded what code on
it.

Connect USB to Arduino without any jump wires. 

Run this code first to erase the previously uploaded code.

After completion, unplug the USB.



### 📌 Task 1.2 Actual System

The actual system is this board named "Tmeperature Control":

<img src="Pic/boardsystem.png" width="300">

* The green resistor is the load to be heated.
* The chip under the green resistor is a temperature sensor.
* The half-cylinder item is a 2N7000 MOSFET and acts as a logic switch. The MOSFET
will be fully turned on if a gate signal is above 3 V.

	In this lab, we use a 3.3 V PWM signal as the gate signal to turn on MOSFET.
So the switch will be on when PWM signal is High, will be off when PWM is Zero.
* The +5 V DC is the voltage of the main circuit loop.

Overall, the board can be simply considered as such connection:
<img src="Pic/boardsystem.png" width="300">






