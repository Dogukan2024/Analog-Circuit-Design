# TRC-11 Citizens Band Radio
![IMG_4540](https://github.com/user-attachments/assets/2190325f-bf38-4602-82bc-fcdcfd53a2ff)

# TRC-11 Radio Transceiver – Laboratory Project  
**Complete Multistage Analog Communication System (Lab Sessions 2–9)**

This repository documents the design, analysis, simulation, and testing of the **TRC-11 27 MHz Radio Transceiver**, implemented across multiple laboratory sessions.  
The project includes building each subsystem of a real-world AM transceiver, performing theoretical analysis, LTSpice simulations, and final hardware testing.

---

# 📡 Project Overview

The TRC-11 is a low-power analog transceiver operating at **27.000 MHz**, with an **intermediate frequency (IF) of 15 MHz**.  
Across the labs, the following modules were designed, calculated, simulated, built, and tested:

- Oscilloscope probe theory & voltage regulation  
- Microphone amplifier (LM358)  
- Loudspeaker/Earphone amplifier (LM386)  
- IF Amplifiers (using KSP10 NPN transistors)  
- Transmitter power amplifier (2N2222)  
- Crystal characterisation & 15 MHz IF filter design  
- Envelope detector (1N4148), AGC circuit (LM358 + PIN diode)  
- Transmitter oscillator (27 MHz crystal oscillator)  
- Monopole antenna tuning  

Each chapter focuses on one functional building block of the transceiver.

---

# 📘 Lab Summaries

## **Lab 2 – Oscilloscope Probe & Voltage Regulator**  
(From: Chapter 2 report :contentReference[oaicite:0]{index=0})

- Probe attenuation ratios (1:1 and 10:1)  
- Required resistances to achieve accurate 10:1 attenuation  
- Compensation capacitor matching condition  
- Effective input capacitance & loading effects  
- 7806 voltage regulator dropout voltage, limits, load regulation  
- PTC thermistor characteristics  
- Forward voltage of diode 1N4001 at 1 A  
- Hands-on measurements of probe behaviour, AC line pickup, noise immunity  

---

## **Lab 3 – Microphone Amplifier (LM358)**  
(From: Chapter 3 report :contentReference[oaicite:1]{index=1})

- Non-inverting amplifier with gain:  
  \[
  A_v = 1 + \frac{R15}{R14}
  \]
- Lower & upper cutoff frequencies using C12/R13 and C13/R15  
- Full transfer function derived using nodal analysis  
- MATLAB frequency response simulation  
- Adjusting gain to 40 dB  
- OPAMP gain, supply current, open-loop response  
- Microphone preamp bandwidth: **~34 Hz – 3.4 kHz**

---

## **Lab 4 – IF Amplifier Design (15 MHz)**  
(From: Chapter 4 report :contentReference[oaicite:2]{index=2})

- Two-stage IF amplifier using **KSP10 high-frequency NPN**  
- Bias design based on:
  - Collector current: 2–8 mA (stage 1), 5–10 mA (stage 2)  
  - VCE = VCC/2 = 6 V  
  - β ≈ 110  
- Calculations for:
  - Rc, R1, Rf  
  - DC blocking capacitor C1 and bypass capacitor C2  
- LTSpice:
  - DC operating point  
  - Input impedance at 15 MHz  
  - Voltage gain in dB  
- Cascading effect analysis (loading between stages)

---

## **Lab 5 – Transmitter Power Amplifier (2N2222)**  
(From: Chapter 5 report :contentReference[oaicite:3]{index=3})

- Class-A RF power amplifier  
- Modulated supply voltage using PNP transistor Q31  
- Impedance-matching network using **coupled inductors (L1, L2) + C37**  
- Optimal load resistance:  
  \[
  R_{opt} = \frac{V_{CE}}{I_C}
  \]
- LTSpice analysis of matching network  
- Transient simulation of transmit signal  
- Safe operating limits for the 2N2222 power transistor  
- Biasing design for 20–40 mA operation  

---

## **Lab 6 – Crystal Characterization & IF Filter**  
(From: Chapter 6 report :contentReference[oaicite:4]{index=4})

- Resonant frequency measurement (fs)  
- Series resistance (rs), Q factor, motional inductance (Ls) & capacitance (Cs)  
- Frequency pulling using series capacitor  
- Two-crystal narrow-band IF filter design (bandwidth ~4–5 kHz)  
- Inverter impedance calculation:
  \[
  X = R_o + r_s
  \]
- Transformer design for proper termination  
- Tuning capacitor for IF transformer primary  

---

## **Lab 7 – Envelope Detector & Automatic Gain Control (AGC)**  
(From: Chapter 7 report :contentReference[oaicite:5]{index=5})

### Envelope Detector (1N4148)
- DC bias calculation  
- Resonant circuit tuning at 15 MHz  
- RC low-pass filtering  
- Detector output voltage:
  \[
  V_{ed} = 6 + I_{dc} R_{65}
  \]

### AGC System
- PIN diode attenuation control  
- LM358 configured as integrator  
- Setpoint voltage calculation  
- LED indication threshold  
- Maximum allowable PIN diode current  

---

## **Lab 8 – Transmitter Oscillator (27 MHz)**  
(From: Chapter 8 report :contentReference[oaicite:6]{index=6})

- Colpitts crystal oscillator using **BC238B** transistor  
- Bias design: IE = 4–6 mA  
- Base bias network using 20×R92 rule  
- Series capacitor (C94) for frequency trimming  
- Fine tuning to **27.000 MHz ± 1 kHz**  
- Oscillation amplitude verification (>1.5 Vpp)  
- Integration with modulation amplifier  

---

## **Lab 9 – Monopole Antenna & Tuning Network**  
(From: Chapter 9 report :contentReference[oaicite:7]{index=7})

- Monopole antenna reactance calculation  
- Radiation resistance formula:
  \[
  R_{rr} \approx 40 \pi^2 \left( \frac{l}{\lambda} \right)^2
  \]
- Series resonance tuning using custom-wound inductor  
- SMA connector installation  
- Resonance dip measurement at 27 MHz  
- Effective resistance RA calculation via voltage divider  
- “On the Air” testing:  
  - Atmospheric noise detection  
  - Receiver sensitivity  
  - AGC behavior during strong signals  

---

# 🛠 Tools & Methods Used

- **LTSpice** (AC analysis, transient analysis, impedance matching, transformer coupling)  
- **MATLAB** (frequency response analysis for microphone amplifier)  
- **Oscilloscope measurements** (fs, Q, envelope detection, harmonics, antenna tuning)  
- **Soldered hardware tests**  
- **Signal generator measurements** (15 MHz & 27 MHz)

---

# 📑 Key Learning Outcomes

- High-frequency transistor amplifier design  
- Biasing techniques for RF systems  
- Crystal physics and narrow-band filtering  
- Impedance matching using L-networks and transformers  
- AGC system architecture & feedback dynamics  
- RF power amplifier design and modulation  
- Antenna theory, tuning, and radiation resistance  
- Building a complete analog communication chain from scratch  

---

# 📦 Repository Contents

```
/Lab Reports
  - Lab2_Oscilloscope_Probe.pdf
  - Lab3_Microphone_Amplifier.pdf
  - Lab4_IF_Amplifier.pdf
  - Lab5_Transmitter_Amplifier.pdf
  - Lab6_Crystal_IF_Filter.pdf
  - Lab7_Envelope_Detector_AGC.pdf
  - Lab8_Transmitter_Oscillator.pdf
  - Lab9_Antenna_Tuning.pdf

/Schematics
  - LTSpice circuits
  - Diagrams and netlists

/Measurements
  - Oscilloscope screenshots
  - Frequency plots
  - MATLAB simulations
```


# 🙌 Acknowledgements

This work is based on the EE2xx Analog Communication Systems Laboratory at **Bilkent University**, following guided experiments that collectively build the TRC-11 radio transceiver.

