# Lab 6 Thermal System

## :dart: Task 3 System Analysis (Individual)

In this task, you will analyze the system based on the theoretical model in Task 1 and experimental data capture in Task 2..

### 📌 Task 3.1 Y-axis Parameter Estimation (Individual)

Based on your Task 2 data and plot, estimate the parameters related with Y-axis in:

$$T_{chip}(t)=\frac{bA}{a}(1-e^{-at})+T_{room}$$

#### :pencil2:  Report Item 3-a (Individual)

| **Parameter**                       | **Estimated Value** | 
|:--------------:|:------------------:|
| $T_{room}$ |                    |           |     
| $\frac{bA}{a}$ |                    |           |     

> [!TIP]
> You can use vertical lines on your Python plot [`plt.axhline()`](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.axhline.html) to visually fine-tune the parameter estimation.

### 📌 Task 3.2 Time Constant Estimation (Individual)

In this theoretical response equation,

$$T_{chip}(t)=\frac{bA}{a}(1-e^{-at})+T_{room}$$

You can see the Time Constant of the system is $a$ in the theoretical model.

First, make a **rough estimate** of the Time Constant value $a$.

Then, use the theoretical response equation, plugging your previously estimated parameters $T_{room}$ and $\frac{bA}{a}$, to **plot the theoretical response** on the same figure as your experimental data.

Next, fine-adjust the Time Constant value gradually until the theoretical response and the experimental data **visually overlap** as closely as possible.

#### :pencil2:  Report Item 3-b (Individual)
Indicate your final estimated Time Constant.

> [!NOTE]
> Time Constant has a unit

#### :pencil2:  Report Item 3-c (Individual)
Provide a single figure showing both the experimental data and the theoretical response (show both code and generated plot).

Plots should have proper title, legend, x/y axis labels, units.
