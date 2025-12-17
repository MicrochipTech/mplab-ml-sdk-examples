<p align="center">
  <img src="images/mchpedgeaibanner.png" alt="Microchip Edge AI" width="100%">
</p>

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Platforms](https://img.shields.io/badge/platforms-MCU%20%7C%20MPU%20%7C%20FPGA%20%7C%20dsPIC-red)
![Domain](https://img.shields.io/badge/Edge%20AI-%20Applications-orange)
![ML](https://img.shields.io/badge/Machine%20Learning-Embedded-yellow)
![License](https://img.shields.io/badge/license-Microchip-blue)

# MPLAB ML SDK Examples

Practical examples and tutorials for working with the [MPLAB ML Development Suite](https://mplabml.microchip.com) Python SDK.

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
│   ├── sharing-projects.ipynb      # ✅ Share projects between accounts
│   ├── understanding-data.ipynb    # ✅ Data formats and exploration
│   ├── labeling-data/              # 🚧 Labeling techniques
│   └── complete-workflows/         # 🚧 End-to-end examples
│
├── datasets/                       # Sample data for examples
│   ├── arc-fault/                  # IEEE arc fault samples
│   ├── gesture/                    # IMU gesture data
│   └── vibration/                  # Motor vibration samples
│
├── docs/                           # Documentation
│   ├── getting-started/
│   │   └── creating-api-key.md    # ✅ API key setup guide
│   └── concepts/                   # 🚧 Deep dive guides
│
└── scripts/                        # Utility scripts
```

## Available Notebooks

### ✅ Ready to Use

**[getting-started.ipynb](notebooks/getting-started.ipynb)**
- Install and authenticate
- Explore SDK functions
- List projects

**[sharing-projects.ipynb](notebooks/sharing-projects.ipynb)**
- Download complete projects
- Share between accounts
- Project transfer workflows

**[understanding-data.ipynb](notebooks/understanding-data.ipynb)**
- Sequential vs wide data formats
- Data quality checks (missing values, outliers, label issues)
- Visualization techniques
- Basic data cleaning


**Labeling Data**
- Manual labeling
- Threshold-based auto-labeling
- Event-triggered labeling
- Creating manifests

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

# Load sample data
df = pd.read_csv('datasets/series_load_sample.csv')
```

### Option 2: Download Individual Files
```python
import pandas as pd

# Download directly from GitHub
url = 'https://raw.githubusercontent.com/MicrochipTech/mplabml-sdk-examples/main/datasets/normal_samples.csv'
df = pd.read_csv(url)
```

### Option 3: Use Sample Data Utility (Coming Soon)
```python
from utils import load_sample_data

# Load pre-configured sample datasets
df = load_sample_data('arc-fault-normal')
```

## Datasets Included
Coming Soon

## Learning Paths

### 🎓 Beginner
1. [Create API Key](docs/getting-started/creating-an-api-key.md)
2. [Getting Started Notebook](notebooks/getting-started.ipynb)
3. [Understanding Data Formats](notebooks/understanding-data.ipynb)
4. [Sharing Projects](notebooks/sharing-projects.ipynb)

### 📊 Data Preparation Focus
1. [Understanding Sequential Format](notebooks/understanding-data.ipynb)
2. [Data Exploration and Visualization](notebooks/understanding-data.ipynb)
3. [Manual Labeling: Working with Pre-labeled Datasets](notebooks/manual_labeling.ipynb)
4. Threshold-Based Auto-Labeling
5. Creating Manifests
6. Upload Complete Project

## Requirements

- Python 3.8+
- MPLAB ML account ([sign up here](https://mplabml.microchip.com))
- API key (see [setup guide](docs/getting-started/creating-api-key.md))

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

[MPLAB ML Development Suite](https://mplabml.microchip.com) is Microchip's cloud-based machine learning platform for embedded systems. It enables:

- 🎯 **Edge ML**: Deploy models on microcontrollers (dsPIC33, SAMD21, etc.)
- 📊 **Data Processing**: Time-series feature extraction and pipeline building
- 🔧 **AutoML**: Automated model training and optimization
- 💾 **Knowledge Packs**: Generate optimized C code for deployment
- 🚀 **No ML Expertise Required**: GUI-driven workflow for engineers

## Contributing

This repository is growing! Contributions welcome:

- 📓 Additional example notebooks
- 📊 New sample datasets
- 📝 Documentation improvements
- 🐛 Bug reports and fixes

## Resources

- [MPLAB ML Documentation](https://mplabml.microchip.com/docs)
- [MPLAB ML Web Interface](https://mplabml.microchip.com)
- [API Key Setup Guide](docs/getting-started/creating-api-key.md)
- [Microchip Developer Help](https://microchipdeveloper.com)

## License

[Add your license here]

## Support

- 📖 Check the [documentation](docs/)
- 💬 Open an issue for questions or bug reports

---

**Status**: 🚧 Active Development - New notebooks and examples added regularly!

**Last Updated**: December 2025