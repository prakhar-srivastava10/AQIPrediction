Air Quality Index (AQI) Prediction – README
🔍 Project Overview
This project aims to predict Air Quality Index (AQI) values using machine learning techniques based on environmental data (e.g., PM2.5 levels) from Indian cities. Accurate AQI prediction helps authorities and the public to take preventive steps against air pollution.

🎯 Objectives
Load and clean air quality data.

Use time-based features (hour, day, etc.) to help with prediction.

Create a regression model to predict AQI (PM2.5 used as a proxy).

Visualize pollution trends and model performance.

📊 Dataset Used
File: station_hour.csv.xlsx

Features include: Datetime, PM2.5, City, etc.

Focused on Delhi city data for prediction.

🔧 Steps Performed
Data Upload
Manually upload the Excel dataset using Google Colab’s files.upload() method.

Data Cleaning

Convert Datetime column to datetime format.

Remove missing values.

Filter only Delhi city records.

Sort data by time.

Feature Engineering

Extract Hour, Day, Month, and Year from datetime.

Create lag features: PM2.5_lag1, PM2.5_lag24.

Calculate 24-hour rolling average of PM2.5.

Modeling

Use Linear Regression to predict PM2.5.

Train on 80% of the data and test on the remaining 20%.

Evaluate with metrics like MAE (Mean Absolute Error) and RMSE (Root Mean Squared Error).

Visualization

Plot PM2.5 trends over time.

Boxplots by hour.

Daily average trends.

Compare actual vs predicted PM2.5 values.

🧠 Algorithm Used: Linear Regression (Simple Explanation)
Linear Regression tries to fit a straight line through the data points. It finds a formula to estimate the next value of AQI based on previous values.
In this project, we used:

PM2.5 from the previous hour (lag1)

PM2.5 from the same hour yesterday (lag24)

24-hour average (rolling24)

📈 Evaluation Metrics
MAE – How much we are wrong on average.

RMSE – Like MAE, but gives more importance to big errors.

R² Score – Shows how well the model explains the variation in AQI.

✅ Conclusion
The model helps in forecasting PM2.5 levels in Delhi using past data. It can be extended to other cities and improved using more advanced models like Random Forest or LSTM for better time-series forecasting.
