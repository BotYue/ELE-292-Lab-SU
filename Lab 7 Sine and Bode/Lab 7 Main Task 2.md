# Lab 7 Sine & Bode

## :dart: Task 2 – Manually Obtain Bode

In this task, we will use the **Wavegen** and **Scope** tools to collect a large number of input–output data pairs from the circuit. 

Using the collected data, we will then manually create a Bode Magnitude plot for the circuit system.

------

### 📌 Task 2.1 Manually Frequency Sweep

**Input Signal is setup by Wavegen setup:**
| Setting   | Value |
| --------- | ----- |
| Type |  Sine     |
| Frequency  |   To be determined (denoted as $f$)  |
| Amplitude |   5 V    |
| Offset    |   0 V    |
| Symmetry    |   50 %    |
| Phase    |   0    |

In such setting, your input signal will be 

$$5\sin(2\pi f t)$$ 

Now, start your data collecting: 

* Set input frequency $f$ at different values.
* For each selected frequency $f$, measure the amplitude of corresponding output signal using the **Scope**.
* To get a complete Bode plot, you need to sweep over many freqs across multiple decades.

> [!TIP]
> As you learned in ELE 251, a Sine signal passing thru a system will retain its frequency.
> 
> So, there is a quick way to configure the Time-Axis of your Scope for clear reading:
> 
> Simply set **“Time-Base”** in Scope to match to the **“Period”** in the Wavegen. 

---
#### :pencil2:  Report Item 2-a

Measure the output amplitude (V) at these freqs in Table.

Then calculate the corresponding Magnitude (dB) for each input–output data pairs:

| **Freq (Hz)** | **Input Amplitude (V)** | **Output Amplitude (V)** | **Magnitude (dB)** |
| :-----------: | :------------------------: | :--------------------------: | :----------------: |
|       1       |            5                |                              |                    |
|       2       |            5                |                              |                    |
|       5       |            5                |                              |                    |
|       8       |            5                |                              |                    |
|       10      |            5                |                              |                    |
|       20      |            5                |                              |                    |
|       25      |            5                |                              |                    |
|       30      |            5                |                              |                    |
|       40      |            5                |                              |                    |
|       50      |            5                |                              |                    |
|       60      |            5                |                              |                    |
|       70      |            5                |                              |                    |
|       80      |            5                |                              |                    |
|       90      |            5                |                              |                    |
|      100      |            5                |                              |                    |
|      200      |            5                |                              |                    |
|      500      |            5                |                              |                    |
|      800      |            5                |                              |                    |
|      1000     |            5                |                              |                    |


---
> [!NOTE]
> Always record experiment data in 3 or more [significant digits (figures)](https://en.wikipedia.org/wiki/Significant_figures)!

> [!Note]
> $\text{Magnitude (dB)} = 20 \log_{10}\left(\frac{V_{\text{out}}}{V_{\text{in}}}\right)$
>
> In Python, $\log_{10}$ is `np.log10()`

> [!Note]
> If one single table is too long in display, you can split in multiple tables

------

### 📌 Task 2.2 Plot as Bode

Based on your table result, plot the Bode using this code piece.

```python

freq_manual = [1, 2, 5, 8, 10, 20, 25, 30, 40, 50, 60, 70, 80, 90, 100, 200, 500, 800, 1000]
mag_manual = [] 
# enter your Magnitude (dB) into this array

plt.semilogx(freq_manual, mag_manual, '-o', label="Manual Frequency Sweep")
plt.xlabel("Frequency (Hz)")
plt.ylabel("Magnitude (dB)")
plt.title("Bode Magnitude Plot")
plt.grid(which="both", linestyle="--", linewidth=0.5)
```

#### :pencil2:  Report Item 2-b

Show both Python code and generated plot in the report. 

If you have an outlier data point in Bode plot, go back to the experiment and re-check.

### ✅ Check Point 1 — Table and Plot

Show to your instructor/TA.

