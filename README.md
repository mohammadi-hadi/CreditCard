<div align="center">

# Credit Card Fraud Detection

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Dataset: Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF.svg)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

*Detecting fraudulent transactions on highly imbalanced data — EDA, resampling, classical classifiers, neural networks, and clustering.*

</div>

## Overview

This is a study project on detecting fraudulent credit card transactions. The dataset is highly imbalanced (fraud cases are a small fraction of all transactions), so the project walks through a full experimental pipeline: exploratory data analysis, outlier detection, dimensionality reduction, supervised classification with and without resampling, small neural networks, and unsupervised clustering. The script was originally written as a Google Colab notebook and exported to Python.

## Data

[Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) dataset from Kaggle (ULB Machine Learning Group): anonymized European card transactions with features `Time`, `V1`-`V28` (PCA-transformed), `Amount`, and the binary target `Class` (1 = fraud). The script uses the first 50,000 rows of `creditcard.csv`. The CSV is not included in this repository; download it from Kaggle.

## Methods

All in `creditcard data fraud detection.py`:

- **EDA**: class distribution (pie chart), scatter plots of feature pairs colored by class, histograms, KDE plots, box and violin plots, and a correlation heatmap.
- **Outlier detection**: Tukey (IQR) fences per feature, with counts of flagged observations.
- **Feature reduction**: PCA with explained-variance analysis and a reduced 12-component projection.
- **Supervised models**: Decision Tree, k-Nearest Neighbors, Logistic Regression, SVM, and Random Forest, trained on
  - the original imbalanced data,
  - randomly oversampled data, and
  - randomly undersampled data (`imbalanced-learn`).
- **Evaluation**: accuracy, F1, precision, recall, confusion matrices, and classification reports for each setting.
- **Neural networks**: feed-forward Keras models (dense layers with concatenation/skip connections, one variant with dropout), trained with class weights and binary cross-entropy.
- **Unsupervised and hybrid**: K-Means clustering with silhouette analysis on PCA-reduced data, followed by cluster-wise classification experiments.

## Quick Start

```bash
git clone https://github.com/mohammadi-hadi/CreditCard.git
cd CreditCard
pip install -r requirements.txt
```

1. Download `creditcard.csv` from the Kaggle link above.
2. Update the path in the `pd.read_csv(...)` call near the top of the script (it currently points to a Google Drive location from the original Colab session).
3. Run the script section by section, or import it back into a notebook environment.

## Repository Structure

```
CreditCard/
├── creditcard data fraud detection.py   # Full analysis pipeline (exported Colab notebook)
├── requirements.txt                     # Python dependencies
├── CONTRIBUTING.md                      # Contribution guidelines
├── LICENSE                              # MIT License
└── README.md                            # This file
```

## License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.

## Contact

- **Hadi Mohammadi** — Utrecht University
- Website: [mohammadi.cv](https://mohammadi.cv)
