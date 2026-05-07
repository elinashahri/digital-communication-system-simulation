# digital-communication-system-simulation
Simulation of a digital communication system in Python including modulation schemes, channel effects, and BER/SER performance evaluation.

---

```markdown
# Digital Communication System Simulation

This project simulates an end-to-end **digital communication system** in Python. It includes bit generation, symbol mapping, pulse shaping, carrier modulation, Rayleigh fading, noise corruption, demodulation, matched filtering, and performance evaluation using BER/SER.

## Features

- Random bit generation
- Bit stream splitting into I/Q/control components
- Custom voltage-level symbol mapping
- Oversampling and pulse shaping
- Root Raised Cosine (RRC) filtering
- I/Q carrier modulation
- Rayleigh fading channel simulation
- Noise addition
- Receiver-side demodulation
- Matched filtering
- Constellation recovery
- BER/SER estimation

## Methods Used

- `numpy.random.randint`
- Custom bit-to-voltage mapping
- `rrcosfilter(...)` for pulse shaping
- Carrier multiplication with sine and cosine signals
- Rayleigh fading generation using a sum-of-sinusoids style model
- `np.convolve` for filtering
- `np.arctan2` for quadrant-based decision making
- BER and SER calculation

## Simulation Parameters

Some of the main hard-coded simulation parameters include:

- Bits per symbol: `bps = 3`
- Sample rate: `sample_rate = 100`
- Samples per symbol: `sps = 8`
- Number of bits: `N = 3000`
- Pulse shaping length: `length = 100`
- Roll-off factor: `beta = 0.8`
- Carrier frequency: `Fc = 10e5`

Rayleigh fading settings:

- Mobile speed: `v_mph = 60`
- Center frequency: `center_freq = 15e6`
- Sampling frequency: `Fs = 8049`
- Number of sinusoids: `N = 100`

## Outputs

The script produces:

- Bit-stream stem plots
- Oversampled PAM-like signals
- RRC filter impulse response
- Filtered I/Q streams
- Carrier waveforms
- Modulated transmitted signals
- Rayleigh fading waveform
- Demodulated received signals
- Real and imaginary received traces
- Constellation diagram
- BER printed in the console

## Purpose

This project is designed as an educational communication systems simulation to demonstrate:

- baseband to passband transmission,
- channel impairments,
- receiver processing,
- and performance analysis in fading environments.

## Requirements

- Python 3
- NumPy
- Matplotlib

## How to Run
```bash
python project_dig_comm_(sof)_.py
