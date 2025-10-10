# LSTM Stock Price Predictor

This is a Streamlit web application that predicts stock prices using a Long Short-Term Memory (LSTM) model. Users can select a stock from a predefined list or enter a custom ticker from Yahoo Finance. The application allows for hyperparameter tuning and will train a model live if a pre-trained version is not available.

## Features

*   **Stock Price Prediction:** Predicts the next day's closing price for a given stock.
*   **Live Model Training:** If a model with the selected parameters doesn't exist, it trains a new one on the fly.
*   **Hyperparameter Tuning:** Allows users to customize the LSTM model's parameters, including sequence length, hidden layer size, epochs, batch size, and learning rate.
*   **Data Visualization:** Displays a plot of the actual vs. predicted stock prices on the test set.
*   **Performance Metrics:** Evaluates the model's performance using RMSE (Root Mean Squared Error), MAPE (Mean Absolute Percentage Error), and SMAPE (Symmetric Mean Absolute Percentage Error).
*   **Feature Engineering:** Uses Simple Moving Average (SMA), Exponential Moving Average (EMA), and Relative Strength Index (RSI) to enhance the model's predictive power.
*   **Downloadable Assets:** Allows users to download the trained model (`.keras` file) and the prediction plot (`.png` file).

## Technologies Used

*   Python
*   Streamlit
*   TensorFlow
*   Pandas
*   NumPy
*   Matplotlib
*   Scikit-learn
*   yfinance

## Installation and Usage

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/stock-predictor.git
    cd stock-predictor
    ```

2.  **Create a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the application:**
    ```bash
    streamlit run app.py
    ```

## Project Structure

```
.
├── app.py                  # Main Streamlit application
├── config.py               # Configuration for model and plot paths
├── requirements.txt        # Python dependencies
├── render.yaml             # Deployment configuration for Render
├── models/                 # Directory for trained models
│   └── [TICKER]/           # Models for a specific stock
└── plots/                  # Directory for prediction plots
    └── [TICKER]/           # Plots for a specific stock
```

## Disclaimer

This is a tool for educational purposes and not financial advice. Always conduct your own thorough research before making any investment decisions. Stock market predictions are inherently uncertain, and past performance is not indicative of future results.
