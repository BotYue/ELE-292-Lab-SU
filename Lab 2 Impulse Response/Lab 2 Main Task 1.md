# Lab 1 Impulse Response


## :dart: Task 1 – System Modeling
---

In this lab, we will use a **series RL** circuit to model a first-order system.

<img src="Pic/circuitdiagram.png" width="400"> 

We want to treat the circuit as a **System** . 

<img src="Pic/system1.png" width="400"> 

Thus we need to specify the following:

- **System Input:** We set the voltage of the source, $V_{in}(t)$, as the system input.  
  This can be set-up via Wavegen in the WaveForms.
- **System Output:** We set the voltage of the resistor $V_{R}(t)$ as the system output.  
  This can be measured via Scope in the WaveForms.

- **System Model:** To be calculated

### 📌 Task 2.1 Derive the System Model

Analyze the circuit, we have:

$$
V_{in}(t) =  V_L(t) + V_R(t) = L\frac{dI(t)}{dt} + I(t)R 
$$

$$
V_{out}(t) = V_R(t) = I(t)R
$$

Apply Laplace Transform:

$$
V_{in}(s) =  LsI(s) + I(s)R 
$$

$$
V_{out}(s) = I(s)R
$$

#### :pencil2:  Report Item 1-a
> **Find the system model in Laplace domain (known as Transfer Function):**
 
$$
\frac{V_{out}(s)}{V_{in}(s)} = ???
$$

*Note: For typing math answers in the report, you need to type the entire
equation and a short text description, not only type the part corresponding to ???.
This rubric applies to all math answers in the semester.*
