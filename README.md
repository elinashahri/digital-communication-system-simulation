# 8‑PSK Digital Communication System Simulation

This project implements an end‑to‑end simulation of a digital communication system using **8‑PSK modulation** in Python.  
The simulation models the main stages of a wireless communication link including baseband processing, pulse shaping, carrier modulation, transmission through a Rayleigh fading channel, and receiver‑side signal recovery.

The system performance is evaluated by computing the **Bit Error Rate (BER)** and visualizing the received constellation.

---

## Overview

The goal of this project is to demonstrate how digital data is transmitted through a wireless channel and how channel effects such as **Rayleigh fading and noise** influence the received signal.

The simulation follows the typical architecture of a communication system:

- Bit generation
- Symbol mapping (8‑PSK)
- Pulse shaping
- Passband modulation
- Wireless channel effects
- Demodulation and detection
- BER evaluation

---

## System Model

### Transmitter
The transmitter performs the following operations:

1. Generate a random binary bit sequence.
2. Group bits into **3‑bit symbols** for 8‑PSK modulation.
3. Map each symbol to corresponding **I/Q voltage levels**.
4. Oversample the signal to create discrete‑time samples.
5. Apply a **Root Raised Cosine (RRC) filter** for pulse shaping.
6. Modulate the baseband signals onto a carrier using **I/Q modulation**.
7. Combine the I and Q branches to produce the transmitted passband signal.

---

### Channel

The transmitted signal passes through a simulated wireless channel including:

- **Rayleigh fading** to model multipath propagation
- **Doppler shift** based on mobile velocity
- **Additive White Gaussian Noise (AWGN)**

Multiple fading paths are combined to form the received signal.

---

### Receiver

At the receiver, the signal processing steps include:

1. Coherent **I/Q demodulation**
2. **Matched filtering** using the same RRC filter
3. Symbol sampling and timing alignment
4. Phase‑based symbol detection for 8‑PSK
5. Reconstruction of the transmitted bit sequence
6. Calculation of **Bit Error Rate (BER)** and **Symbol Error Rate (SER)**

---

## Visualization

The simulation generates several plots that illustrate signal behavior throughout the system, such as:

- Transmitted baseband signals
- Pulse shaping filter response
- Carrier waveforms
- Received I/Q signals
- **Constellation diagram of detected symbols**

These plots help visualize the impact of fading and noise on signal detection.

---

## Technologies Used

- Python
- NumPy
- Matplotlib

---

## How to Run

Install the required Python libraries and run the script:
```bash
python project_dig_comm_(sof)_.py
