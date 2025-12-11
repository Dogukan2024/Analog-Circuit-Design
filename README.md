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

- Non-inverting amplifier with gain:  
- Lower & upper cutoff frequencies using C12/R13 and C13/R15  
- Full transfer function derived using nodal analysis  
- MATLAB frequency response simulation  
- Adjusting gain to 40 dB  
- OPAMP gain, supply current, open-loop response  
- Microphone preamp bandwidth: **~34 Hz – 3.4 kHz**

---

## **Lab 4 – IF Amplifier Design (15 MHz)**  

- Two-stage IF amplifier using **KSP10 high-frequency NPN**  
- Bias design  
- LTSpice 
- Cascading effect analysis (loading between stages)

---

## **Lab 5 – Transmitter Power Amplifier (2N2222)**  

- Class-A RF power amplifier  
- Modulated supply voltage using PNP transistor Q31  
- Impedance-matching network using **coupled inductors (L1, L2) + C37**  
- Optimal load resistance:  
- LTSpice analysis of matching network  
- Transient simulation of transmit signal  
- Safe operating limits for the 2N2222 power transistor  
- Biasing design for 20–40 mA operation  

---

## **Lab 6 – Crystal Characterization & IF Filter**  

- Resonant frequency measurement (fs)  
- Series resistance (rs), Q factor, motional inductance (Ls) & capacitance (Cs)  
- Frequency pulling using series capacitor  
- Two-crystal narrow-band IF filter design (bandwidth ~4–5 kHz)  
- Inverter impedance calculation:
- Transformer design for proper termination  
- Tuning capacitor for IF transformer primary  

---

## **Lab 7 – Envelope Detector & Automatic Gain Control (AGC)**  

### Envelope Detector (1N4148)
- DC bias calculation  
- Resonant circuit tuning at 15 MHz  
- RC low-pass filtering  
- Detector output voltage:

### AGC System
- PIN diode attenuation control  
- LM358 configured as integrator  
- Setpoint voltage calculation  
- LED indication threshold  
- Maximum allowable PIN diode current  

---

## **Lab 8 – Transmitter Oscillator (27 MHz)**  

- Colpitts crystal oscillator using **BC238B** transistor  
- Bias design: IE = 4–6 mA  
- Base bias network using 20×R92 rule  
- Series capacitor (C94) for frequency trimming  
- Fine tuning to **27.000 MHz ± 1 kHz**  
- Oscillation amplitude verification (>1.5 Vpp)  
- Integration with modulation amplifier  

---

## **Lab 9 – Monopole Antenna & Tuning Network**  

- Monopole antenna reactance calculation  
- Radiation resistance formula:
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

```


# 🙌 Acknowledgements

This work is based on the EE211 Analog Circuit Design Laboratory at Bilkent University, following guided experiments that collectively build the TRC-11 radio transceiver.

