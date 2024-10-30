# Stock Price Prediction
This project predicts Google’s closing stock price for the next 30 days using historical stock price data. Leveraging Long Short Term Memory (LSTM) networks, this model is well-suited for time-series forecasting due to its ability to capture long-term dependencies in the data.

# Table of Contents
1. Data Source
2. Preprocessing
3. Model Architecture
4. Evaluation Metrics
5. Key Features
6. Installation and Usage
7. Future Improvements

# Data Source
The dataset for this project was obtained via Google Sheets using the GOOGLEFINANCE function. This function provides easy access to historical stock price data by directly importing it into a spreadsheet, making it accessible and ready for analysis.

# Preprocessing
To prepare the data, a lookback value of 75 days was selected, meaning the model considers the stock prices from the previous 75 days to predict the next day's closing price. The dataset was split into training, validation, and testing sets, and evaluated with the Root Mean Square Error (RMSE) metric to assess model performance on each partition.

# Model Architecture
The model architecture includes stacked LSTM layers for effective time-series analysis:

2 LSTM Layers, followed by fully connected layers.<br/>
The LSTM architecture is designed to capture the temporal dependencies in stock prices, helping to reveal patterns that impact future prices.<br/>

# Evaluation Metrics
The RMSE values for different datasets are as follows:<br/>

Training Data: 0.02088<br/>
Validation Data: 0.03383<br/>
Testing Data: 0.04167<br/>
These RMSE values indicate a minimal difference between true and predicted values, showcasing the model’s effectiveness in accurately predicting stock prices.<br/>

# Key Features
Historical Data: Trains on past stock price data with a 75-day lookback window.<br/>
Next 30 Days Prediction: Outputs predictions for the next 30 days.<br/>
RMSE Evaluation: Assesses accuracy using RMSE across training, validation, and testing sets.<br/>

# Installation and Usage
Clone the Repository<br/>
git clone https://github.com/Audrik21242/Stock-Price-Prediction.git<br/>
Install Dependencies<br/>
<br/>
The project is built in Python and requires the following libraries:<br/>
TensorFlow/Keras: For building and training the LSTM model.<br/>
NumPy and Pandas: For data manipulation and preprocessing.<br/>
Matplotlib: For visualizing stock price trends.<br/>
<br/>
Install dependencies using:<br/>
pip install tensorflow numpy pandas matplotlib<br/>
<br/>

# Future Improvements
Feature Engineering: Incorporate additional features such as trading volume, moving averages, or technical indicators to enhance model performance.<br/>
Model Experimentation: Test alternative time-series models like GRU, ARIMA, or hybrid models combining LSTM with convolutional layers.<br/>
Hyperparameter Tuning: Perform tuning to further minimize RMSE and improve accuracy<br/>
