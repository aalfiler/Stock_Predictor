# Deep Learning - LSTM Stock Predictor

### Background

Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the [Crypto Fear and Greed Index (FNG)](https://alternative.me/crypto/fear-and-greed-index/) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. You have been asked to help build and evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.

In this project will use deep learning recurrent neural networks to model bitcoin closing prices. One model will use the FNG indicators to predict the closing price while the second model will use a window of closing prices to predict the nth closing price.

### Files

[Closing Prices Notebook](Analysis/lstm_stock_predictor_closing.ipynb)

[FNG Notebook](Analysis/lstm_stock_predictor_fng.ipynb)

### Objectives

- Use the FNG values to try and predict the closing price.
- Use previous closing prices to try and predict the next closing price. 
- Each model will need to use 70% of the data for training and 30% of the data for testing.
- Apply a MinMaxScaler to the X and y values to scale the data for the model.
- Reshape the X_train and X_test values to fit the model's requirement of samples, time steps, and features. 

### Summary performance of each model:

- Which model has a lower loss?
  - The LSTM model where we fit the data using only closing prices

- Which model tracks the actual values better over time?
  - The model where we fit using closing prices did slightly better at tracking actual values over time
  
- Which window size works best for the model? 
  - window_size = 10
