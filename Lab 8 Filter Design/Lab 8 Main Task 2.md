# Lab 8 Filter Design

## :dart: Task 2 – Understand FFT

Keep the previous setting in Task 1.

---
### 📌 Task 1.1 FFT Tool
**“FFT” ** (Fast Fourier Transform) is a tool to identify the freq-based compositions of a complex
signal.

On the top bar of the Scope, click `FFT` and set it as:

* Start: 0 Hz; Stop 500 Hz (or smaller)
* Top: 20 dB; Bottom -40 dB
* Type: Sample; Window: Flat Top
* Units: Peak (dB); Reference: 1 V

Now, in the FFT display, you should see 2 significant peaks.

The primary peak corresponds to the main signal $sin(50t)$, the secondary peak corresponds
to the noise part $0.2 \sin(1000t)$.

Any peak below -40 dB can be ignored, as $20 log 0.01 = −40 dB$, 0.01 is a
small enough ratio. This is why Buttom is -40 dB setup.

### 
