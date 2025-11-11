# Lab 9 Pendulum I

## :dart: Task 4 – System Analysis

--------

The pendulum you just work on can be considered as a **second order system**. 

The tap action can be considered as an **impulse input** .

<img src="Pic/pen_model.png" width="650">

Where
- $m = 0.038 \mathrm{kg}$ is the mass.
- $g = 9.81 \mathrm{m/s^2}$ is the gravitational constant
- $\phi$ (unit: rad) is the pendulum offset angle.
> **Note:** When discussing transfer functions, angular quantities are always expressed in radians (rad), not degrees. Their conversion is:

$$\phi_{\text{rad}} = \theta_{\text{deg}} \times \frac{\pi}{180}$$

