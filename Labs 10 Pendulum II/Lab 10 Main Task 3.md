# Lab 10 Pendulum II 

## :dart: Task 3 – System Modeling (Individual)

---
### 📌 Task 3.1 Linear & Nonlineary Models

In this experiment, the system can be modeled by a differential equation with initial conditions.

##### 🧷 i) Nonlinear Model

System Equation:

$$\frac{d^{2}\phi(t)}{dt^{2}} + \frac{b}{m l^{2}} \frac{d\phi(t)}{dt} + \frac{g}{l} \sin(\phi(t)) = 0$$

Initial Conditions:

$$\phi(0) = 120^\circ = \frac{2\pi}{3} \text{ rad}, \quad
\frac{d\phi}{dt}(0) = 0 \text{ rad/s}$$

##### 🧷 ii) Approximated Linear Model (using [Small-Angle Approximation](https://en.wikipedia.org/wiki/Small-angle_approximation) )

System Equation:

$$
\frac{d^{2}\phi(t)}{dt^{2}} + \frac{b}{m l^{2}} \frac{d\phi(t)}{dt} + \frac{g}{l} \phi(t) = 0
$$

Initial Conditions:

$$
\phi(0) = 120^\circ = \frac{2\pi}{3} \text{ rad}, \quad
\frac{d\phi}{dt}(0) = 0 \text{ rad/s}
$$









