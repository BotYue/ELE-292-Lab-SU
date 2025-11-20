# Lab 10 Pendulum II 

## :dart: Task 3 – System Modeling (Individual)

---
### 📌 Task 3.1 Linear & NonLinear Models

In this experiment, the system can be modeled by a differential equation with initial conditions.

##### 🧷 i) NonLinear Model

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
\begin{bmatrix}\dot{x}_1(t) \\ \dot{x}_2(t)\end{bmatrix} =
\begin{bmatrix}? & ? \\? & ?\end{bmatrix}
\begin{bmatrix}x_1(t) \\x_2(t)\end{bmatrix}+
\begin{bmatrix}0 \\0\end{bmatrix} u(t)
$$
```

```math
$$
y(t) =
\begin{bmatrix}1 & 0\end{bmatrix}
\begin{bmatrix}x_1(t) \\ x_2(t) \end{bmatrix}+
\begin{bmatrix}0\end{bmatrix}
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

*note: remove the ` ```math ` ` ``` ` fence if you copy matrix from Github to Jupyter Notebook Markdown.*

---
### 📌 Task 3.2 Visualize the Approximated Linear Model (Individual)

Once you have the $A$, $B$, $C$, $D$ matrices and initial conditions, <br>you can obtain the zero-input response of the system in `scipy` and plot it.

```python
from scipy import signal as sig
## Enter system matrices
A =
B = np.array([[0.0], [0.0]])
C = np.array([[1.0, 0.0]])
D = np.array([[0.0]]) 
## Enter initial conditions
phi_0 = ??            # initial angle (rad), better replaced by your own angle
phi_dot_0 = ??        # initial angular velocity (rad/s)

t = np.linspace(???)
linear_system = sig.lti(A, B, C, D)
_, linear_system_response, _ = sig.lsim(linear_system, U=0, T=t, X0=[phi_0, phi_dot_0] )
linear_system_response_deg = np.rad2deg(linear_system_response)

plt.plot(t, linear_system_response_deg)
```

> [!NOTE]
> Type every numbers in A, B, C, D as float numbers, not int numbers. Otherwise `Scipy` may fail to generate response.

#### :pencil2:  Report Item 3-b (Individual)

In Python, plot the two signals on the same figure:
* **Experimental:** Pendulum Offset Angle (Deg) versus Time (s), using the experimental signal from the Task 2 (which has been shifted to 0-seconds release).
* **Theoretical:** Pendulum Offset Angle (Deg) versus Time (s), based on the approximated linear model

Show code and figure. The figure should have proper title, x/y axis labels, units.

-------
### ✅ Check Point 2 — Python Plot

Show to your instructor/TA.

---
### 📌 Task 3.3 Visualize the NonLinear Model (Individual)

For the nonlinear model, you can obtain its response by solving a Diff equation using the Runge–Kutta (RK45) method via `scipy`.

The system equation can be re-arranged as:

$$\frac{d^{2}\phi(t)}{dt^{2}} = -\frac{b}{m l^{2}} \frac{d\phi(t)}{dt} - \frac{g}{l} \sin(\phi(t))$$


```python
from scipy.integrate import solve_ivp
## Enter initial conditions
phi_0 = ??            # initial angle (rad), better replaced by your own angle
phi_dot_0 = ??        # initial angular velocity (rad/s)

def nonlinear_system(t, y):
  phi_t, dphi_dt = y
  dphi_dt_dt = ???  ## enter the diff equation
  return [dphi_dt, dphi_dt_dt]

t_span = (0, 15)
t_eval = np.linspace(0, 15, 1000)
X0 = [phi_0 , phi_dot_0]

diffq_solution = solve_ivp(nonlinear_system, t_span, X0, t_eval=t_eval, method='RK45')
nonlinear_system_time = diffq_solution.t
nonlinear_system_response_deg = np.rad2deg(diffq_solution.y[0])

plt.plot(nonlinear_system_time, nonlinear_system_response_deg)
```
#### :pencil2:  Report Item 3-c (Individual)

In Python, plot the two signals on the same figure:
* **Experimental:** Pendulum Offset Angle (Deg) versus Time (s), using the experimental signal from the Task 2 (which has been shifted to 0-seconds release).
* **Theoretical:** Pendulum Offset Angle (Deg) versus Time (s), based on the nonlinear model

Show code and figure. The figure should have proper title, x/y axis labels, units.

---
### 📌 Task 3.4 Model Comparison

#### :pencil2:  Report Item 3-d (Individual)

Based on your 3-b & 3-c figures, briefly comment on which one (nonlinear model/approximated linear model) gives better results. in 3 or more sentences.

You can refer to the [Small-Angle Approximation](https://en.wikipedia.org/wiki/Small-angle_approximation) and think about the reason.








