# Lab 8 Filter Design

## :dart: Task 3 – Active Low-pass Filter

Keep the Wavegen input from previous tasks.

For the previous input signal, we can apply a filter to make it less noisy. 

From a linear system view, this means passing the **input** $x(t) = \sin(50t) + 0.2\sin(1000t)$ through a **filter system**,<br> so that the main signal amplitude **in output** remains nearly unchanged, while the noise part **in output** gets attenuated.

In the filter design process, we select a **cutoff frequency** that lies between the two frequency components of the signal

* $f_{\text{cutoff}}\ (\text{Hz}) > 50/(2\pi) \approx 7.96~\text{Hz}$
* $f_{\text{cutoff}}\ (\text{Hz}) < 1000/(2\pi) \approx 159.15~\text{Hz}$

A practical choice for $f_{\text{cutoff}}$ will be around 15–30 Hz, nearly a decade left from 159.15 Hz.

---
### 📌 Task 3.1 Filter Design Objective

In Task 3, you need to design a filter that satisfies both requirements:

**Requirement 1.** cutoff frequency $f_{\text{cutoff}}$ will be around 15–30 Hz<br>
**Requirement 2.** DC Gain, $H(s)$, to be 2.

### 📌 Task 3.2 Filter Circuit

For circuit, we will build an **active low-pass filter** consists of two main stages:

* **RC Stage:** Uses an **RC network** ($R_1, C_1$) to set the desired cutoff frequency
* **Gain Stage:** Since the RC network naturally reduces the signal amplitude, we use an **Op-Amp network** to restore the signal amplitude. In other words, make $DC\ Gain = 1$.

<img src="Pic/filter_diagram.png" width="600">

The Transfer Function of this entire circuit is:

$$H(s) = \frac{V_{\text{out}}(s)}{V_{\text{in}}(s)}= \frac{sR_1C_1}{1 + sR_1C_1}\cdot (1 + \dfrac{R_f}{R_g})$$

* $R_1 = 47 \mathrm{k}\Omega$
* $C_1 = 220 \mathrm{nF}$

This gives $f_{\text{cutoff}}\ (\text{Hz}) = 1/(2\pi \cdot 47E3 \cdot 220E-9) =15.39 Hz$, satisfying the Task 3.1 requirement.

The DC Gain of $H(s)$ is

$$|H(0)|=\frac{0\cdot R_1C_1}{1 + 0\cdot R_1C_1}\cdot (1 + \dfrac{R_f}{R_g})=
