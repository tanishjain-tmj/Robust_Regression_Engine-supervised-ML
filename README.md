## Robust Regression Engine project
## House Price Prediction

A machine learning project that predicts house prices using different regression algorithms. This project explores regularization, cross-validation, tree-based models, Support Vector Regression, hyperparameter tuning, and model evaluation to identify the best-performing regression approach.

## 🎥 Project Video Presentation

Watch the project presentation:

[Click Here to Watch Project Presentation](https://drive.google.com/file/d/1TKOb-dWcaHLd_AUphB32Du1l8J-Dw3jr/view?usp=sharing)

## 📌 Project Overview

The objective is to estimate house prices based on property-related features and compare different regression algorithms to understand their prediction performance.

This project covers:
- Ridge Regression (L2 Regularization)
- Lasso Regression (L1 Regularization)
- K-Fold Cross-Validation
- Stratified K-Fold Cross-Validation
- Leave-One-Out Cross-Validation (LOOCV)
- Time Series Split
- Decision Tree Regression
- Random Forest Regression
- Support Vector Regression (SVR)
- Hyperparameter Tuning
- Model Evaluation and Comparison
- Overfitting and Underfitting Analysis

## 📂 Dataset

The project uses `Advanced_Regression_HousePrice_Dataset_3800.xlsx`, containing 3,800 records and 12 columns.

### Column Description

| Column | Description |
|---|---|
| property_id | Unique property identifier |
| sale_date | Date of property sale |
| area_sqft | House area in square feet |
| bedrooms | Number of bedrooms |
| bathrooms | Number of bathrooms |
| location_score | Numerical location score |
| property_age | Age of the property |
| distance_city_km | Distance from the city |
| near_school | Indicates whether a school is nearby |
| near_metro | Indicates whether a metro station is nearby |
| crime_rate_index | Crime rate index of the area |
| house_price_inr | Target house price in INR |

`property_id` and `sale_date` are excluded from the regular model inputs. The sale date is used for chronological ordering in Time Series Split. The target variable is `house_price_inr`, while the remaining 9 property features are used as predictors.

## 🛠️ Technologies and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

## ⚙️ Project Workflow

1. Load and inspect the dataset.
2. Check data types, missing values, and duplicate records.
3. Separate input features and target variable.
4. Split data into training and testing sets.
5. Apply feature scaling using StandardScaler.
6. Implement Ridge and Lasso Regression.
7. Perform hyperparameter tuning using GridSearchCV.
8. Apply different cross-validation techniques.
9. Implement Decision Tree and Random Forest Regression.
10. Implement Linear and RBF Support Vector Regression.
11. Compare models using regression evaluation metrics.
12. Analyze overfitting and underfitting.
13. Prepare the final model comparison and conclusion.

## 🤖 Regression Models

### 1. Regularized Linear Models

**Ridge Regression (L2):** Applies a squared-coefficient penalty to reduce model complexity and prevent overfitting.

**Lasso Regression (L1):** Applies an absolute-coefficient penalty and can eliminate less important features by reducing their coefficients to zero.

### 2. Tree-Based Regression Models

**Decision Tree Regression:** Predicts house prices by dividing data into smaller groups using feature-based conditions.

**Random Forest Regression:** Combines multiple decision trees and averages their predictions to improve stability and prediction performance.

### 3. Support Vector Regression (SVR)

**Linear Kernel:** Models linear relationships between input features and house prices.

**RBF Kernel:** Captures nonlinear relationships using the Radial Basis Function kernel.

## 🔄 Cross-Validation Techniques

The project explores four cross-validation methods:

**K-Fold Cross-Validation:** Divides the dataset into K folds and uses each fold for validation once.

**Stratified K-Fold:** Maintains a similar distribution of house-price ranges across folds by binning the target variable.

**Leave-One-Out Cross-Validation (LOOCV):** Uses one observation for validation and all remaining observations for training.

**Time Series Split:** Preserves chronological order by using earlier records for training and later records for validation.

## 🎯 Hyperparameter Tuning

GridSearchCV is used to find suitable model parameters.

- Ridge and Lasso: Alpha
- Decision Tree: Max depth, minimum samples split, and minimum samples leaf
- SVR: C, Gamma, and Epsilon

Hyperparameter tuning helps improve model performance and control model complexity.

## 📊 Evaluation Metrics

The models are evaluated using the following regression metrics:

| Metric | Purpose |
|---|---|
| MAE | Average absolute prediction error |
| MSE | Average squared prediction error |
| RMSE | Square root of MSE, expressed in the target's units |
| R² Score | Proportion of target variation explained by the model |

For regression, R² is a performance metric; it is not classification accuracy.

## 📈 Model Comparison Results

| Model | MSE | R² Score |
|---|---:|---:|
| Ridge Regression | 6.5454 × 10¹² | 0.9187 |
| Lasso Regression | 6.5441 × 10¹² | 0.9187 |
| Decision Tree | 8.1680 × 10¹² | 0.8986 |
| Random Forest | 5.8427 × 10¹² | 0.9275 |
| Linear SVR | 8.0689 × 10¹³ | -0.0019 |
| RBF SVR | 8.0772 × 10¹³ | -0.0029 |

### 🏆 Best Performing Model

Random Forest Regression achieved the best performance among the evaluated models.

- **MSE:** 5.8427 × 10¹²
- **R² Score:** 0.9275

It achieved the lowest prediction error and explained approximately 92.75% of the variation in house prices on the test dataset.

## 📉 Overfitting and Underfitting Analysis

The project compares training and testing errors to understand model generalization.

**Underfitting:** The model performs poorly on both training and testing data.

**Overfitting:** The model performs very well on training data but noticeably worse on unseen testing data.

**Good Generalization:** The model performs well on testing data with a reasonably small training-testing performance gap.

## 🎯 Key Learning Outcomes

- Understanding regularization using Ridge and Lasso.
- Implementing different cross-validation techniques.
- Understanding tree-based regression algorithms.
- Working with Linear and RBF Support Vector Regression.
- Performing hyperparameter tuning using GridSearchCV.
- Evaluating regression models using appropriate metrics.
- Identifying possible overfitting and underfitting.
- Comparing linear and nonlinear regression approaches.

## 🔮 Future Improvements

- Experiment with additional regression algorithms.
- Improve SVR performance through feature and parameter optimization.
- Perform more extensive hyperparameter tuning.
- Use advanced ensemble methods such as Gradient Boosting and XGBoost.
- Deploy the selected model through a web application.
- Build an interactive house price prediction dashboard.
