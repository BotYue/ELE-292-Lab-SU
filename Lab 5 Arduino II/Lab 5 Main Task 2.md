# Lab 5 Arduino II

## :dart: Task 2 – Joystick with Arduino

### 📌 Task 2.1 Circuit Setup

You have studied the characteristics of joystick analog reading. Now we will combine it with Arduino.

Get:

* one KY-023 analog joystick
* one Adafruit ItsyBitsy M0 Express

<img src="Pic/joystick.png" width="300">

**Connection Requirement:**

* Use `VHI` in Arduino to provide 5 V DC to the joystick. 
* Use one Analog input pin to measure the voltage (**VRX**) for X-position of the joystick. 
* Use another Analog input pin to measure the voltage (**VRY**) for Y-position of the joystick. 
* Ensure Arduino `G` is connected to the joystick Ground

### 📌 Task 2.2 Arduino Code

Write Arduino Code to
* Read the voltages (**VRX**, **VRY**)from both analog input pins
* Print out both voltages via Serial Monitor

> [!TIP]
> You can re-visit the Lab 4 Main Task 3 code to understand how to obtain pin voltage and print.

#### :pencil2:  Report Item 2-a
Open the Serial Monitor. 

* Make sure your joystick is in **Center position**. Un-click “AutoScrolling”. Copy 10 consecutive output lines and paste them below.
```text
<paste your 10 lines here>
```
* Make sure your joystick is in **Rightmost position**. Un-click “AutoScrolling”. Copy 10 consecutive output lines and paste them below. 
```text
<paste your 10 lines here>
```

