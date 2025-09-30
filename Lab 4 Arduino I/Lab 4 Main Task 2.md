# Lab 4 Arduino I

## :dart: Task 2 – Temperature sensor reading
### 📌 Task 2.1 Circuit Setup
**Component Used**

* One Kookye TMP36 Temperature Sensor
  
<img src="Pic/tmpcircuit.png" width="350">

Insert the three leads of the TMP36 into separate rows of the breadboard.

Make its flat surface facing toward you. This will help you correctly identify the pins.

-----
In this task, we will use the **Analog Discovery** to study the TMP36 sensor characteristics.

**Pin-to-Lead:**  
- Analog Discovery `W1` → `left lead` (TMP36='s Vin) 
- Analog Discovery `1+`  → `middle lead` (TMP36's analog voltage output)  
- Analog Discovery `1-` → Analog Discovery Ground `↓` → `right lead` (TMP36's ground) 

> [!CAUTION]  
> Never reverse the TMP 36 sensor's Vin and Gound connections.
>
> Wrong wiring can cause the sensor to overheat rapidly, even burn your finger!!

> [!TIP]  
> For easier checking, recommend to use a **red wire for Vin** and a **blue wire for Ground** when wiring the TMP36 sensor.

### 📌 Task 2.2 Sensor Reading

In WaveForms software, configure the **Wavegen** setup and run:

| Setting   | Value |
| --------- | ----- |
| Type |  DC     |
| Offset    |   5 V    |

Next in WaveForms software, open the **Voltmeter** and run.


<img src="Pic/voltmeter.png" width="350">


#### :pencil2:  Report Item 2-a

Record three voltage readings from Channel 1, taking a measurement every 30 seconds.


> [!CAUTION]  
> If the reading **exceeds 1.0 V**: Something is wrong. **Power down immediately**. **Do not touch the sensor**.

#### :pencil2:  Report Item 2-b

The conversion between TMP36 voltage and temperature is:

$$\mathrm{Temperature (°C)} = \dfrac{\mathrm{V (volts)} - 0.500}{0.010}$$

Use your three voltmeter readings from 2-a, compute the corresponding temperatures (°C). 

Do your values make sense?


### ✅ Proceed to Task 3. No Check Point in this part.

unless the temperature values make no sense.
