# Lab 8 Filter Design

## :dart: Task 1 – Noisy Input

In Electrical Engineering, filters are used to selectively pass or attenuate specific frequency components of a signal. 

A common application of filters is dealing with signals affected by low-frequency or high-frequency noise. 

We will use Analog Discovery 2 to create signals with low frequency noise.

---
### 📌 Task 1.1 Wavegen Setup
Connect Analog Discovery 2 with your computer.

Open up **Wavegen.**

In Signal Type, click the gearbox to add a new customized signal:

```java
0.5*sin(50*X) + 0.1*sin(1000*X)
```

Untick ``Normalize``

Then click ``Generate``, Once you observe such graph, click `save`.

Then go back to the main page of Wavegen, set as follows.

| Setting   | Value              |
| --------- | ------------------ |
| Type      | Your custom signal |
| Frequency | 1 Hz               |
| Amplitude | 2 V                |
| Offset    | 0 V                |
| Symmetry  | 50 %               |

By doing so, you set up such signal:

$$x(t) = \sin(50t)+0.2\sin(1000t)$$



