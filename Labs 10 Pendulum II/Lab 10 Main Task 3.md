# Lab 10 Pendulum II 

## :dart: Task 3 – System Modeling (Individual)

---
### 📌 Task 3.1 Linear & Nonlineary Models

In this experiment, the system can be modeled by a differential equation with initial conditions.

##### 🧷 i) Nonlinear Model

System Equation:

$$\frac{d^{2}\phi(t)}{dt^{2}} + \frac{b}{m l^{2}} \frac{d\phi(t)}{dt} + \frac{g}{l} \sin(\phi(t)) = 0$$

Initial Conditions:

$$
\phi(t=0) = 120 \text{ Deg} =\frac{2\pi}{3} \text{ rad}, 
\qquad \dot{\phi}(t=0) = 0  \text{ rad/s}
$$


##### 🧷 ii) Approximated Linear Model (using [Small-Angle Approximation](https://en.wikipedia.org/wiki/Small-angle_approximation) )

System Equation:

$$
\frac{d^{2}\phi(t)}{dt^{2}} + \frac{b}{m l^{2}} \frac{d\phi(t)}{dt} + \frac{g}{l} \phi(t) = 0
$$

Initial Conditions:

$$
\phi(t=0) = 120 \text{ Deg} =\frac{2\pi}{3} \text{ rad}, 
\qquad \dot{\phi}(t=0) = 0  \text{ rad/s}
$$

------
#### :pencil2:  Report Item 3-a
Convert the Approximated Linear Model into a state space representation.

Assume two state variables:

* $x_1(t) = \phi(t) \quad \text{(angle, in rad)}$
* $x_2(t) = \frac{d\phi(t)}{dt} \quad \text{(angular speed, in rad/s)}$

```math
$$
\begin{bmatrix}
\dot{x}_1(t) \\
\dot{x}_2(t)
\end{bmatrix}

=

\begin{bmatrix}
? & ? \\
? & ?
\end{bmatrix}
\begin{bmatrix}
x_1(t) \\
x_2(t)
\end{bmatrix}
+
\begin{bmatrix}
0 \\
0
\end{bmatrix} u(t)
$$
```

```math
$$
y =
\begin{bmatrix}
1 & 0
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2
\end{bmatrix}
+
\begin{bmatrix}
0
\end{bmatrix}
u(t)
$$
```







