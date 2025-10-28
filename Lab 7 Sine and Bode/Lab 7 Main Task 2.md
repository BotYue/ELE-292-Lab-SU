# Lab 6 Sine & Bode

## :dart: Task 2 – Manually Obtain Bode

In this task, we will use the **Wavegen** and **Scope** tools to collect a large number of input–output data pairs from the circuit. 

Using the collected data, we will then manually create a Bode Magnitude plot for the circuit system.

------

### 📌 Task 2.1 Frequency Sweep

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
* To get a complete Bode plot, you need to sweep over many freqs in different decades.

> [!TIP]
> As you learned in ELE 251, a Sine signal passing thru a system will retain its frequency.
> 
> So, there is a quick way to configure the Time-Axis of your Scope for clear reading:
> 
> Simply set **“Time-Base”** in Scope to match to the **“Period”** in the Wavegen. 



