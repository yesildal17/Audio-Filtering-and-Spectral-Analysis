# Signals & Systems - Audio Signal Processing & Fourier Analysis

This repository contains the implementation of various Digital Signal Processing (DSP) techniques as part of the BLG354E Signals & Systems course. The project focuses on practical applications of filtering, LTI systems, and time-frequency analysis using Python.

##  Project Overview

The project is divided into three main technical challenges:

### 1. Noise Removal & Signal Isolation
- **Problem:** A corrupted audio signal containing human voice and musical instruments, masked by a 16kHz jamming tone and white noise.
- **Solution:** - Identified the interference frequency using Global FFT.
    - Designed a **4th-order Butterworth Low-pass filter** using **Second-Order Sections (SOS)** for numerical stability.
    - Isolated specific frequency bands using Bandpass filters.
    - **Result:** Improved Signal-to-Noise Ratio (SNR) from 0 dB to **39.12 dB**.

### 2. LTI Systems & Room Acoustics
- **Problem:** Simulating the effect of a physical environment on a clean audio signal.
- **Solution:**
    - Performed **Linear Convolution** between the audio signal and a Room Impulse Response (RIR).
    - Analyzed the **Comb Filtering** effect in the frequency domain.
    - Discussed the relationship between periodic nulls in the spectrum and time-domain echoes.

### 3. Waveform Classification (Time-Frequency Analysis)
- **Problem:** Identifying unknown waveforms (Sine, Square, Triangle) in a non-stationary signal.
- **Solution:**
    - Implemented **Short-Time Fourier Transform (STFT)** to generate Spectrograms.
    - Classified segments based on harmonic decay rates ($1/n$ for square vs $1/n^2$ for triangle).
    - Detected transition timestamps with high precision.

##  Technologies Used
- **Language:** Python 3.x
- **Libraries:** - `NumPy`: Numerical computations and signal representation.
  - `SciPy`: Signal processing modules (`scipy.signal`, `scipy.fft`, `scipy.io.wavfile`).
  - `Matplotlib`: Data visualization and spectral plotting.

##  Repository Structure
- `codes.ipynb`: Main Jupyter Notebook containing all signal processing algorithms and visualizations.
- `signal_hw2.pdf`: Detailed technical report with theoretical discussions and result analysis.
- `data/`: (Optional) Directory containing the .wav files used in the project.

##  How to Run
1. Ensure you have the required libraries installed:
   ```bash
   pip install numpy scipy matplotlib