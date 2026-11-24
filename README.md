# Digital Signal Processing Laboratory (COU 07506)

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![NumPy](https://img.shields.io/badge/NumPy-Numerical_Computing-013243?logo=numpy)
![SciPy](https://img.shields.io/badge/SciPy-Signal_Processing-8CAAE6)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Data_Visualization-11557C)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Status](https://img.shields.io/badge/Status-3_Weeks_Completed-success)

A practical learning repository containing laboratory experiments, Python implementations, mathematical calculations, signal visualizations and observations for **Digital Signal Processing (COU 07506)** at Dar es Salaam Institute of Technology (DIT).

The repository covers the first three weeks of the module, focusing on fundamental concepts of discrete-time signals, sampling, aliasing, quantization, convolution, correlation and digital systems.

---

## Course Information

| Item | Details |
|---|---|
| Institution | Dar es Salaam Institute of Technology |
| Department | Computer Studies Department |
| Module | Digital Signal Processing |
| Module Code | COU 07506 |
| Academic Year | 2026/2027 |
| Semester | I |
| Unit | Unit 1 – Signals, Sampling and Systems |
| Programming Language | Python |
| Development Environment | Visual Studio Code and Jupyter Notebook |

## Repository Structure

```text
COU07506-DSP-Labs/
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
├── .gitignore
│
└── README.md
```

Each week has its own Jupyter Notebook containing the practical implementation, results, graphs, experimental observations and analysis questions.

---

# Weekly Laboratory Activities

## Week 1 – Lab 0: Setting Up the DSP Laboratory

**Topic:** Introduction to Digital Signal Processing and its role in AI.

The first week focused on preparing the programming environment and understanding elementary discrete-time signals.

### Activities Performed

**Task 1.1 – Generating Elementary Discrete-Time Signals**

Implemented and plotted four fundamental signals:

- Unit impulse signal.
- Unit step signal.
- Unit ramp signal.
- Exponential signal.

**Task 1.2 – Changing Signal Parameters**

Investigated exponential signals using different values of the exponential parameter:

- a = 0.5
- a = -0.8
- a = 1.1

Also investigated the periodicity of sampled cosine signals.

**Task 1.3 – Working with Audio**

Recorded and analysed a personal voice recording using Python.

The activities included:

- Loading WAV audio files.
- Converting stereo audio into mono.
- Normalizing audio amplitude.
- Displaying audio waveforms.
- Identifying sampling frequency and recording duration.
- Playing recorded audio inside Jupyter Notebook.

### Main Learning Outcomes

- Understanding discrete-time signals.
- Generating and plotting elementary signals.
- Understanding signal periodicity.
- Reading and analysing digital audio files.
- Preparing a Python environment for DSP experiments.

**Notebook:** [COU07506_Week01_240242463081.ipynb](Week-01/COU07506_Week01_240242463081.ipynb)

---

## Week 2 – Lab 1A: Sampling, Aliasing and Quantization

**Topic:** Sampling, aliasing, quantization and analogue-to-digital conversion.

The second week focused on understanding how continuous signals are represented digitally and how sampling frequency and quantization resolution affect signal quality.

### Activities Performed

**Task 2.1 – Aliasing of a Sinusoid**

Generated a 7 Hz cosine signal and investigated its behaviour at different sampling frequencies:

- 10 Hz
- 12 Hz
- 14 Hz
- 20 Hz

Calculated alias frequencies and compared the original and sampled signals using graphs.

**Task 2.2 – Hearing Aliasing**

Compared naive downsampling with proper decimation using an FIR anti-aliasing filter.

Tested different reduction factors:

- k = 2
- k = 4
- k = 8

Listened to the processed audio recordings and investigated the effects of aliasing.

**Task 2.3 – Implementing a Uniform Quantizer**

Generated a 300 Hz sinusoidal signal and implemented a 3-bit uniform quantizer.

Investigated:

- Number of quantization levels.
- Quantization step size.
- Quantization error.
- Difference between original and quantized signals.

**Task 2.4 – Verification of the 6 dB-per-bit Rule**

Calculated and compared measured and theoretical Signal-to-Quantization-Noise Ratio (SQNR) for different quantization resolutions.

Investigated the relationship between quantization bits and signal quality.

**Task 2.5 – Quantization of My Voice**

Quantized a recorded voice signal using:

- 4-bit resolution.
- 8-bit resolution.
- 12-bit resolution.

Compared the resulting audio recordings, calculated their SQNR and plotted the quantized waveforms.

### Selected Experimental Results

| Quantization | Levels | Measured SQNR |
|---|---:|---:|
| 4 bits | 16 | 17.74 dB |
| 8 bits | 256 | 40.95 dB |
| 12 bits | 4,096 | 64.78 dB |

### Main Learning Outcomes

- Understanding the Nyquist sampling principle.
- Identifying and calculating alias frequencies.
- Understanding anti-aliasing filters.
- Implementing uniform quantization.
- Calculating quantization error and SQNR.
- Verifying the theoretical 6 dB-per-bit relationship.

**Notebook:** [COU07506_Week02_240242463081.ipynb](Week-02/COU07506_Week02_240242463081.ipynb)

---

## Week 3 – Lab 1B: Convolution, Correlation and Difference Equations

**Topic:** Signals, systems, convolution, correlation and difference equations.

The third week focused on understanding how digital systems process signals and how their properties can be investigated using mathematical equations and Python.

### Activities Performed

**Task 3.1 – Convolution from the Definition**

Implemented linear convolution manually using Python loops.

Compared the manual implementation with NumPy's `np.convolve()` function.

Also measured execution time using two random sequences containing 2,000 samples each.

**Task 3.2 – Smoothing a Noisy Signal by Convolution**

Generated a noisy sinusoidal signal and applied moving-average filters with different lengths:

- M = 3
- M = 9
- M = 25

Compared the filtered signals and investigated the trade-off between noise reduction and signal distortion.

**Task 3.3 – Testing Linearity and Time-Invariance**

Investigated three digital systems to determine whether they were linear and time-invariant.

The systems included:

- Squaring system: y[n] = x[n]².
- Time-dependent system: y[n] = n*x[n].
- Three-point moving-average system.

**Task 3.4 – Finding a Hidden Delay Using Cross-Correlation**

Generated a transmitted random signal and simulated a delayed received signal containing noise.

Used SciPy cross-correlation to estimate the time delay.

Tested different noise levels and converted the estimated delay into time and sound travel distance.

Experimental delay:

- Actual delay: 37 samples.
- Estimated delay: 37 samples.
- Sampling frequency: 1,000 Hz.
- Time delay: 0.037 seconds.

**Task 3.5 – Difference Equations**

Implemented a digital system using three methods:

1. Direct recursion using a Python loop.
2. SciPy `signal.lfilter()`.
3. Mathematical closed-form expression.

Compared the impulse responses and calculated the step response.

The computed final step-response value was approximately 5.3333, agreeing with the theoretical system gain.

### Main Learning Outcomes

- Understanding and implementing linear convolution.
- Comparing manual and optimized numerical algorithms.
- Applying moving-average filters.
- Testing linearity and time-invariance.
- Estimating signal delays using cross-correlation.
- Solving digital difference equations.
- Understanding impulse responses, step responses and IIR systems.

**Notebook:** [COU07506_Week03_240242463081.ipynb](Week-03/COU07506_Week03_240242463081.ipynb)

---

# Technologies and Libraries

The laboratory activities were implemented using the following technologies:

| Technology | Purpose |
|---|---|
| Python 3.11 | Main programming language |
| NumPy | Numerical calculations and array operations |
| SciPy | Signal processing, convolution, filtering and correlation |
| Matplotlib | Signal visualization and plotting |
| Jupyter Notebook | Interactive laboratory implementation |
| Visual Studio Code | Development environment |
| Git | Version control |
| GitHub | Source code hosting and laboratory documentation |

## Environment Setup

The following instructions can be used to set up the laboratory environment on Windows.

### 1. Clone the repository

```bash
git clone https://github.com/DAV-cloud764/digital-signal-processing-lab.git
```

### 2. Open the project directory

```bash
cd digital-signal-processing-lab
```

### 3. Create a Python virtual environment

```bash
python -m venv .venv
```

### 4. Activate the environment

For Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 5. Install the required libraries

```bash
python -m pip install numpy scipy matplotlib jupyter ipykernel
```

### 6. Register the Jupyter kernel

```bash
python -m ipykernel install --user --name cou07506-dsp --display-name "Python 3.11 (COU07506 DSP)"
```

### 7. Open the project in Visual Studio Code

```bash
code .
```

Open the required weekly notebook and select the registered Python kernel.

**Note:** Python 3.11 or newer is suitable, provided the required libraries are installed.

---

# How to Use This Repository

1. Clone or download the repository.
2. Open the project using Visual Studio Code.
3. Activate the Python virtual environment.
4. Open the notebook for the week you want to study.
5. Select the Python DSP kernel.
6. Execute the notebook cells sequentially.
7. Review the numerical outputs, graphs and experimental observations.

Each notebook is organized according to its weekly laboratory activities.

---

# Learning Objectives

Through these three weeks of practical activities, the main objectives were to develop an understanding of:

- Discrete-time signal representation.
- Signal sampling and reconstruction concepts.
- Aliasing and the Nyquist sampling principle.
- Uniform quantization and SQNR.
- Digital filtering and signal smoothing.
- Linear systems and time-invariance.
- Linear convolution and cross-correlation.
- Digital difference equations.
- Impulse and step responses.

These concepts establish the foundation for more advanced Digital Signal Processing topics.

---

# Academic Reference

Dar es Salaam Institute of Technology (DIT).

**Computer Studies Department.**

*COU 07506 – Digital Signal Processing Laboratory Manual.*

Academic Year 2026/2027, Semester I.

Unit 1 – Signals, Sampling and Systems.

---

# Author

**David F. Mwakajonga**

Bachelor of Engineering in Computer Engineering
Dar es Salaam Institute of Technology

GitHub: [@DAV-cloud764](https://github.com/DAV-cloud764)

---

**Repository:** [digital-signal-processing-lab](https://github.com/DAV-cloud764/digital-signal-processing-lab)

*Learning Digital Signal Processing through practical implementation, mathematical analysis and experimentation.*
