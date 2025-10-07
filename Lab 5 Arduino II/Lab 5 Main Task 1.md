# Lab 5 Arduino II

The 5 continues the introduction on Arduino basics, with emphasis on I/O.

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

* Use `Wavegen` in Analog Discovery to provide 5 V DC to the joystick. 
* Use `Scope Channel 1` in Analog Discovery to measure the voltage (**VRX**) for X-position of the joystick. 
* Use `Scope Channel 2` in Analog Discovery to measure the voltage (**VRY**) for Y-position of the joystick. 
* Ensure all grounds are properly connected, including:
   * both `Scope Channel` negative pins,
   * Analog Discovery Ground `↓`
   * joystick Ground

> [!NOTE]  
> You have completed multiple labs already. This time you are expected to handle the wiring **by yourself**.
> 
> No detailed pin-to-pin connection will be provided.

> [!TIP]  
> If you have too many ground wires, organize them to the blue rail of your breadboard.

### 📌 Task 1.2 Scope Reading

Configue your **Wavegen** to provide 5 V DC.

Open your **Scope**, 
* Change the Mode from **Repeated** to **Screen**
* Use 1 s/div or 2 s/div for Time Base
* Make sure both Channels are ticked.

Move the joystick in different directions, observe and understand the voltage.

* You may need to adjust the Channel Offset and Range to observe the full signal.
