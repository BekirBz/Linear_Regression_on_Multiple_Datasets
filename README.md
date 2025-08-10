# Linear Regression on Multiple Datasets

## Project Overview
This project applies **Linear Regression** techniques to analyze and model three different datasets. The goal is to predict target variables using simple and multiple linear regression models, evaluate their performance, and visualize the results.

The project was developed in a **ROS (Robot Operating System)** environment using Python and the `scikit-learn` library.

---

## Datasets Used
1. **Human Height and Weight Dataset**
   - Records: **10,000**
   - Features: Height (cm)
   - Target: Weight (kg)

2. **Human Brain Weight and Head Size Dataset**
   - Records: **237**
   - Features: Head Size (cm³)
   - Target: Brain Weight (grams)

3. **Boston Housing Dataset**
   - Records: **506**
   - Features: 13 attributes (e.g., CRIM, RM, TAX, LSTAT)
   - Target: MEDV (Median value of owner-occupied homes in $1000s)

---

## Steps Implemented

### **1. Data Loading**
- CSV datasets are loaded using `pandas`.
- Dataset statistics and head samples are printed for verification.

### **2. Feature & Label Selection**
- Height → Weight (Dataset 1)
- Head Size → Brain Weight (Dataset 2)
- 13 features → MEDV (Dataset 3)

### **3. Data Splitting**
- Used `train_test_split` from `sklearn.model_selection`.
- Train/Test ratio: **80% / 20%**
- Random seed fixed for reproducibility.

### **4. Model Training**
- `LinearRegression()` model from `sklearn.linear_model`.
- Model fitted using training data.

### **5. Model Prediction**
- Predictions generated on test data using `.predict()`.

### **6. Model Evaluation**
- Metrics:
  - **Mean Absolute Error (MAE)**
  - **R² Score**
- Visualization of regression lines and prediction results.

---

## Results Summary

| Dataset | MAE | R² Score | Notes |
|---------|-----|----------|-------|
| Human Height & Weight | ~2.96 | 0.97 | Very high correlation, model performs excellently. |
| Human Brain Weight & Head Size | ~27.45 | 0.63 | Moderate correlation, model captures trend but with variability. |
| Boston Housing | ~3.45 | 0.74 | Decent performance; multiple features contribute to prediction accuracy. |

---

## Visualizations
- Scatter plots with regression lines for single feature datasets.
- Predicted vs. actual value plots for Boston Housing.
- Error distribution histograms.

---

## Requirements
```bash
pandas
numpy
matplotlib
scikit-learn
