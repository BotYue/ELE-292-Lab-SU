# Lab 3 Step Response


## :dart: Task 2 – Obtain System Response
---
### 📌 Task 2.1 RC Circuit Setup

| **Circuit Diagram** | **Breadboard Pin** |
|---------------------|------------------------------|
| <img src="Pic/RCdiagram.png" width="380"> | <img src="Pic/breadboardRC.png" width="380"> |

**Components Used:**
- $R = 100~\mathrm{k}\Omega$ resistor 
- $L = 0.22~\mu\mathrm{F}$ capacitor

-------------
### 📌 Task 2.2 Input Setup
**Input Signal is setup by Wavegen setup:**
| Setting   | Value |
| --------- | ----- |
| Type |  Square     |
| Period  |    1 s   |
| Amplitude |   0.5 V    |
| Offset    |   0.5 V    |
| Symmetry    |   50 %    |
| Phase    |   0    |

This setting generates a unit step input $u(t)$, whose amplitude jumps from 0 V to 1 V.

---
### 📌 Task 2.3 Obtain Output
Run the Wavegen to generate the signal.

Run the Scope to measure the voltage across the capacitor.

Adjust the scope to get a clear, readable display. You should get **only 1 exponential increase** clearly in the display.
