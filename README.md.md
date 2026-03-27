
# Car Price Prediction

This project aims to **predict the price of used cars** based on key features using **XGBoost Regressor**. 

## Features Used
- **Year of Manufacturing**
- **Engine Size (L)**
- **Fuel Type**
- **Car Brand (Make)**
- **Car Model**
- **Car Age** (calculated as 2024 - Year)

## Dataset
The dataset contains car listings from 2010 to 2020 with features including price, engine size, fuel type, make, and model.

## Steps in the Project
1. **Data Loading & Cleaning** – convert types, handle missing values, and create new features.
2. **Exploratory Data Analysis (EDA)** – visualizing price distribution, engine size vs price, and price by brand.
3. **Feature Encoding** – convert categorical features using one-hot encoding.
4. **Train-Test Split** – split the dataset into training and testing sets.
5. **Model Training** – using XGBoost Regressor with tuned hyperparameters.
6. **Model Evaluation** – using MAE (Mean Absolute Error) and R² score.
7. **Feature Importance** – visualize the top features that affect car prices.
8. **Prediction Function** – a function `predict_car_price()` to predict the price of any car based on input features.

## Example Usage

```python
from predict import predict_car_price  # if you separate the function in a module

price = predict_car_price(2020, 2.0, "Petrol", "Toyota", "Camry")
print(f"Predicted Price: ${price:,.2f}")