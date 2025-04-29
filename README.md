# Asthma Prevalence Prediction Using Machine Learning

## 📌 Overview
This project focuses on predicting the prevalence of current asthma (CASTHMA) across U.S. counties using machine learning techniques. Utilizing the CDC PLACES dataset, we combine behavioral, preventive, and spatial features to develop accurate and interpretable models for small-area health prediction.

## 🧠 Objective
- Predict CASTHMA values at the county level.
- Evaluate and compare multiple regression models.
- Incorporate spatial awareness and model uncertainty through Gaussian Process Regression (GPR).

## 🗂️ Data Source
- **CDC PLACES Dataset**: [https://www.cdc.gov/places/](https://www.cdc.gov/places/)
- Features used: Smoking rates, preventive health behavior, geographic coordinates (Latitude & Longitude), and more.

## 🛠️ Methods Used
- Data Preprocessing: Cleaning, feature selection, scaling (MinMaxScaler)
- Feature Engineering: Cyclical transformation of spatial features
- Model Training:
  - Linear Regression
  - Ridge Regression
  - Support Vector Regression (SVR)
  - Gradient Boosting (with tuning)
  - Neural Network (MLP)
  - Gaussian Process Regression (GPR)
- Hyperparameter tuning via `RandomizedSearchCV`
- Evaluation Metrics: R² score, Mean Squared Error (MSE)

## 📊 Key Findings
- **SVR** and **Tuned Gradient Boosting** achieved the highest performance with R² ~0.79.
- **Gradient Boosting** had the lowest Test MSE (~0.0012), indicating highly accurate predictions.
- **GPR** provided uncertainty quantification with 95% confidence intervals, improving interpretability.
- **Neural Networks (MLP)** underperformed, likely due to data size and complexity.

## 📈 Visualization
- Scatter plots comparing actual vs predicted CASTHMA values.
- Confidence interval plots from GPR model.
- Feature importance analysis from tree-based models.

## ✅ Requirements
- Python 3.8+
- scikit-learn
- pandas
- numpy
- matplotlib / seaborn
- scipy

Install dependencies using:
```bash
pip install -r requirements.txt

