# Machine Learning-Based Prediction of Dry Eye Disease from Lifestyle and Ocular Metrics

**Author:** Harshini Muthukumar  
**Date:** December 12, 2025

---

## Overview

This project applies machine learning techniques to predict the presence of **Dry Eye Disease (DED)** using a structured dataset of lifestyle and ocular health metrics. The dataset includes subjects aged 18–45 and captures features such as sleep patterns, redness, BMI, blood pressure, and blue-light filter usage.

The analysis addresses class imbalance, evaluates multiple ML models, and culminates in a **heterogeneous weighted stacking ensemble** for improved diagnostic accuracy.

---

## Goals

- Build interpretable and accurate ML models for DED prediction
- Compare multiple classification algorithms (Logistic Regression, Random Forest, XGBoost)
- Develop a stacking ensemble approach to enhance performance
- Use evaluation metrics beyond accuracy: **Precision, Recall, F1-Score, and AUC-ROC**

---

## Repository Contents

| File | Description |
|------|-------------|
| `ded_pred.Rmd` | R Markdown source file with full analysis and code |
| `ded_pred.html` | Rendered HTML report with all outputs, plots, and model results |

---

## Analysis Workflow

### 1. Data Acquisition
- Dataset sourced from Kaggle containing ocular and lifestyle metrics

### 2. Data Exploration
- Distribution of Dry Eye Disease (imbalanced ~14,000 majority class)
- Sleep Disorder vs. DED comparison
- BMI distribution across DED groups
- Correlation heatmap
- Chi-square analysis for categorical features

### 3. Data Cleaning and Shaping
- Separated blood pressure into systolic and diastolic numeric features
- Derived BMI from height and weight
- Assessed normality of numeric variables (Shapiro-Wilk test)
- Identified and handled outliers
- Applied feature encoding for categorical variables

### 4. Handling Class Imbalance
- The dataset is significantly imbalanced
- Applied resampling strategies (oversampling/undersampling)
- Evaluated models using AUC-ROC, Precision, Recall, and F1-Score

### 5. Model Construction and Evaluation

| Model | Type |
|-------|------|
| Baseline Logistic Regression | Linear |
| Tuned Logistic Regression | Linear (hyperparameter-tuned) |
| Baseline Random Forest | Tree-based ensemble |
| Tuned Random Forest | Tree-based (hyperparameter-tuned) |
| Baseline XGBoost | Gradient boosting |
| Tuned XGBoost | Gradient boosting (hyperparameter-tuned) |

### 6. Heterogeneous Weighted Stacking Ensemble
- Combined predictions from all models into a meta-learner
- Improved overall diagnostic performance

### 7. Conclusion
- Summary of findings and best-performing model

---

##  Tools & Technologies

- **Language:** R
- **Format:** R Markdown (`.Rmd`) → HTML
- **Key Libraries:** `caret`, `randomForest`, `xgboost`, `ggplot2`, `dplyr`, `ROSE` (or `DMwR`)

---

## How to Run

1. Clone this repository:
```bash
   git clone https://github.com/harshi-vvm/dry-eye-disease-ml-prediction.git
```
2. Open `ded_pred.Rmd` in RStudio
3. Install required packages (if not already installed)
4. Click **Knit** to generate the HTML report

---


## Contact

For questions or feedback, feel free to reach out via GitHub Issues.
