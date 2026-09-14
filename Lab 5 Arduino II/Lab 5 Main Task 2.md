# Lab 5 Arduino II

## :dart: Task 2 – Transition from Analog Discovery to Arduino



### 📌 Task 2.1 Connection

In this task, we will use the Arduino as a "simple scope" and perform the similar measurement.

- [ ] You still need the Analog Discovery, but now it only acts as a DC power supply.
- [ ] Move the measurement from Analog Discovery Channel 1/2 pins to the analog input pins of Arduino (Adafruit ItsyBitsy M0 Express).
<br> In other words, use 2 analog input pins of Arduino to read Vrx, Vry in joystick.
- [ ] Ensure the 3 things sharing the same grounds: Analog Discovery, Joystick, Arduino board.

### 📌 Task 2.2 Code

Write your Arduino code:
- [ ] Use serial port baud rate 9600
- [ ] Continuously read data from two analog pins, convert raw data to voltage
- [ ] Continuously print two voltages to the serial port.
- [ ] delay 200 ms in main loop

If you have no clue in coding, [← Back to Lab 4 Task 3](../Lab%204%20Arduino%20I/Lab%204%20Main%20Task%203.md) and re-cap. The code should be in a similar style.

#### :pencil2:  Report Item 2-a
Provide your full code in Jupyter Notebook.
<br> Format: use the "Markdown" (text) cell, use triple grave accents as a fenced block. Use c as the language tag.

-----

### 📌 Task 2.3 Serial Monitor Reading

Once code is successfully running.

Perform the same experiment as Task 1 today. But now record data from your Arduino Serial Monitor.


#### :pencil2:  Report Item 2-b

Always record experiment data in 3 digits after decimal point. (this can be set by Arduino code)

| Joystick Direction |  VRX Voltage   |  VRY Voltage   |
| :----------------- | :--------------------: | :--------------------: |
| Center (initial)           |        ?? V        |         ?? V        |
| Move Left          |  ?? V|         ??  V     |
| Move Rightmost          |  ?? V|         ??  V     |
| Move Upmost            |   ??   V   | ?? V|
| Move Downmost          |    ??  V     | ?? V|

--------------

### 📌 Task 2.4 Serial Plotter

Keep your Arduino running. Now open Serial Plotter.

The Serial Plotter is like a simplest scope.

Move your joystick around and see what is going on with the Serial Plotter.


#### :pencil2:  Report Item 2-b

Provide a screenshot of your Serial Plotter that correspond to the your joystick movements.


