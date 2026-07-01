# 🔬 LAB-O-SCOPE v3.0
### Real-Time Digital Signal Processing Oscilloscope & Spectrum Analyzer

<div align="center">

![HTML](https://img.shields.io/badge/HTML5-Frontend-orange?style=for-the-badge&logo=html5)
![CSS](https://img.shields.io/badge/CSS3-Styling-blue?style=for-the-badge&logo=css3)
![JavaScript](https://img.shields.io/badge/JavaScript-Logic-yellow?style=for-the-badge&logo=javascript)
![Web Audio API](https://img.shields.io/badge/Web-Audio%20API-green?style=for-the-badge)
![Canvas](https://img.shields.io/badge/HTML5-Canvas-red?style=for-the-badge)

**A browser-based professional Digital Signal Processing laboratory capable of performing real-time waveform visualization, spectrum analysis, frequency detection, RMS measurement, and signal generation using native Web APIs.**

</div>

[🚀 Live Demo](https://premshah-22.github.io/LAB-O-SCOPE-v3.0/)

---

# 📖 Overview

LAB-O-SCOPE v3.0 is an advanced browser-based virtual laboratory instrument inspired by professional oscilloscopes and spectrum analyzers.

Instead of requiring expensive laboratory hardware, this project transforms any modern web browser into a complete digital signal processing workstation capable of analyzing live audio signals with extremely low latency.

The application captures audio from the microphone (or internally generated signals), processes the incoming waveform using browser-native DSP capabilities, and visualizes both the time-domain and frequency-domain representations simultaneously.

Unlike simple audio visualizers, this project performs actual engineering calculations such as:

- Root Mean Square (RMS)
- Fast Fourier Transform (FFT)
- Frequency Bin Detection
- Trigger Stabilization
- Peak Frequency Estimation
- Signal Generation
- Oscilloscope Rendering

Everything runs completely inside the browser without requiring external frameworks.

---

# 🚀 Features

## 📈 Real-Time Oscilloscope

- Live waveform visualization
- Time-domain rendering
- Smooth phosphor-style animation
- Trigger stabilized waveform
- Adjustable gain
- Professional oscilloscope grid
- Low latency rendering

---

## 🎵 Real-Time Spectrum Analyzer

- Fast Fourier Transform (FFT)
- Frequency spectrum visualization
- Frequency bins
- Live spectral energy
- Dynamic amplitude display
- Real frequency estimation
- 20Hz – 20kHz visualization

---

## 🎙 Microphone Input

Supports direct live microphone analysis.

Features include:

- Live microphone capture
- Browser audio permissions
- Real-time visualization
- Instant frequency detection
- RMS computation

---

## 🔊 Built-in Signal Generator

Generate signals directly inside the browser.

Supported waveforms:

- Sine Wave
- Square Wave
- Triangle Wave
- Sawtooth Wave

Adjustable frequency from:

```
20 Hz
↓

4000 Hz
```

Perfect for testing DSP algorithms.

---

## 📊 FFT Analysis

The project uses the browser's native **AnalyserNode** for performing Fast Fourier Transform.

Supported FFT Sizes:

- 512
- 1024
- 2048
- 4096

Larger FFT sizes provide higher frequency resolution while smaller sizes improve refresh rate.

---

## ⚡ Trigger Stabilization

One of the major features of professional oscilloscopes is trigger synchronization.

LAB-O-SCOPE implements software trigger logic using rising-edge detection.

This keeps repetitive signals perfectly stable on the display.

Trigger options include:

- Enable / Disable Trigger
- Adjustable Trigger Threshold
- Rising Edge Detection

---

## 📏 RMS Voltage Measurement

The application continuously calculates signal RMS using

```
RMS = √((x₁²+x₂²+...+xₙ²)/N)
```

This provides a real engineering measurement of signal power rather than simple amplitude estimation.

---

## 🎯 Peak Frequency Detection

The strongest FFT frequency bin is detected automatically.

The application converts FFT bins into real-world frequency values using

```
Frequency =

(Bin Index × Sample Rate)
/ FFT Size
```

This allows accurate frequency estimation directly inside the browser.

---

## ❄ Freeze Frame

Capture the current waveform for inspection.

Useful for

- waveform analysis
- debugging
- educational demonstrations

---

## 🖥 Professional Laboratory UI

Designed to resemble laboratory-grade instruments.

Includes

- Oscilloscope screen
- Spectrum analyzer
- Hardware control panel
- Readout displays
- Instrument labels
- Professional color palette
- Retro CRT styling

---

# 🛠 Technologies Used

## Frontend

- HTML5
- CSS3
- Vanilla JavaScript

---

## Browser APIs

- Web Audio API
- Canvas API
- MediaDevices API
- AudioContext
- OscillatorNode
- AnalyserNode
- MediaStreamAudioSourceNode

---

## Graphics

- HTML5 Canvas
- Real-time rendering
- Dynamic plotting
- Animated waveform generation

---

# 🧠 DSP Concepts Implemented

This project demonstrates several Digital Signal Processing concepts including:

- Digital Signal Processing
- Fast Fourier Transform
- Discrete Fourier Transform
- Frequency Spectrum Analysis
- RMS Calculation
- Trigger Synchronization
- Waveform Sampling
- Signal Generation
- Audio Buffer Processing
- Time Domain Visualization
- Frequency Domain Visualization
- Nyquist Frequency
- Frequency Bin Mapping
- Real-Time Rendering

---

# ⚙ System Architecture

```
               Microphone
                    │
                    ▼
      MediaStreamAudioSourceNode
                    │
                    ▼
              AudioContext
                    │
                    ▼
              AnalyserNode
          ┌─────────┴─────────┐
          │                   │
          ▼                   ▼
 Time Domain Data      Frequency Data
          │                   │
          ▼                   ▼
 Oscilloscope          FFT Spectrum
          │                   │
          └─────────┬─────────┘
                    ▼
            Hardware Dashboard
```

---

# 🎛 Controls

### Input Source

- Microphone
- Signal Generator

---

### Generator Controls

- Waveform Type
- Frequency Slider

---

### Display Controls

- Gain
- FFT Window Size
- Trigger Level
- Freeze Display

---

### Readouts

- Peak Frequency
- RMS Voltage

---

# 📂 Project Structure

```
LAB-O-SCOPE/

│
├── index.html
├── style.css
├── script.js
├── assets/
│
└── README.md
```

*(If your project is currently a single HTML file, this structure can be adopted later by separating the CSS and JavaScript into their own files.)*

---

# 🎯 Educational Value

This project is useful for learning

- Digital Signal Processing
- Browser Audio APIs
- HTML5 Canvas
- FFT
- Audio Engineering
- Oscilloscope Design
- JavaScript Graphics
- Signal Analysis
- Web Performance
- Real-Time Visualization

It is especially suitable for students studying

- Electronics Engineering
- Computer Engineering
- Signal Processing
- Embedded Systems
- Communication Engineering

---

# 💡 Future Improvements

Possible future enhancements include:

- Export waveform as CSV
- Screenshot capture
- Multiple channels
- XY Mode
- Trigger modes
- Windowing Functions
- Spectrogram
- Waterfall Display
- Recording
- Audio File Import
- Measurement Cursors
- Peak Hold
- Harmonic Analysis
- THD Calculation
- Noise Floor Analysis
- Zoom Controls
- Mobile Support

---

# 🌐 Browser Compatibility

✔ Google Chrome

✔ Microsoft Edge

✔ Brave

✔ Opera

✔ Firefox (limited Web Audio differences)

---

# 🚀 Getting Started

Clone the repository

```bash
git clone https://github.com/your-username/LAB-O-SCOPE.git
```

Navigate to the project

```bash
cd LAB-O-SCOPE
```

Open

```
index.html
```

Allow microphone permissions when prompted.

Start analyzing audio instantly.

---

# 🤝 Contributing

Contributions are welcome.

If you would like to improve the project:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push your branch
5. Open a Pull Request

---

# 📜 License

This project is intended for educational, research, and learning purposes.

Feel free to use, modify, and extend the project while providing proper attribution.

---

# 👨‍💻 Author

## Prem Shah

**GitHub**

https://github.com/PremShah-22

**LinkedIn**

https://linkedin.com/in/prem-shah-848054389

---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.

It helps support the project and motivates future development.

---

<div align="center">

### 🔬 Bringing Professional Digital Signal Processing to the Browser

**LAB-O-SCOPE v3.0**

Real-Time • Interactive • Educational • Professional

</div>
