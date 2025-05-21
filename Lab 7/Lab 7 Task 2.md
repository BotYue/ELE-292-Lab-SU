# ELE 292 Lab 7: Filters

---
## :wrench: Task 2 – Low-Pass Filter

Low-pass filters reduce high-frequency components.

### :test_tube: Problem

Design a **series RC low-pass filter** to reject the noise term `0.2 sin(1000x)`.

**Constraints**:
- Capacitors: `220 nF` or `22 nF`
- Resistors: > `100 Ω`, use E6-series: `10, 15, 22, 33, 47, 68 × 10^x`

---

### :straight_ruler: Step 1 – Rough Pick by Bode Plot

Transfer function of RC low-pass filter:

```
H(s) = 1 / (RC) / (s + 1 / (RC))
```

---

### :pencil: Report Item 2-a

- Write the **cut-off frequency expression** \( f_c = \frac{1}{2\pi RC} \)
- Estimate cut-off range so:
  - `50 rad/s` (main signal) is on flat part
  - `1000 rad/s` (noise) is on drop-off part

---

### :notebook: Report Item 2-b

- List **at least 3** combinations of R and C that meet the design and constraints

---

### :computer: Step 2 – Test in Simulation (Python)

Use `scipy.signal.lsim()` to simulate.

---

### :bar_chart: Report Item 2-c

- Plot responses for all 3 RC combinations from Item 2-b
- Show input and output signals
- Code + Plot (3 figures)
- Select and justify the **best RC combination**

---

### :electric_plug: Step 3 – Test in Real Circuit

- Build circuit with chosen RC
- Use Wavegen to generate `sin(50x) + 0.2 sin(1000x)`
- Open Scope and FFT

---

### :camera: Report Item 2-d

- Screenshot of Scope and FFT (show both input & output)
- Make sure **local time is visible**
- In Scope: High-frequency noise should be **reduced**
- In FFT: Secondary peak should be **much lower**

:white_check_mark: **Check Point 2**

