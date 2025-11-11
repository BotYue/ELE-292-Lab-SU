# Lab 9 Pendulum I

## :dart: Task 2 – Obtain Impulse Response

---
### 📌 Task 1.1 Tap and Record

Let your Arduino continuously print the real-time voltage from your assigned Analog pin to the Serial Monitor.

Do not add any `delay()` function inside your `loop()` function.

Now, tap the end of the pendulum to make it swing. This can be treated as an impulse input $A\delta(t)$ with some unknown amplitude (A).

* Make sure your pendulum is steady in the downward position before tapping.
* Make your pendulum’s first swing angle reach about 40 Degrees.
* Clear the Serial Monitor about 2–5 seconds before tapping. This helps you capture some initial-time data without recording an unnecessarily long time.
* After the pendulum comes to rest (no longer moving), unplug the USB cable to stop the Serial Monitor recording.

Once finished, open the **Serial Monitor** and select all data (`Ctrl + A`), then copy it (`Ctrl + C`).
Open Notepad (Windows) or TextEditor (Mac), and paste (`Ctrl + V`) the data into a new empty file.

Sometimes the first few lines may appear corrupted or contain buffer noise—simply delete those lines.
Finally, **save the file as a `.txt` file** using **UTF-8 encoding**.


