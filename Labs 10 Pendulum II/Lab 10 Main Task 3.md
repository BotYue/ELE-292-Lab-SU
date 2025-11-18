# Lab 10 Pendulum II 

## :dart: Task 3 – System Modeling (Individual)

---
### 📌 Task 3.1 Linear & Nonlinear Models

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

Now, we convert the **Approximated Linear Model** into a state space representation.

Assume two state variables:

* $x_1(t) = \phi(t) \quad \text{(angle, in rad)}$
* $x_2(t) = \frac{d\phi(t)}{dt} \quad \text{(angular speed, in rad/s)}$
  
And we are in the **Zero-Input** case, so the matrices associated with $u(t)$ are both zero.

System Equations:

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
y(t) =
\begin{bmatrix}
1 & 0
\end{bmatrix}
\begin{bmatrix}
x_1(t) \\
x_2(t)
\end{bmatrix}
+
\begin{bmatrix}
0
\end{bmatrix}
u(t)
$$
```

Initial Conditions:

$$
\phi(t=0) = 120 \text{ Deg} =\frac{2\pi}{3} \text{ rad}, 
\qquad \dot{\phi}(t=0) = 0  \text{ rad/s}
$$

#### :pencil2:  Report Item 3-a

Fill the 2 × 2 state matrix $A$ in the state space model.

---
### 📌 Task 3.2 Visualize the Approximated Linear Model (Individual)

Once you have the $A$, $B$, $C$, $D$ matrices and initial conditions, <br>you can obtain the zero-input response of the system in `scipy` and plot it.

```python
from scipy import signal as sig
## Enter system matrices
A =
B =
C =
D =
## Enter initial conditions
phi_0 = ??            # initial angle
phi_dot_0 = ??        # initial angular velocity

t = np.linspace(???)
linear_system = sig.lti(A, B, C, D)
_, linear_system_response, _ = sig.lsim(linear_system, U=0, T=t, X0=[phi_0, phi_dot_0] )

plt.plot(t, linear_system_response/np.pi*180)
```

