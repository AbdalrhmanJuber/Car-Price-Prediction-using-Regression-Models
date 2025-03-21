# Car Price Prediction using Regression Models

## Project Overview
This project applies various regression techniques to predict car prices using a dataset sourced from the YallaMotors website. The primary goal is to explore linear and nonlinear regression models, perform feature selection, and apply regularization methods and hyperparameter tuning to identify the best predictive model.

## Dataset Information
The dataset contains approximately 6,750 records and 9 features, including:
- Car name
- Price (target variable)
- Engine capacity
- Cylinder count
- Horsepower
- Top speed
- Number of seats
- Brand
- Country of origin

[Dataset Source](https://www.kaggle.com/datasets/ahmedwaelnasef/cars-dataset/data)

## Data Processing Steps
### 1. Data Cleaning
- Standardized car prices to USD.
- Converted numeric features to appropriate data types, handling illegal values as NaN.
- Filled numeric missing values with the mean, categorical missing values with the mode.

### 2. Feature Engineering
- Applied Label Encoding for categorical features.
- Normalized numeric features using Min-Max Scaling (range 0 to 1).
- Split data into training (60%), validation (20%), and testing (20%) sets.

### 3. Feature Selection
- Applied Forward Selection, resulting in the selection of features: `Cylinder`, `Top speed`, `Engine capacity`, `Country`, `Brand`, and `Car name`.

## Regression Models Evaluated
- Linear Regression (Closed-form)
- Linear Regression (Gradient Descent)
- LASSO Regression (L1 Regularization)
- Ridge Regression (L2 Regularization)
- Polynomial Regression (degree optimized via grid search)
- Gaussian Regression (Radial Basis Function)

## Results and Evaluation
- Polynomial Regression (degree 9) demonstrated the highest performance, with very high accuracy and minimal error (MSE, MAE, and R² near optimal).
- Evaluated all models using metrics: Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared (R²).

## Hyperparameter Tuning
- Used Grid Search to optimize hyperparameters:
  - LASSO (optimal α = 59.64)
  - Ridge (optimal α = 0.123)
  - Polynomial Regression (optimal degree = 9)
  - Gaussian Regression (optimal σ = 7.9)
  - Gradient Descent learning rate (optimal = 0.452)

## Python Libraries Used
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## How to Run the Project
1. Clone this repository.
2. Install required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```
3. Execute the provided Python script:
```bash
python regression_models.py
```

## Contributors
- Ali Shaikh Qasem (ID: 1212171)
- Abdelrahman Jaber (ID: 1211769)

## Supervisors
- Dr. Ismail Khater
- Dr. Yazan Abu Farha

## University
Birzeit University, Faculty of Engineering and Technology, Department of Electrical and Computer Engineering.

## Date
November 28, 2024

