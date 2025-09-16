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

  
#### :pencil2:  Report Item 2-a
Provide a clear photo of your breadboard connection. 

It will better to compress the photo to less than 1 MB before pasting into Notebook. Any online image compressor should work.

-------------
### 📌 Task 2.2 Input Setup
**Input Signal is setup by Wavegen setup:**
| Setting   | Value |
| --------- | ----- |
| Type |  Square     |
| Period  |    1 s   |
| Amplitude |   1 V    |
| Offset    |   1 V    |
| Symmetry    |   50 %    |
| Phase    |   0    |

This setting generates a step input $2u(t)$, whose amplitude jumps from 0 V to 2 V.

---
### 📌 Task 2.3 Obtain Output
Run the Wavegen to generate the signal.

Run the Scope to measure the voltage across the capacitor.

Adjust the scope to get a clear, readable display. You should get **only 1 exponential increase** clearly in the display.
  
> [!TIP]
> 1. the signal is not stable, adjust the **Trigger Level** until the display locks.  
> 2. If the signal looks too compressed or stretched in Time axis, adjust the **Time-Base**.  
> 3. If the signal looks too compressed or stretched in Voltage axis, adjust the **Channel 1-Range**.  
> 4. If the entire signal is off-screen (up or below), adjust the **Channel 1-Offset**.

-------------
### 📌 Task 2.4 Measure

We will measure a special metric known as **Time Constant**.

Recall in Task 1, you final result for step response of first order system may look like:


$$
\mathrm{Output} = K \bigl(1 - e^{-\frac{1}{\tau}t}\bigr)u(t)
$$

**$K$ (called statedy-state value)** and **$\tau$ (called Time Constant)** are two constants that depend on **input amplitude $A$** and the **system model parameters $R$ and $C$**.

* **When $t=\infty$:**
  $\mathrm{Output}=K$,
  (reaches a steady-state value).

* **When $t=\tau$:**
  $\mathrm{Output}=K\bigl(1-e^{-1}\bigr)\approx 0.632\cdot K$,
  (63.2% of the steady-state value).

To measure them graphically, we need to use the **Cursor Tool** as these steps:

