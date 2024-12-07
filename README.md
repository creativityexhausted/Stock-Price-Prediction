# Stock Price Prediction using Random Forest Regressor

# Overview
This project implements a stock price prediction model for Tesla using historical stock data. The model uses various technical indicators, including Simple Moving Averages (SMA), Relative Strength Index (RSI), and lagged values of the closing price as features. The model is built using a Random Forest Regressor and is evaluated using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared.

# Features
Technical Indicators:

SMA_50: 50-period Simple Moving Average

SMA_200: 200-period Simple Moving Average

RSI: Relative Strength Index
Lagged Features:
Close_lag1: Previous day's closing price
Close_lag2: Closing price two days ago
Random Forest Regressor: Predicts the closing price using the engineered features.
Dataset
The dataset used is Tesla's stock price, stored in a CSV file (tesla.csv), which should include at least the following columns:

Date: The date of the stock price record.
Close: The closing price of Tesla's stock.
Requirements
Dependencies:
The following Python libraries are required to run the program:

pandas
numpy
scikit-learn
matplotlib
Install them using pip:

bash
Copy code
pip install pandas numpy scikit-learn matplotlib
Usage
1. Load Data
The stock price data is read from a CSV file (tesla.csv), which should contain historical Tesla stock data with a Close column representing daily closing prices.

2. Feature Engineering
The program calculates two key moving averages (SMA_50 and SMA_200) for technical analysis.
The RSI (Relative Strength Index) is calculated for the stock prices.
Lagged Features are added, which represent the previous day’s and two days ago’ closing prices.
3. Train-Test Split
The data is split into training and test sets with an 80-20 split ratio.
4. Scaling the Features
The features are scaled using StandardScaler to normalize the data before training the model.
5. Model Training
A Random Forest Regressor is trained on the scaled data.
6. Predictions and Evaluation
Predictions are made on the test set, and the model's performance is evaluated using the following metrics:
Mean Absolute Error (MAE)
Mean Squared Error (MSE)
Root Mean Squared Error (RMSE)
R-squared (R²)
Percentage Accuracy: A measure of how close the predicted values are to the actual values, calculated as 1 - mean absolute percentage error.
7. Visualization
A plot of the actual vs. predicted closing prices is shown to visually assess the model's performance.
Example Output
When you run the program, the following evaluation metrics will be printed:

makefile
Copy code
MAE: <value>
MSE: <value>
RMSE: <value>
R-squared: <value>
Accuracy: <value>%
The plot showing the actual vs. predicted closing prices will also be displayed.

Folder Structure
bash
Copy code
StockPricePrediction/
├── tesla.csv               # Tesla stock price data (CSV)
├── stock_prediction.py     # Main script for training and prediction
└── README.md               # Project documentation
Model Performance
The model performance is evaluated using several metrics:

MAE (Mean Absolute Error): Measures the average magnitude of errors in predictions.
MSE (Mean Squared Error): Measures the average squared difference between predicted and actual values.
RMSE (Root Mean Squared Error): A measure of the average magnitude of the error.
R² (R-squared): Indicates how well the model explains the variance in the target variable.
Contributing
If you would like to contribute to this project, feel free to fork the repository, make changes, and submit a pull request.

