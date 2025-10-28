# Lab 7 Sine & Bode

## :dart: Task 3 – Auto Obtain Bode

In this task, we will use the **[Network Analyzer](https://en.wikipedia.org/wiki/Network_analyzer_(electrical))** tool to automatically obtain a Bode magnitude plot for the circuit system.

The WaveForms of Analog Discovery includes a network analyzer tool. <br> To open it, click the **Network** icon on the welcome page.

<img src="Pic/netAys_welcome.png" width="300">

------

### 📌 Task 3.1 Automatically Frequency Sweep

Configure your Network Analyze as such:

<img src="Pic/netAys.png" width="800">

**Top Panel**:
* Start: 1 Hz; Stop 1 kHz
* Steps: 51 or more
* Source: Wavegen C1; Mode: Constant
* Amplitude: 5 V; Offset: 0 V
* Scale: Logarithmic

**Right Panel**:
* Magnitude only
* Channel 1 only
* Others as default  

After completing the configuration, click **Run** to start.

You will see it starts the analysis: Step 1/51; Step 2/51; Step 3/51; ...

After a while, it will finish all analysis and show a Bode plot.

#### :pencil2:  Report Item 3-a

Provide the screenshot of the display of your Bode. Include device Serial Number in the screenshot.

------

Export your Bode data as `.csv` for later use.

Use Notepad/TextEditor to double check your saved `.csv`. Make sure there are 51 lines of data (suppose set Steps as 51 in Network Analyzer)

### ✅ Check Point 2 — Bode in Network Analyzer

Show to your instructor/TA.

