 # Stock-Price-Prediction

In this project, we aim to predict the closing stock price of Google for the next 30 days using historical stock price data. This project utilizes Long Short Term Memory (LSTM) networks, which are well-suited for time-series forecasting tasks due to their ability to capture long-term dependencies.


**Data Source**
The dataset used for this project was downloaded via Google Sheets using the GOOGLEFINANCE function. This function allows us to pull historical stock price data directly into a spreadsheet, making it easily accessible for analysis.


**Preprocessing**
We selected a lookback value of 75 days, meaning that the model considers the stock prices from the previous 75 days to predict the next day's closing price. The dataset was split into training, validation, and testing datasets, and the errors for each partition were evaluated using the Root Mean Square Error (RMSE) metric.


**Model Architecture**
The model consists of stacked Long Short Term Memory (LSTM) layers, specifically:

2 LSTM layers, followed by fully connected layers.
The LSTM model was chosen for its ability to handle time-series data and capture the patterns that influence stock prices over time.


**Evaluation Metrics**
The RMSE values for the different datasets are as follows:

Training Data: 0.02088\n
Validation Data: 0.03383\n
Testing Data: 0.04167\n
These values indicate that the difference between the true and predicted values is minimal, demonstrating that the model can predict the stock prices with a good degree of accuracy.


**Key Features**
Historical Data: The model was trained using past stock price data with a 75-day lookback window.
Next 30 Days Prediction: The model outputs the predicted stock prices for the next 30 days.
RMSE Evaluation: The performance of the model is evaluated using RMSE, indicating the accuracy across training, validation, and testing sets.


**Installation and Usage**
Clone the Repository:
git clone https://github.com/Audrik21242/Stock-Price-Prediction.git


**Install Dependencies:**

The project uses Python and the following major libraries:
TensorFlow/Keras: For building and training the LSTM model.
NumPy and Pandas: For data manipulation and preprocessing.
Matplotlib: For visualizing stock price trends.


**Future Improvements**
Feature Engineering: Introduce additional features such as volume, moving averages, or technical indicators to enhance model performance.
Other Models: Experiment with other time-series models like GRU, ARIMA, or even hybrid models combining LSTM with Convolutional layers for further improvement.
Fine-tuning: Perform hyperparameter tuning to further reduce RMSE.
