**LSTM Time Series - Multivariate Stock Price Prediction for Reliance Industries**

This project implements a multivariate time series analysis using RNN/LSTM to predict stock prices of Reliance Industries Limited (RELIANCE.NS). A deep RNN model was trained on five years of historical Reliance stock data to forecast performance over a two-month period.

**Dataset (Reliance Industries Stock Price)**

The dataset comprises historical records of Reliance Industries' stock prices (NSE: RELIANCE.NS), sourced from Yahoo Finance. It includes:

Opening price

Highest price

Lowest price

Closing price

Adjusted closing price

Trading volume

**Data Splits:**

Training data: Jan 2019 – June 2023

Validation data: July 2023 – Dec 2023

Testing data: First two months of 2024

Implementation Phases
PHASE 1 - Exploratory Data Analysis
Notebook: data-exploratory-analysis.ipynb

Download and load raw Reliance stock data.

Analyze summary statistics and historical trends (2019–2024).

Clean data (handle missing values, validate types).

Filter and save the dataset for the target period.

PHASE 2 - Data Preprocessing
Notebook: data-preprocessing.ipynb

Load filtered Reliance data.

Select features: Open, High, Low, Close, Volume.

Split into training (70%), validation (20%), and testing (10%).

Scale data to  range using MinMaxScaler (fit on training data).

Save processed splits to data/processed/.

PHASE 3 - Model Training & Inference
Notebook: `model-training.ipynb**

Model Architecture (TensorFlow Sequential):

Input layer with 60-timestep sequences

4× LSTM layers (100 units each)

4× Dropout layers (rate=0.3)

Dense output layer (1 unit)

Training:

Optimizer: Adam

Loss: Mean Squared Error

Epochs: 200 | Batch size: 64

Predictions:

Forecast prices for training, validation, and test periods.

Inverse-scale predictions to original price range.

Visualize results (actual vs. predicted).

Key Results
Predictions captured Reliance’s price trends, including consolidation phases and breakout patterns.

Model achieved low validation loss (MSE) and generalized well to unseen test data.

