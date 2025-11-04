# Lab 8 Filter Design

## :dart: Task 3 – Active Low-pass Filter

Keep the Wavegen input from previous tasks.

---
### 📌 Task 3.1 Filter Design
For the previous input signal, we can design an **active low-pass filter** to make it less noisy. 

From a linear system view, this means passing the **input** $x(t) = \sin(50t) + 0.2\sin(1000t)$ through a **filter system**,<br> so that the main signal amplitude **in output** remains nearly unchanged**, while the noise part **in output** gets attenuated.

In the filter design process, we select a **cutoff frequency** that lies between the two frequency components of the signal

* $f_{\text{cutoff}}\ (\text{Hz}) > 50/(2\pi) \approx 7.96~\text{Hz}$
* $f_{\text{cutoff}}\ (\text{Hz}) < 1000/(2\pi) \approx 159.15~\text{Hz}$

In RC-based first order filter, 

$$f_{\text{cutoff}}\ (\text{Hz})  = \frac{1}{2\pi R_1C_1}$$

Based on the components avaiable at lab bins, we choose

* $R_1 = 47 \mathrm{k}\Omega$
* $C_1 = 220 \mathrm{nF}$
