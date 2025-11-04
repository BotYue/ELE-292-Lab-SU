# Lab 8 Filter Design

## :dart: Task 3 – Active Low-pass Filter

Keep the Wavegen input from previous tasks.

---
### 📌 Task 3.1 Filter Introduction

For the previous input signal, we can design an **active low-pass filter** to make it less noisy. 

From a linear system view, this means passing the **input** $x(t) = \sin(50t) + 0.2\sin(1000t)$ through a **filter system**,<br> so that the main signal amplitude **in output** remains nearly unchanged, while the noise part **in output** gets attenuated.

In the filter design process, we select a **cutoff frequency** that lies between the two frequency components of the signal

* $f_{\text{cutoff}}\ (\text{Hz}) > 50/(2\pi) \approx 7.96~\text{Hz}$
* $f_{\text{cutoff}}\ (\text{Hz}) < 1000/(2\pi) \approx 159.15~\text{Hz}$

A practical choice for $f_{\text{cutoff}}$ will be around 15–30 Hz, nearly a decade left from 159.15 Hz.

### 📌 Task 3.2 Filter Circuit

For circuit, we will build an **active low-pass filter** consists of two main stages:

* **Filter Stage:** Uses an **RC network** ($R_1, C_1$) to set the desired cutoff frequency
* **Gain Stage:** Since the RC network naturally reduces the signal amplitude, we use an **Op-Amp network** to restore the signal amplitude.

<img src="Pic/filter_diagram.png" width="600">

The Transfer Function of this entire circuit is:

$$H(s) = \frac{V_{\text{out}}(s)}{V_{\text{in}}(s)}= \frac{1}{1 + sR_1C_1}\cdot (1 + \dfrac{R_f}{R_g})$$
