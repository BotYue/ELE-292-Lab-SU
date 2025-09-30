# Lab 4 Arduino I

These two labs (Lab4 & 5) will introduce Arduino basics, with emphasis on I/O.

Overall, Arduino is capable of:

* **Analog input** 
* **True analog output** (only on certain boards)
* **PWM output** 
* **Digital input**
* **Digital output**

Our lab will focus on the first 3 I/O types.

----------
<img src="Pic/m0pic.png" width="400">

The board we use is **Adafruit ItsyBitsy M0 Express**,
Its pinout can be found on 
https://github.com/adafruit/Adafruit-ItsyBitsy-M0-PCB/blob/master/Adafruit%20ItsyBitsy%20M0%20pinout.pdf 

For the pinout,

* **Analog input**: All pins labeled with **AIN** can do analog input. We recommend use from **Pin A1** to **Pin A5**.
* **True analog output**: **Pin A0** is the only true analog output pin. It is labeled by **VOUT**
* **PWM output**: Most pins labeled with **D** can do PWM output. We recommend use from **Pin 9** to **Pin 13** 

## :dart: Task 1 – LED and PWM output
---

Components Used:
* one LED
* one 220 Ω resistor (color code: red red brown gold)

<img src="Pic/ledplace.png" width="400">
