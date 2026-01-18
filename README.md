<div align="center">

# Credit Card Fraud Detection

### Machine Learning Pipeline for Detecting Fraudulent Transactions

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)

*Comprehensive fraud detection using exploratory data analysis and machine learning*

---

</div>

## Overview

This repository contains a Python implementation for detecting credit card fraud using various visualization and machine learning techniques. The pipeline includes exploratory data analysis, outlier detection, feature reduction, and model evaluation.

## Features

- **Exploratory Data Analysis (EDA)**: Comprehensive visualizations for understanding data patterns
- **Outlier Detection**: Tukey method for identifying anomalies
- **Feature Reduction**: PCA for dimensionality reduction
- **Multiple Visualizations**: Pie charts, scatter plots, histograms, KDE, box plots, violin plots, heatmaps

## Dataset

The dataset consists of 50,000 credit card transactions with:
- 30 features per transaction
- Binary classification: fraudulent (1) or non-fraudulent (0)

## Quick Start

```bash
# Clone the repository
git clone https://github.com/mohammadi-hadi/CreditCard.git
cd CreditCard

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# Run the analysis
python "creditcard data fraud detection.py"
```

## Pipeline

### 1. Data Import
Load and prepare the credit card transaction dataset.

### 2. Exploratory Data Analysis
- Pie chart for target distribution
- Scatter plots for feature relationships
- Histograms, KDE plots, box plots, violin plots
- Correlation heatmaps

### 3. Outlier Detection
Tukey method implementation with box plot visualizations for each feature.

### 4. Feature Reduction
- Principal Component Analysis (PCA)
- Explained variance plots
- 2D transformed data visualization

### 5. Preprocessing
Missing value detection and handling.

### 6. Model Training
Machine learning model training and evaluation for fraud prediction.

## Repository Structure

```
CreditCard/
├── creditcard data fraud detection.py  # Main analysis script
├── LICENSE                              # MIT License
├── CONTRIBUTING.md                      # Contribution guidelines
└── README.md                           # This file
```

## Requirements

- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or collaboration inquiries:
- **Hadi Mohammadi** - Utrecht University
- **Email**: [h.mohammadi@uu.nl](mailto:h.mohammadi@uu.nl)
- **Website**: [mohammadi.cv](https://mohammadi.cv)
