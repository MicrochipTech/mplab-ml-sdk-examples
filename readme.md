<p align="center">
  <img src="images/mchpedgeaibanner.png" alt="Microchip Edge AI" width="100%">
</p>

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Platforms](https://img.shields.io/badge/platforms-MCU%20%7C%20MPU%20%7C%20FPGA%20%7C%20dsPIC-red)
![Domain](https://img.shields.io/badge/Edge%20AI-%20Applications-orange)
![ML](https://img.shields.io/badge/Machine%20Learning-Embedded-yellow)
![License](https://img.shields.io/badge/license-Microchip-blue)

# MPLAB ML SDK Examples

Practical examples and tutorials for working with the [MPLAB ML Development Suite](https://www.microchip.com/en-us/tools-resources/develop/mplab-machine-learning-development-suite) Python SDK.

## Quick Start

### 1. Get an API Key
Follow the [API key creation guide](docs/getting-started/creating-an-api-key.md) to set up authentication.

### 2. Install Dependencies
```bash
pip install mplabml pandas matplotlib seaborn
```

### 3. Run Your First Notebook
Start with [getting-started.ipynb](notebooks/getting-started.ipynb) to:
- Authenticate with MPLAB ML
- Explore available SDK functions
- List your projects

## Repository Structure
```
mplabml-sdk-examples/
├── notebooks/                      # Interactive tutorials
│   ├── getting-started.ipynb       # ✅ Start here!
│   ├── sharing-projects.ipynb      # ✅ Collaborate with others
│   ├── understanding-data.ipynb    # ✅ Prepare your data
│   ├── import-research-dataset.ipynb  # ✅ Import labeled datasets
│   └── auto-label-with-events.ipynb   # ✅ Event-triggered labeling
│
├── datasets/                       # Sample data for examples
│   ├── series_load_sample.csv      # Arc fault data example
│   └── gesture_sample.csv          # Gesture with button events
│
├── docs/                           # Documentation
│   └── getting-started/
│       └── creating-an-api-key.md  # ✅ API key setup guide
│
└── scripts/                        # Utility scripts
```

## Available Notebooks

### ✅ Ready to Use

**[getting-started.ipynb](notebooks/getting-started.ipynb)** - Start here!
- Authentication and SDK setup
- Explore available functions
- List your projects

**[sharing-projects.ipynb](notebooks/sharing-projects.ipynb)** - Collaborate with others
- Download and share complete projects
- Transfer between accounts

**[understanding-data.ipynb](notebooks/understanding-data.ipynb)** - Prepare your data
- Sequential vs wide formats
- Data quality checks and visualization
- Find and fix common issues

**[import-research-dataset.ipynb](notebooks/import-research-dataset.ipynb)** - Use existing labeled data
- Import from IEEE, Kaggle, or your own research
- Work with pre-labeled datasets
- Create manifest and upload to MPLAB ML

**[auto-label-with-events.ipynb](notebooks/auto-label-with-events.ipynb)** - Automate labeling with triggers
- Use button press, GPIO, or PWM signals
- Detect rising/falling edges automatically
- Label gesture or activity segments

## Using Datasets from the Repository

Datasets are included in this repository for easy access in notebooks. You can load them directly:

### Option 1: Clone the Repository
```bash
git clone https://github.com/MicrochipTech/mplabml-sdk-examples.git
cd mplabml-sdk-examples
jupyter notebook
```

Then in your notebook:
```python
import pandas as pd

# Load arc fault sample
df = pd.read_csv('datasets/series_load_sample.csv')

# Or load gesture sample
df = pd.read_csv('datasets/gesture_sample.csv')
```

### Option 2: Download Directly from GitHub
```python
import pandas as pd

# Arc fault detection sample
url = 'https://raw.githubusercontent.com/MicrochipTech/mplabml-sdk-examples/main/datasets/series_load_sample.csv'
df = pd.read_csv(url)

# Gesture with button events sample
url = 'https://raw.githubusercontent.com/MicrochipTech/mplabml-sdk-examples/main/datasets/gesture_sample.csv'
df = pd.read_csv(url)
```

## Datasets Included

**Arc Fault Detection Sample**
- Source: IEEE Low Voltage DC Series Arc Fault dataset
- Format: Sequential (Time, current_signal, label)
- Size: 200,000 samples (~12.5 seconds)
- Sampling rate: 16 kHz
- Labels: -1 (normal), 0 (transient), 1 (arc fault)
- Location: `datasets/series_load_sample.csv`

**Gesture with Button Events Sample**
- Format: Sequential (AccelerometerX/Y/Z, GyroscopeX/Y/Z, Trigger)
- Size: 950 samples (~9.5 seconds)
- Sampling rate: 100 Hz
- Events: 3 wave gestures with button triggers
- Location: `datasets/gesture_sample.csv`

## Learning Paths

### 🚀 Complete Workflow
Follow this path to go from setup to trained model:

1. **Setup** → [Create API Key](docs/getting-started/creating-an-api-key.md)
2. **Authenticate** → [Getting Started](notebooks/getting-started.ipynb)
3. **Prepare Data** → [Understanding Data Formats](notebooks/understanding-data.ipynb)
4. **Import Data** → Choose your path:
   - Already have labels? → [Import Research Dataset](notebooks/import-research-dataset.ipynb)
   - Need to label with events? → [Auto-Label with Events](notebooks/auto-label-with-events.ipynb)
5. **Train Model** → Use MPLAB ML web interface for pipeline building and training
6. **Collaborate** → [Sharing Projects](notebooks/sharing-projects.ipynb) (optional)

### 📊 I Have Labeled Data
Skip straight to importing your research or proprietary datasets:

1. [Create API Key](docs/getting-started/creating-an-api-key.md) - Set up authentication
2. [Getting Started](notebooks/getting-started.ipynb) - Connect to MPLAB ML
3. [Understanding Data](notebooks/understanding-data.ipynb) - Verify your data format
4. [Import Research Dataset](notebooks/import-research-dataset.ipynb) - Upload with labels

### 🎯 I Need to Label Data with Events
Collect data with hardware triggers and auto-label:

1. [Create API Key](docs/getting-started/creating-an-api-key.md) - Set up authentication
2. [Getting Started](notebooks/getting-started.ipynb) - Connect to MPLAB ML
3. [Auto-Label with Events](notebooks/auto-label-with-events.ipynb) - Button/GPIO labeling

### 🎓 Quick Reference
**Just need one thing?**
- 🔑 [Set up API key](docs/getting-started/creating-an-api-key.md)
- 📤 [Share a project](notebooks/sharing-projects.ipynb)
- ✅ [Check data quality](notebooks/understanding-data.ipynb)
- 📥 [Import labeled data](notebooks/import-research-dataset.ipynb)
- 🔘 [Auto-label with button/events](notebooks/auto-label-with-events.ipynb)

## Requirements

- Python 3.8+
- MPLAB ML account ([sign up here](https://mplabml.microchip.com))
- API key (see [setup guide](docs/getting-started/creating-an-api-key.md))

### Python Dependencies
```
mplabml
pandas
numpy
matplotlib
seaborn
jupyter
```

Install all at once:
```bash
pip install -r requirements.txt
```

## What is MPLAB ML?

[MPLAB ML Development Suite](https://www.microchip.com/en-us/tools-resources/develop/mplab-machine-learning-development-suite) is Microchip's cloud-based machine learning platform for embedded systems. It enables:

- 🎯 **Edge ML**: Create compact supervised and anomaly-detection algorithms that can run on tiny edges for MCUs, dsPIC® DSCs and MPUs
- 📊 **Data Processing**: Time-series feature extraction and pipeline building
- 🔧 **AutoML**: Automated model training and optimization
- 💾 **Knowledge Packs**: Generate optimized C code for deployment
- 🚀 **No ML Expertise Required**: GUI-driven workflow for engineers

## Contributing

This repository is growing:

- 📓 Additional example notebooks
- 📊 New sample datasets
- 📝 Documentation improvements

## Support

- 

---

**Last Updated**: December 2025
