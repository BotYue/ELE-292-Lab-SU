# Lab 3 Step Response


## :dart: Task 3 – Visualize and Analyze Data
----------
### 📌 Task 3.1 Data into Python (Individual)

Same as the last lab. Export your Scope data as .csv. Then read it into Python.

### 📌 Task 3.2 Data Visualization (Individual)

In Jupyter Notebook, use Python to plot **on the same figure**:
1) the **experimental output signal** exported from Scope,
2) the **theoretical output signal** (1-b result with R, C, A values plugged in).

The experimental output can be plotted using the same approach as the last lab.

The theoretical output can be plotted by using 

```python
t_theo = np.linspace( , , )
V_theo = ... 
plt.plot(t_theo, V_theo, label="...")
```
> [!TIP]
> If their starting points no aligned, you can shift the Time-Axis of experimental output.
> 
> For example
> 
> ```plt.plot(my_data['Time (s)'] -2.7, my_data['Channel 1 (V)'])``` will shift left 2.7 seconds
> 
> ```plt.plot(my_data['Time (s)'] +3.1, my_data['Channel 1 (V)'])``` will shift right 3.1 seconds

#### :pencil2:  Report Item 3-a

Show both code and generated plot in the report. Use Python to display the plot of your Scope data. 

Plots should have proper title, legend, x/y axis labels, units.

---
### ✅ Check Point 2 — Python Plot
You may now disconnect and put away all hardware.  
- Return resistor, capacitor to their proper bins.  
- Place the blue workbench on the shelf in the correct order:  
  *(EECS 1–2, EECS 3–4, EECS 5–6, …)*  

----------
### 📌 Task 3.3 Data Analysis (Individual)

#### :pencil2:  Report Item 3-b

|        | **Answer** | 
|-----------------|----|
| **Experimental Time Constant**| ?? |
| **Theoretical Time Constant**| ?? |
| **Percent Error**| ?? |

> [!TIP]
>
> * **Experimental Time Constant:** Take the value in **Report Item 2-c**.
> * **Theoretical Time Constant:** Use the result from **Report Item 1-c**, compare it with the definition given in **Task 2.4**. Then substitute the component values from your circuit.
> * **Percent Error:** Compare Experimental Time Constant vs. Theoretical Time Constant.


