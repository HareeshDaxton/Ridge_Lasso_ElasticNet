# Algerian Forest Fires - Regression Analysis (Ridge, Lasso, ElasticNet)

## 📌 Project Overview

This project focuses on the **Algerian Forest Fires dataset**, a real-world dataset collected from the Bejaia and Sidi-Bel Abbes regions. The goal is to **analyze the relationship between environmental factors and the Fire Weather Index (FWI)** using various linear regression techniques: Ridge, Lasso, ElasticNet, and standard Linear Regression.

This repository includes:
- Complete **data cleaning and preprocessing**
- **EDA** (Exploratory Data Analysis) to understand distributions and correlations
- **Model building and comparison** of regression algorithms
- Feature scaling and multicollinearity handling

---

## 🗂️ Files Included

| File Name                                | Description                                                   |
|------------------------------------------|---------------------------------------------------------------|
| `Algerian_forest_fires_dataset_UPDATE.csv` | Original dataset (raw format)                                |
| `Cleaned_Algerian_forest_fires_dataset.csv` | Cleaned and formatted dataset ready for modeling              |
| `ridge_lasso_EDA.ipynb`                  | EDA + preprocessing: cleaning, conversion, visualization      |
| `ridge_lasso_MAIN.ipynb`                 | Regression model training, evaluation, and comparison         |

---

## 🔍 Dataset Description

- **Total samples:** 243
- **Target variable:** `FWI` (Fire Weather Index)
- **Features include:** 
  - Temperature, Relative Humidity (RH), Wind speed (Ws), Rainfall, and fire indices (FFMC, DMC, DC, ISI, BUI)
  - `Region` (Bejaia=0, Sidi-Bel Abbes=1)
  - `Classes` (converted to binary: fire = 1, not fire = 0)

---

## 📊 EDA Highlights

- Null values identified and removed
- Feature types cast appropriately (`int64`, `float64`)
- Outlier detection using histograms and boxplots
- Correlation analysis using heatmaps
- Class distribution visualized using pie chart

---

## ⚙️ Modeling Techniques

| Model            | Purpose                                                   |
|------------------|-----------------------------------------------------------|
| **LinearRegression** | Baseline regression model                               |
| **Ridge Regression** | L2 regularization to reduce overfitting from multicollinearity |
| **Lasso Regression** | L1 regularization to perform feature selection          |
| **ElasticNet**       | Hybrid of L1 + L2 regularization                        |
| **LassoCV / RidgeCV / ElasticNetCV** | Cross-validated versions for optimal alpha selection |

All models use:
- `StandardScaler` for feature scaling
- Train/Test split: 75% training, 25% testing
- Evaluation metrics: **MSE**, **MAE**, **R² score**

---

## 📈 Evaluation Metrics

For each model, predictions were evaluated using:

- **Mean Squared Error (MSE)**
- **Mean Absolute Error (MAE)**
- **R² Score** (Coefficient of determination)

Visual validation done via scatter plots comparing actual vs predicted values.

---

## 🧠 Learning Purpose

This project is part of personal experimentation with regression techniques in machine learning. The goal is to practice real-world data cleaning, EDA, and model tuning using scikit-learn.

---


