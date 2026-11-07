# Data Mining Assignment: Bank Marketing & Concrete Strength Prediction

## Student Information
Name: Jonathan Stephen Kateega
Registration Number: S25M19/006
Access Number: B34976
Course: MSc Data Science & Analytics
Institution: Uganda Christian University (UCU)
Date: 7 November 2026

## Repository Link
[GitHub](https://github.com/jonathern/data_mining_assignment_1)

## Project Overview
This repository contains the complete analysis, code, and documentation for the Data Mining project-based assessment. It comprises two distinct machine learning projects:
1. **Project 1 (Classification):** Predicting term-deposit subscriptions for a Portuguese banking institution.
2. **Project 2 (Regression):** Predicting the compressive strength of concrete based on mixture composition and curing age.

## Directory Structure
```
data_mining_assignment_1/
├── .venv/                                          # Python virtual environment (not committed)
├── data/                                           # Raw datasets and documentation
│   ├── bank-additional-full-README.txt             # Documentation for Bank Marketing dataset
│   ├── bank-additional-full.csv                    # Dataset for Project 1
│   ├── Concrete_Data_README.txt                    # Documentation for Concrete dataset
│   └── Concrete_Data.csv                           # Dataset for Project 2
├── notebooks/                                      # Jupyter Notebooks (executable analysis)
│   ├── 1. Bank Marketing.ipynb                     # Project 1: Classification analysis
│   └── 2. Concrete Compressive Strength.ipynb      # Project 2: Regression analysis
├── .gitignore                                      # Git ignore rules
├── README.md                                       # Project documentation (this file)
└── requirements.txt                                # Python dependencies for reproducibility
```

## Prerequisites and Setup
To ensure reproducibility, this project requires Python 3.8 or higher.

### 1. Create a Virtual Environment (Recommended)

```
python -m venv venv
# Activate on Windows:
venv\Scripts\activate
# Activate on macOS/Linux:
source venv/bin/activate
```

### 2. Install Dependencies
Install the required Python packages using the provided `requirements.txt` file:

```
pip install -r requirements.txt
```

### 3. Run the Notebooks
Launch Jupyter Notebook or JupyterLab:

```
jupyter notebook
```

Open `1. Bank Marketing.ipynb` and `2. Concrete Compressive Strength.ipynb`. Run all cells from top to bottom (`Kernel -> Restart & Run All`). The notebooks are fully executable and contain all data preparation, modeling, and visualization steps.

----------------------------------

## Project 1: Bank Marketing (Classification)
### Objective
Develop and evaluate a model to predict whether a customer will subscribe to a term deposit, supporting targeted marketing campaigns.
### Key Methodological Steps
- **Data Preparation:** Identified and removed the duration feature to prevent data leakage (as call duration is unknown prior to the call). Handled missing values encoded as "unknown".
- **Baseline:** Established a majority-class baseline to demonstrate the "Accuracy Paradox" caused by severe class imbalance (~11% positive rate).
- **Model Selection:** Compared Logistic Regression, Random Forest, and XGBoost.
- **Threshold Optimization:** Analyzed the Precision-Recall curve to recommend an optimal decision threshold that balances the cost of unnecessary calls (False Positives) against the profit of missed subscribers (False Negatives).

----------------------------------

## Project 2: Concrete Compressive Strength (Regression)

### Objective
Predict the compressive strength (MPa) of concrete from its mixture ingredients and curing age.

### Key Methodological Steps
- **Data Preparation:** Applied StandardScaler to normalize features with varying magnitudes (e.g., Age vs. Aggregate volume).
- **Baseline:** Established a mean-prediction baseline (R² ≈ 0.0) to set the minimum performance threshold.
- **Model Comparison:** Compared linear (Ridge Regression) and non-linear (Random Forest, Gradient Boosting) approaches.
- **Diagnostics:** Inspected residual plots to identify that linear models systematically underestimate high-strength concrete, proving the necessity of non-linear modeling for this chemical process.
- **Causal Inference:** Critically evaluated the difference between predictive association and real-world causation, highlighting the risks of confounding variables (e.g., water-to-cement ratio) in observational data.

-----------------------------

## Data Sources and Attribution
The datasets used in this project are sourced from the UCI Machine Learning Repository and are used here strictly for academic purposes.
### Bank Marketing Dataset
Moro, S., Rita, P., & Cortez, P. (2014). Bank Marketing. UCI Machine Learning Repository. https://doi.org/10.24432/C5K306

### Concrete Compressive Strength Dataset:
Yeh, I. (1998). Concrete Compressive Strength. UCI Machine Learning Repository. https://doi.org/10.24432/C5PC7W