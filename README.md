Weather Forecasting using Machine Learning

This project focuses on building a multivariate time-series machine learning model to forecast daily temperature using several weather-related features.
The dataset includes the following columns:

Temperature

Humidity

Wind Speed

Cloud Cover

Pressure

Rain (rain / no rain)

The goal is to analyze the weather data, engineer meaningful features, train ML models, and generate short-term forecasts.

Project Overview

The notebook includes the following steps:

1. Data Cleaning

Converted all feature values to numeric where necessary

Encoded the Rain column (rain → 1, no rain → 0)

Filled missing values using forward/backward filling

Assigned a proper date index to create a time series

2. Exploratory Analysis

Temperature trend visualization

Rolling mean and rolling standard deviation

Seasonal decomposition to understand trend and seasonality

3. Feature Engineering

Lag features (1, 3, 7, and 14 days)

Rolling averages over 7, 14, and 30 days

Lagged versions of exogenous variables

Final dataset constructed for model training

4. Machine Learning Models

Two supervised learning models were used for forecasting:

Random Forest Regressor

XGBoost Regressor

5. Evaluation

Models were evaluated using:

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

6. Forecasting

A simple 7-day ahead temperature forecast was generated using the trained XGBoost model.

Results

Both models performed reasonably well, with XGBoost producing slightly smoother and more stable predictions.
The notebook includes:

Actual vs Predicted temperature plot

Comparison table of MAE and RMSE

A 7-day future forecast plot

Files Included

weather_forecast.ipynb — Main notebook containing full implementation

weather_forecast_data.csv — Dataset used for the project (optional to upload)

How to Run

Clone the repository

Open the notebook in Jupyter Notebook or Google Colab

Install required packages (XGBoost, scikit-learn, pandas, etc.)

Run all the cells sequentially

Notes

This project uses ML-based forecasting rather than classical methods like ARIMA.

The model can be extended with neural networks (LSTM/GRU), hyperparameter tuning, or deployment through Streamlit.

The focus of this repository is to demonstrate understanding of time-series ML workflows, feature engineering, and model evaluation.

Possible Future Improvements

Add an LSTM or GRU deep learning model

Add automated hyperparameter tuning

Deploy the model using a simple Streamlit application

Include additional weather features for improved accuracy
