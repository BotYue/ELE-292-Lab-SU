# Lab 4 Arduino I

## :dart: Task 3 – Temperature sensor & Analog Input
---
### 📌 Task 3.1 Circuit Setup
In this task, we will use the **Arduino** to get the reading from TMP36 temperature sensor.

**Pin-to-Lead:**  
- Arduino `3V` or `VHI` Pin → `left lead` (sensor's Vin) 
- Arduino Analog input Pin  → `middle lead` (sensor's analog voltage output)  
- Arduino `G` Pin  → `right lead` (sensor's ground) 

`3V` Pin is a 3.3 V source; `VHI` Pin is a 5 V source. Either one satisfies the requirement.

For Arduino Analog input Pin, you can pick any one indicated in the pre-Task 1 introduction.

> [!CAUTION]  
> Never reverse the TMP 36 sensor's Vin and Gound connections.
> 
<img src="Pic/tmpcircuit.png" width="350">

-------
### 📌 Task 3.2 Arduino Code
```c
const int   PIN_TEMP = A1;
// If your TMP36 is connected to A1 Pin.


void setup() { 
  Serial.begin(9600); 
  }

void loop() {
  float tmp36_raw_reading = analogRead(PIN_TEMP);
  float tmp36_voltage = tmp36_raw_reading/1023.0*3.3;
  
// your work later

  Serial.print(millis()); // Print Time
  Serial.print(", ");
  Serial.println(tmp36_voltage, 3);

}
```
