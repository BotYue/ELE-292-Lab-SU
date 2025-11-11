# Lab 9 Pendulum I

## :dart: Task 2 – Obtain Impulse Response

---
### 📌 Task 1.1 Tap and Record

##### 🧷 Step 1: Configure Arduino code
Let your Arduino continuously print the real-time voltage from your assigned analog pin to the Serial Monitor.

Use the following print format so that each line includes both a **timestamp** and the **voltage** value:

```c
Serial.print(millis());         // Print time in milliseconds
Serial.print(", ");
Serial.println(your_voltage, 3);
// your_voltage is a variable name
// Print voltage with 3 decimal places
```

- Do not add any `delay()` function inside your `loop()` function. We should let Arduino to sample as fast as possible.

- Do not include any extra text or units (such as `"V"`) in the print functions. Extra characters will make the data file harder to process later.

---
##### 🧷  Step 2: Tap your pendulum

Now, tap the end of the pendulum to make it swing. This can be treated as an impulse input $A\delta(t)$ with some unknown amplitude $A$

* Make sure your pendulum is steady in the downward position before tapping.
* Make your pendulum’s first swing angle reach about 40 Degrees.
* Clear the Serial Monitor about 2–5 seconds before tapping. This helps you capture some initial-time data without recording an unnecessarily long time.
* After the pendulum comes to rest (no longer moving), quickly unplug the USB cable to stop the Serial Monitor recording.


https://github.com/user-attachments/assets/43410443-7dfd-4b92-a2ab-d84c2f34f4f9




---
##### 🧷  Step 3: Export and load data

Once finished, open the **Serial Monitor** and select all data (`Ctrl + A`), then copy it (`Ctrl + C`).
Open Notepad (Windows) or TextEdit (Mac), and paste (`Ctrl + V`) the data into a new empty file.

* Make sure your editor is in Plain Text mode. <br>(pay extra attention if on Mac. Mac TextEdit may defaultly set in Rich Text, not in Plain Text)
* Sometimes the first line or last line may appear as buffer lines, you can check and delete them.
  
Finally, save the file as a `.txt` file using UTF-8 encoding.

> [!IMPORTANT]
> You should not use Arduino IDE 2.x. Its Serial Monitor is poorly configured and cannot copy full data.
>
> [Lab 0 (Software Installation)](../Lab%200%20Software%20Installation/Lab%200%20Main%20Task%202.md) has complete guidance on installing Arduino Legacy IDE 1.8.X








