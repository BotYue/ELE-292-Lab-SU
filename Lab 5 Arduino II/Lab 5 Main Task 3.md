# Lab 5 Arduino II

## :dart: Task 3 – Joystick with Arduino

### 📌 Task 3.1 Circuit Setup

You have studied the characteristics of joystick analog reading. Now we will combine it with Arduino.

**Components Used:**

* one KY-023 analog joystick
* one Adafruit ItsyBitsy M0 Express
* No need for Analog Discovery 2

<img src="Pic/joystick.png" width="300">

**Connection Requirement:**

* Use `3V` in Arduino to provide 3.3 V DC to the joystick. 
* Use one Arduino Analog input pin to measure the voltage (**VRX**) for X-position of the joystick. 
* Use another Arduino Analog input pin to measure the voltage (**VRY**) for Y-position of the joystick. 
* Ensure Arduino `G` is connected to the joystick Ground

---
### 📌 Task 3.2 Arduino Code

Write Arduino Code to
* Read the voltages (**VRX**, **VRY**) from both analog input pins
* Print out both voltages via Serial Monitor

> [!TIP]
> You can re-visit the [Lab 4 Main Task 3](../Lab%204%20Arduino%20I/Lab%204%20Main%20Task%203.md) code to understand how to obtain pin voltage and print.

<img src="Pic/joystickorit.png" width="400">

#### :pencil2:  Report Item 3-a
Open the Serial Monitor. 

* Make sure your joystick is in **Upmost position**. Un-click “AutoScrolling”. Copy 5 consecutive output lines and paste them below.
```text
<paste your 5 lines here>
```
* Make sure your joystick is in **Rightmost position**. Un-click “AutoScrolling”. Copy 5 consecutive output lines and paste them below. 
```text
<paste your 5 lines here>
```

#### :pencil2:  Report Item 3-b

Provide your all Arduino code .

* Use the proper Markdown format: triple grave accents as a fenced block; `c` as the language tag. (introduced in [Lab 4 Main Task 3](../Lab%204%20Arduino%20I/Lab%204%20Main%20Task%203.md))
* Use clear, meaningful variable names in code

### ✅ Check Point 2 — Arduino Print Voltage

- Return components to their proper bins.
- Place the blue workbench on the shelf in the correct order:  
  *(EECS 1–2, EECS 3–4, EECS 5–6, …)*  







