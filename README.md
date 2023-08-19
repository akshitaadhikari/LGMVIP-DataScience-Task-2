# LGMVIP-DataScience-Task-2
# Stock Market Prediction and Forecasting Using Stacked LSTM

This repository contains code and resources for predicting and forecasting stock market prices using Stacked LSTM.

## Code Example

```python
import pandas as pd
import numpy as np
from sklearn.preprocessing import MinMaxScaler
from keras.models import Sequential
from keras.layers import LSTM, Dense, Dropout

# Load and preprocess data
data = pd.read_csv('stock_data.csv')
# Preprocessing steps...

# Prepare training data
# ...

# Build the Stacked LSTM model
model = Sequential()
model.add(LSTM(units=50, return_sequences=True, input_shape=(x_train.shape[1], 1)))
model.add(LSTM(units=50, return_sequences=True))
model.add(LSTM(units=50))
model.add(Dense(units=1))

# Compile and train the model
model.compile(optimizer='adam', loss='mean_squared_error')
model.fit(x_train, y_train, epochs=epochs, batch_size=batch_size)

# Make predictions
predicted_stock_price = model.predict(x_test)
# ...

# Visualize the results
# ...

