# Lab 9 Pendulum I

## :dart: Task 4 – System Analysis

--------

The pendulum can be approximately considered as a **second order system**. 

The tap action can be considered as an **impulse input** .

<img src="Pic/pen_model.png" width="650">

Where,
- $m = 0.038 \mathrm{kg}$ is the mass.
- $g = 9.81 \mathrm{m/s^2}$ is the gravitational constant
- $\phi$ (unit: rad) is the pendulum offset angle.
> **Note:** When discussing transfer functions, angular quantities are always expressed in radians (rad), not degrees. Their conversion is:

$$\phi_{\text{rad}} = \theta_{\text{deg}} \times \frac{\pi}{180}$$

We also assume two are unknown,
- $b$: unknown friction parameter
- $l$: unknown pendulum length

---
Compare the denominator of pendulum system model:

$$\frac{...}{s^2+\frac{b}{m\cdot l^2}s+\frac{g}{l}}$$

Versus the standard 2nd order transfer function:

$$\frac{...}{s^2+2\zeta\omega_n s+\omega_n^2}$$

We can solve for the expression of unknowns in terms of $\zeta$ and $\omega_n$ as:

$$l = \dfrac{g}{\omega_n^2},
\qquad
b = \dfrac{2 \zeta m g^2}{\omega_n^3}$$
