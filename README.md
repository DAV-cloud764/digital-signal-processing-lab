# Digital Signal Processing Laboratory

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![NumPy](https://img.shields.io/badge/NumPy-Numerical_Computing-013243?logo=numpy)
![SciPy](https://img.shields.io/badge/SciPy-Signal_Processing-8CAAE6)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?logo=matplotlib)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

A practical repository documenting Digital Signal Processing experiments and implementations using Python. It contains Jupyter Notebooks, mathematical calculations, signal visualizations, numerical results and experimental observations.

The experiments cover discrete-time signals, sampling, aliasing, quantization, convolution, correlation, difference equations, z-transforms, pole-zero analysis and system stability.

---

## Repository Structure

```text
digital-signal-processing-lab/
│
├── Week-01/
│   └── COU07506_Week01_240242463081.ipynb
│
├── Week-02/
│   └── COU07506_Week02_240242463081.ipynb
│
├── Week-03/
│   └── COU07506_Week03_240242463081.ipynb
│
├── Week-04/
│   └── COU07506_Week04_240242463081.ipynb
│
├── .gitignore
└── README.md
```

Each weekly directory contains a Jupyter Notebook with the corresponding practical exercises, code, results, plots and analysis.

---

## Laboratory Activities

### Week 1 – Introduction to Digital Signal Processing

**Topics:** Discrete-time signals and audio processing.

Activities:
- Generating unit impulse, step, ramp and exponential signals.
- Investigating exponential signals with different parameter values.
- Analysing discrete-time cosine signals and periodicity.
- Recording, loading, normalizing and plotting audio signals.
- Reading sampling frequency and audio duration.

**Notebook:** [Week 1 Laboratory](Week-01/COU07506_Week01_240242463081.ipynb)

### Week 2 – Sampling, Aliasing and Quantization

**Topics:** Sampling theory, aliasing, quantization and SQNR.

Activities:
- Demonstrating aliasing at different sampling frequencies.
- Comparing naive downsampling and FIR-based decimation.
- Implementing a uniform quantizer.
- Measuring quantization error.
- Verifying the 6 dB-per-bit SQNR relationship.
- Quantizing and analysing voice recordings.

**Notebook:** [Week 2 Laboratory](Week-02/COU07506_Week02_240242463081.ipynb)

### Week 3 – Convolution, Correlation and Difference Equations

**Topics:** Digital systems, convolution, correlation and system responses.

Activities:
- Implementing linear convolution using Python loops.
- Comparing manual convolution with NumPy.
- Measuring computational performance.
- Smoothing noisy signals using moving-average filters.
- Testing linearity and time-invariance.
- Estimating time delays using cross-correlation.
- Solving difference equations using recursion and SciPy.

**Notebook:** [Week 3 Laboratory](Week-03/COU07506_Week03_240242463081.ipynb)

### Week 4 – z-Transform, Poles, Zeros and Stability

**Topics:** z-transform, inverse z-transform, frequency response and system stability.

Activities:
- Developing a pole-zero plotting function.
- Calculating poles and zeros using SciPy.
- Computing inverse z-transforms using partial fractions.
- Verifying results using `signal.lfilter()`.
- Investigating pole radius and impulse-response behaviour.
- Classifying digital systems using pole-zero diagrams.
- Applying second-order stability conditions.
- Designing a digital resonator and analysing its response.

**Notebook:** [Week 4 Laboratory](Week-04/COU07506_Week04_240242463081.ipynb)

---

## Technologies and Libraries

| Technology | Purpose |
|---|---|
| Python 3.11 | Programming and numerical computation |
| NumPy | Array operations and mathematical calculations |
| SciPy | Digital signal processing and filtering |
| Matplotlib | Signal visualization |
| Jupyter Notebook | Interactive experiments |
| IPython | Notebook utilities and audio playback |
| Visual Studio Code | Development environment |
| Git | Version control |
| GitHub | Repository hosting |

---

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/DAV-cloud764/digital-signal-processing-lab.git
```

### 2. Navigate to the Project

```bash
cd digital-signal-processing-lab
```

### 3. Create a Virtual Environment

```bash
python -m venv .venv
```

### 4. Activate the Environment

For Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 5. Install Dependencies

```bash
python -m pip install numpy scipy matplotlib jupyter ipykernel
```

### 6. Register the Jupyter Kernel

```bash
python -m ipykernel install --user --name cou07506-dsp --display-name "Python 3.11 (COU07506 DSP)"
```

### 7. Open the Project in VS Code

```bash
code .
```

Open a weekly notebook and select the `Python 3.11 (COU07506 DSP)` kernel.

---

## Working with Audio Files

Some experiments require a WAV audio recording.

For Week 1, place your recording in the `Week-01` directory or the project root before running the notebook.

Personal audio recordings are excluded from the repository to protect privacy.

---

## Version Control

This project uses Git and GitHub to manage laboratory notebooks and track development history.

To get the latest changes:

```bash
git pull origin main
```

To contribute changes:

```bash
git add .
git commit -m "Update DSP laboratory exercises"
git push origin main
```

---

## Author

**David F. Mwakajonga**

GitHub: [@DAV-cloud764](https://github.com/DAV-cloud764)

---

**Repository:** [digital-signal-processing-lab](https://github.com/DAV-cloud764/digital-signal-processing-lab)

*Exploring Digital Signal Processing through Python, mathematical analysis and practical experimentation.*
