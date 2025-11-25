

# Weather Forecasting using Machine Learning

This project focuses on building a multivariate time-series model to forecast daily temperature using machine learning techniques. The dataset contains weather features such as humidity, wind speed, cloud cover, pressure, and rainfall. The objective is to analyze historical weather patterns, engineer time-dependent features, train ML models, and generate short-term temperature forecasts.

---

## Project Overview

### 1. Data Preparation

* Converted all feature columns to numeric formats
* Encoded the Rain column (rain → 1, no rain → 0)
* Handled missing values using forward and backward fill
* Created a date index to structure the data as a time series

### 2. Exploratory Analysis

* Visualized the overall temperature trend
* Computed rolling mean and rolling standard deviation
* Performed seasonal decomposition to understand trend and seasonality

### 3. Feature Engineering

* Lag features for temperature (1, 3, 7, 14 days)
* Rolling averages over 7, 14, and 30-day windows
* Lag features for other weather variables (humidity, wind speed, cloud cover, pressure, rain)
* Final dataset prepared for supervised learning

### 4. Machine Learning Models

Two machine-learning models were trained and evaluated:

* **Random Forest Regressor**
* **XGBoost Regressor**

### 5. Evaluation Metrics

Models were evaluated on:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)

A comparison table is included in the notebook.

### 6. Forecasting

A 7-day temperature forecast was generated using the trained XGBoost model.
Plots for actual vs predicted values and future forecasts are included.

---

## Repository Contents

* **weather_forecast.ipynb** — Main Jupyter/Colab notebook with full implementation
* **weather_forecast_data.csv** — Dataset used for training (optional to upload)

---

## How to Run the Project

1. Clone the repository
2. Open the notebook in Jupyter Notebook or Google Colab
3. Install required packages (XGBoost, scikit-learn, pandas, matplotlib, seaborn)
4. Run the notebook cells in order

---

## Notes

* The project uses machine-learning-based forecasting rather than classical ARIMA-based models.
* The pipeline demonstrates core time-series ML concepts including feature engineering, lag analysis, and rolling statistics.
* The workflow is suitable for academic submissions, ML portfolios, and entry-level AIML roles.

---

## Future Improvements

* Add an LSTM or GRU model for deep-learning-based forecasting
* Include automated hyperparameter tuning (Optuna or GridSearchCV)
* Build a simple Streamlit app for interactive forecasting
* Add additional weather features or external data sources

