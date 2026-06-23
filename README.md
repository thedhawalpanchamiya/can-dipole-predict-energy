# Can Molecular Dipole Moments Predict Molecular Potential Energy?

Investigating whether molecular dipole moments contain sufficient information to estimate quantum-chemically calculated molecular potential energy.

## Overview

This project explores a fundamental question in computational chemistry:

> Can molecular polarity alone provide enough information to predict molecular potential energy?

Using the CHAMPS Scalar Coupling dataset, this study examines the relationship between dipole moments and potential energy through exploratory data analysis, feature engineering, and machine learning regression models.

Rather than pursuing predictive accuracy alone, the objective is to understand the extent to which simple physicochemical descriptors capture information about molecular energetics and where their limitations emerge.

---

## Research Question

Can molecular dipole moments alone serve as reliable descriptors for predicting molecular potential energy?

Potential energy governs molecular stability and chemical behavior, whereas dipole moments characterize charge separation and molecular polarity.

Since electrostatic interactions contribute to molecular energy, this work investigates whether dipole moment information alone contains sufficient signal to estimate molecular potential energy.

---

## Motivation

Molecular machine learning often relies on complex descriptors involving geometry, connectivity, and electronic structure.

This project intentionally adopts a minimal representation based solely on dipole moments to examine:

* How much information polarity contains.
* Whether simple descriptors possess meaningful predictive power.
* The limitations of ignoring structural information.

Both positive and negative outcomes are scientifically informative.

---

## Dataset

Source:

**CHAMPS Scalar Coupling – Predicting Molecular Properties (Kaggle)**

License:

MIT License

### Files Used

#### dipole_moments.csv

Columns:

* molecule_name
* X
* Y
* Z

#### potential_energy.csv

Columns:

* molecule_name
* potential_energy

---

## Data Preparation

### Dataset Integration

The dipole moment and potential energy tables were merged using:

* molecule_name

### Data Quality Checks

* Verification of dataset dimensions
* Missing value inspection
* Consistency checks after merging

---

## Feature Engineering

### Input Features

* X
* Y
* Z

### Derived Feature

Dipole Magnitude

μ = √(X² + Y² + Z²)

### Potential Future Features

* Squared magnitude
* Absolute dipole components
* Interaction terms
* Higher-order polynomial features

Target Variable:

* potential_energy

---

## Exploratory Data Analysis

Visualizations include:

* Histograms
* Distribution plots
* Correlation heatmaps
* Scatterplots
* Pairplots

Questions investigated:

* Are dipole components correlated with potential energy?
* Does dipole magnitude exhibit systematic trends?
* Are relationships linear or nonlinear?
* Which descriptors contribute most strongly to prediction?

---

## Machine Learning Models

### Baseline Models

* Linear Regression
* K-Nearest Neighbors Regression
* Random Forest Regression

### Potential Future Models

* Ridge Regression
* Gradient Boosting
* XGBoost
* Neural Networks

The goal is to compare simple linear relationships with nonlinear learning approaches and evaluate the amount of information contained within dipole-based descriptors.

---

## Evaluation Metrics

Model performance is assessed using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score

Additional analyses include:

* Residual plots
* Predicted vs Actual plots
* Feature importance analysis

---

## Scientific Objectives

This study seeks to determine:

* Whether dipole moments are informative molecular descriptors.
* Whether polarity alone explains molecular energy.
* Which limitations arise when structural information is omitted.
* How far simple descriptors can be pushed before richer representations become necessary.

---

## Expected Outcomes

### Positive Outcome

Dipole moments provide meaningful predictive power and contain nontrivial information about molecular energetics.

### Negative Outcome

Dipole moments alone are insufficient, implying that molecular potential energy depends strongly on additional information such as:

* Molecular geometry
* Atomic composition
* Electronic structure
* Partial charges
* Bond connectivity

Either outcome contributes to understanding descriptor quality in molecular machine learning.

---

## Future Directions

Potential extensions include:

* Incorporating Mulliken charges
* Including structural descriptors
* Computing RDKit descriptors
* Generating molecular fingerprints
* Applying Graph Neural Networks
* Exploring SchNet and DimeNet architectures
* Extending toward broader molecular property prediction tasks

---

## Tools and Libraries

### Programming Language

Python

### Libraries

* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

### Development Environment

* Jupyter Notebook

### Version Control

* Git
* GitHub

---

## Project Structure

```text
├── data/
│   ├── dipole_moments.csv
│   └── potential_energy.csv
│
├── notebooks/
│   └── molecular_energy_prediction.ipynb
│
├── figures/
│   ├── correlation_heatmap.png
│   ├── distribution_plots.png
│   └── residual_analysis.png
│
├── requirements.txt
├── LICENSE
└── README.md
```

---

## Keywords

Computational Chemistry

Machine Learning

Molecular Property Prediction

Dipole Moments

Potential Energy

Regression

Quantum Chemistry

Chemical Informatics

Scientific Python

Scikit-Learn

---

## Author

Dhawal Panchamiya

BS-MS Natural Sciences
IISER Bhopal

Interested in:

* Computational Chemistry
* Machine Learning
* Scientific Computing
* Molecular Property Prediction
* Chemical Informatics

If you found this project interesting, consider starring the repository.
