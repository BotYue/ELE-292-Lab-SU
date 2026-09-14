# Lab 5 Arduino II

## :dart: Task 3 – A Closer look at Serial Signal

This task shows you in detail what is a serial signal.

### 📌 Task 3.1 Setup

- [ ] Get rid of all previous wires. Also return the joystick.

- [ ] In WaveForms, turn off "Supplies".

- [ ] Now, use only 2 jumpwires:
<br> one from Analog Discovery digital pin 0 to Arduino pin TX
<br> one from Analog Discovery ground pin to Arduino ground pin.

- [ ] Keep most of your previous Arduino code in Task 2.<br>
change all `Serial.print` to `Serial1.print`, change `Serial.println` to `Serial1.println`

- [ ] Upload code and run.

--------
### 📌 Task 3.2 Logic Analyzer

Go to WaveForms, open "Logic". This is logic analyzer, another instrument.

- [ ] Add "UART" Channel at Pin DIO 0, specify the Baud rate at "Manual", "9.6k".
- [ ] On top tab, "Simple - Pulse - Protocol", select "Protocol", then "Idle".
- [ ] Set trigger type as "Auto"
- [ ] Run as "Single"
- [ ] Adjust to obtain the full message and corresponding signal

### ✅ Check Point 3 — Logic Analyzer

- Return components to their proper bins.
- Place the blue workbench on the shelf in the correct order:  








