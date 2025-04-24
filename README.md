# Car-Price-Prediction-USA-Market
Car price prediction model for a Chinese car manufacturing company to enter into US Market


## Project Overview

This project involves building a regression model to predict car prices based on various car specifications. The analysis is tailored for a Chinese automobile company aiming to enter the US market and understand how pricing is influenced by technical and categorical features of cars.

## Business Objective

The goal is to:
- Identify significant variables that affect the pricing of cars in the American market.
- Develop predictive models to estimate car prices.
- Help stakeholders make informed decisions for product design and market positioning.

## Dataset

- **Source**: CarPrice_Assignment.csv
- **Size**: 10,000+ rows, 15+ columns
- **Type**: Tabular dataset with both categorical and numerical features

## Tech Stack Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

## Steps Followed

### 1. Data Loading and Preprocessing
- Handled missing values, duplicates
- Encoded categorical features using One-Hot Encoding
- Scaled numeric features for models like SVR

### 2. Model Implementation
Implemented and evaluated the following regression models:
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regressor (SVR)

### 3. Model Evaluation
Models were evaluated using:
- R-squared (R²)
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)

| Model                   | R² Score | MSE         | MAE      |
|------------------------|----------|-------------|----------|
| Linear Regression       | -4000568319853787468529664.00 | Extremely high | Extremely high |
| Decision Tree Regressor| 0.9268   | 5,865,943.98 | 1,659.58 |
| Random Forest Regressor| **0.9443**   | **4,464,372.70** | **1,242.00** |
| Gradient Boosting      | 0.9370   | 5,043,739.86 | 1,369.23 |
| SVR                    | -0.0984  | 87,968,534.92| 5,626.30 |

### 4. Feature Importance
- The most influential features were: `engine-size`, `horsepower`, `curb-weight`, `make`, and `car-body`.

### 5. Hyperparameter Tuning
- Tuned `Random Forest Regressor` using GridSearchCV
- Final R² after tuning: **0.9497**

## Insights

- Car price is strongly correlated with technical features like engine size, horsepower, and brand.
- Random Forest performed best due to its ability to handle non-linear relationships and feature interactions.
- Hyperparameter tuning led to further performance improvement.

## Conclusion

This model serves as a robust tool for predicting car prices in the US market and offers actionable insights for vehicle design and pricing strategies.

## Folder Structure
- Dataset: CarPrice_Assignment.csv
- Notebook: Car_Price_Prediction.ipynb
