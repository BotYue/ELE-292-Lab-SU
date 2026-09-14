# Lab 5 Arduino II

The Lab 5 continues the introduction on Arduino basics, with emphasis on I/O.

Recall the pinout of **Adafruit ItsyBitsy M0 Express**,

https://github.com/adafruit/Adafruit-ItsyBitsy-M0-PCB/blob/master/Adafruit%20ItsyBitsy%20M0%20pinout.pdf 


* **Analog input**: All pins labeled with **AIN** can do analog input. We recommend use from **Pin A1** to **Pin A5**.
* **True analog output**: **Pin A0** is the only true analog output pin. It is labeled by **VOUT**
* **PWM output**: Most pins labeled with **D** can do PWM output. We recommend use from **Pin 9** to **Pin 13** 

---

## :dart: Task 1 – Joystick Analog Reading

### 📌 Task 1.1 Circuit Setup

Task 1 requires you to analyze the joystick analog readings using the Analog Discovery 2. This will prepare you for the Task 2 Arduino set-up.

**Components Used:**

* one KY-023 analog joystick
* one workbench with Analog Discovery 2
* No need for Arduino in Task 1
----------
<img src="Pic/joystick.png" width="300">

The **VRX** and **VRY** pins output analog voltages for the X- and Y-axis positions.

 The **SW** pin is a digital push-button input. We won’t use it.

 Internally, **VRX** and **VRY** are driven by simple potentiometer-based voltage divider.

----------
**Connection Requirement:**

* Use `Supplies` (Pin V+) in Analog Discovery to provide 1 V DC to the joystick. 
* Use `Scope Channel 1` in Analog Discovery to measure the voltage (**VRX**) for X-position of the joystick. 
* Use `Scope Channel 2` in Analog Discovery to measure the voltage (**VRY**) for Y-position of the joystick. 
* Ensure all grounds are connected together, including:
   * both `Scope Channel` negative pins,
   * Analog Discovery Ground `↓`
   * joystick Ground

> [!NOTE]  
> You have completed multiple labs already. This time you are expected to handle the wiring **by yourself**.

> [!TIP]  
> If you have too many ground wires, organize them to the blue rail of your breadboard.

### 📌 Task 1.2 Scope Reading

In "WaveForms" -> "Supllies" to provide 1 V DC at the V+ pin.

Open your **Scope**, 
* Change the Mode from **Repeated** to **Screen**
* Use 2 s/div or 1 s/div for Time Base
* Make sure both Channels are enabled.

Move the joystick in different directions, observe and understand the voltage.

* You may need to adjust the Channel Offset and Range to observe the full signal.
* Must set the same offset for 2 channels, same range to 2 channels, overwise may create confusion in reading.
---
Based on the joystick direction in the picture, measure and fill the table.

<img src="Pic/joystickorit.png" width="400">

#### :pencil2:  Report Item 1-a

Always record experiment data in 3 or more significant digits (figures).

| Joystick Direction |  VRX Voltage   |  VRY Voltage   |
| :----------------- | :--------------------: | :--------------------: |
| Center (initial)             |         ≈ 0.500 V        |         ≈ 0.500 V        |
| Move Left          |  ?? V|         ??  V     |
| Move Rightmost          |  ?? V|         ??  V     |
| Move Upmost            |   ??   V   | ?? V|
| Move Downmost          |    ??  V     | ?? V|

#### :pencil2:  Report Item 1-b

Provide a screenshot of the display of your Scope with measurement on it.<br>
You don't need 8 screenshots for 8 measurements in 1-a, just one screenshot that matches one of the eight measurements in table.

---
### 📌 Task 1.3 Record 2-Channel Data

In Wavegen Scope, use the regular Voltage-Time Scope and the new X-Y Scope at the same.

X-Y Scope can be found on top tab -> "+XY".

Play with your joystick, until you can draw an interesting pattern on your X-Y scope.

Feel free to explore whatever interesting pattern that you can draw!

|Here is an example that I draw. It is a reversed L|
|---|
|<img src="Pic/XYscope.png" width="800">|


#### :pencil2:  Report Item 1-c

Provide the screenshot of the display of your Scope. Showing the Voltage-Time Scope and the new X-Y Scope at the same.

> [!NOTE]
> Include the local time and device Serial Number (Discovery 2 C SN: ..) in the screenshot.
> Use computer-built-in app to screenshot. Not use your phone camera to take pictures.


#### :pencil2:  Report Item 1-d (Individual)

Use text to clearly describe the sequence of joystick movements you used to produce the pattern shown on the 1-c.

---
### ✅ Check Point 1 — Scope Display and Movement








