# Lab 2 Impulse Response


## :dart: Task 2 – Obtain System Response
---

### 📌 Task 2.1 RL Circuit Setup

| **Circuit Diagram** | **Breadboard Pin** |
|---------------------|------------------------------|
| <img src="Pic/circuitdiagram.png" width="380"> | <img src="Pic/realcircuit.png" width="380"> |

**Components:**
- $R = 22~\Omega$ resistor, (color code: red red black gold)
- $L = 1~\mathrm{mH}$ inductor  

-------------
### 📌 Task 2.2 Input Setup
**Input Signal is setup by Wavegen setup:**
| Setting   | Value |
| --------- | ----- |
| Type |  Square     |
| Period  |    1 ms   |
| Amplitude |   1 V    |
| Offset    |   1 V    |
| Symmetry    |   1 %    |
| Phase    |   0    |

For such setting, the area of this signal is,

$$
2~\mathrm{V} \times 1~\mathrm{ms} \times 1\mathrm{percent} 
= 2 \times 10^{-3}~\mathrm{V \cdot s} \times 0.01
= 2 \times 10^{-5}~\mathrm{V \cdot s}
$$

This signal can be approximately treated as an **impulse** with the such area (scalar value):

$$
A = 2 \times 10^{-5}
$$

Thus, input signal will be $2 \times 10^{-5}\delta(t)$

-------------
### 📌 Task 2.3 Obtain Output
Run the Wavegen to generate the signal.

Run the Scope to measure the voltage across the resistor.

Adjust the scope to get a clear, readable display. You should get **2~5 exponential decays** clearly in the display.
  
**🔧 Scope Adjustment Tip**  
- If the signal is not stable, adjust the **Trigger Level** until the display locks.  
- If the signal looks too compressed or stretched in Time axis, adjust the **Time-Base**.  
- If the signal looks too compressed or stretched in Voltage axis, adjust the **Channel 1-Range**.  
- If the entire signal is off-screen (up or below), adjust the **Channel 1-Offset**.

#### :pencil2:  Report Item 2-a

Provide the screenshot of the display of your Scope. 

> Include the local time and device Serial Number (Discovery 2 C SN: ..) in the screenshot.

> Use computer-built-in app to screenshot. Not use your phone camera to take pictures.

-------------
### 📌 Task 2.4 Measure

Use either the Quick Memasure tool or Cursor tool to measure the peak voltagef the output signal.

#### :pencil2:  Report Item 2-b

| **Tool**        | ?? |
|-----------------|----|
| **Peak Voltage**| ?? |

*Always record experiment data in 3 or more [significant digits (figures)](https://en.wikipedia.org/wiki/Significant_figures)!*  

---------

### ✅ Check Point 1 — Scope Display and Peak Voltage


Show to your instructor/TA.

Keep the circuit and WaveForms software. We still need them in the next task.
