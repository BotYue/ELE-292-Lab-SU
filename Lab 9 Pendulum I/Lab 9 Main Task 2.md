# Lab 9 Pendulum I

## :dart: Task 2 – Obtain Impulse Response

---
### 📌 Task 2.1 Tap and Record

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
##### 🧷  Step 3: Export data

Once finished, open the **Serial Monitor** and select all data (`Ctrl + A`), then copy it (`Ctrl + C`).
Open Notepad (Windows) or TextEdit (Mac), and paste (`Ctrl + V`) the data into a new empty file.

* Make sure your editor is in Plain Text mode. <br>(pay extra attention if on Mac. Mac TextEdit may defaultly set in Rich Text, not in Plain Text)
* Sometimes the first line or last line may appear as buffer lines, you can check and delete them.
  
Finally, save the file as a `.txt` file using UTF-8 encoding.

> [!IMPORTANT]
> You should not use Arduino IDE 2.x. Its Serial Monitor is poorly configured and cannot copy full data.
>
> [Lab 0 (Software Installation)](../Lab%200%20Software%20Installation/Lab%200%20Main%20Task%202.md) has complete guidance on installing Arduino Legacy IDE 1.8.X

---
### 📌 Task 2.2 Visualize Data in Python

Once you saved the .txt file, you can use Python to load and visualize the data.

We will use the same `pandas.read_csv()` function that we previously used for `.csv` files. Even though the file extension is `.txt`, the data are still in comma-separated format (`time,voltage`), so `read_csv()` works.

This is the simplease code that works:

```python
import pandas as pd

file_path = '???.txt' 
lab9_data = pd.read_csv(file_path, names=['Time', 'Voltage'])
print (lab9_data)
```

#### :pencil2:  Report Item 2-a

In Python, plot the **Pendulum Offset Angle (Deg)** versus **Time (s)** using your experimental data. 

Show code and figure. The figure should have proper title, x/y axis labels, units.

* Plot **Time (s)** on the x-axis.
  * If you used `millis()` in your Arduino code, your time data are in **milliseconds (ms)**.  
    Convert to seconds in Python by dividing by `1e3`:
  * If you used `micros()` in your Arduino code, your time data are in **microseconds (μs)**.  
    Convert to seconds in Python by dividing by `1e6`:
* Plot **Pendulum Offset Angle (Deg)** on the y-axis.
  * The offset angle is the recorded rotation angle you measure ($V_{out}$) relative to the downward position (180 deg, 1.65 V).
  * If you tap to right, the offset angle (Deg) is: $\frac{V_{out}-1.65}{3.3}\cdot 360$
  * if you tap to left, the offset angle (Deg) is: $-\frac{V_{out}-1.65}{3.3}\cdot 360$
  * 1.65 should be adjust to your actual downward voltage obtained in Task 1

-------
### ✅ Check Point 1 — Python Plot

Show to your instructor/TA.



