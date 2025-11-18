# Lab 10 Pendulum II 

## :dart: Task 2 – Fine-adjust Physics Parameter (Individual)

---
### 📌 Task 2.1 Fine-adjust Physics Parameter (Individual)

You have calculated the physics parameters from the last lab.
- $l$: pendulum length (unit: m)
- $b$: friction parameter (unit: N·m·s/rad)

The pendulum length $l$ is fixed. But the friction parameter $b$ will vary a little if you swing (realease) at different degrees.

This task requires you to fine-adjust the friction parameter $b$ based on the recorded data.

To do so, plot these on on the same figure:
* **Pendulum Offset Angle (Deg) versus Time (s)**, using your experimental data.<br>
  In addition, shift your time data, such as your releasing exactly happens at 0 second.
* **The theoretical Exponential decay in Deg:**
  
$$A_{\text{init}} e^{-\zeta \omega_n t} = A_{\text{init}} e^{-\frac{b}{2 m l^2} t}$$

   where:
   - $$A_{\text{init}}$$ is the **initial angle (in degrees)** at the moment of release, inspect from your experimental data.
   - $A_{\text{init}}$ cannot be exactly 120.0 Deg in practice due to human error.
   - Set $l = 0.271$
   - Set $b = 0.001$

Once plotted, you may find the peaks of two traces are not well aligned.<br>
Fine-adjust your $b$ value in a small range until they are well aligned in a few beginning peaks. You don't need to care about the tailing portion.

| This is my example plot | 
|---------------------|
| <img src="Pic/pendulum_plot_F25.png" width="600"> | 

