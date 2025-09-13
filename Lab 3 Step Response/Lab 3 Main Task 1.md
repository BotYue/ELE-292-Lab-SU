# Lab 3 Step Response


## :dart: Task 1 – System Modeling
---

In this lab, we will use a **series RC** circuit to model a first-order system.

<img src="Pic/RCdiagram.png" width="400"> 

We want to treat the circuit as a **System** . 

<img src="Pic/system1.png" width="400"> 

- **System input:** $V_{in}(t)$ 
- **System output:** $V_{out}(t)=V_{C}(t)$ 
- **System model:** To be calculated

### 📌 Task 1.1 Derive the System Model (Individual)

Analyze the circuit, we have:

$$
V_{in}(t) =  V_C(t) + V_R(t) = \frac{1}{C}\int I(t)dt + I(t)R 
$$

$$
V_{out}(t) = V_C(t) = \frac{1}{C}\int i(t)dt
$$

Apply Laplace Transform:

$$
V_{in}(s) =  \frac{1}{C}\frac{I(s)}{s} + I(s)R 
$$

$$
V_{out}(s) = \frac{1}{C}\frac{I(s)}{s}
$$
