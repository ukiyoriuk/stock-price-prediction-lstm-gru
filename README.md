# Stock Price Prediction with LSTM & GRU

This repository contains my **Bachelor's Thesis (TFG)** project on **time series forecasting**.  
The goal is to predict Apple stock prices (AAPL) using **deep learning models (LSTM & GRU)** and compare their performance against a baseline linear regression model.

📄 The full thesis is available in [`/docs/TFG.pdf`](docs/TFG.pdf).  
🎞️ The final presentation is available in [`/docs/presentacion.pptx`](docs/presentacion.pptx).

## Project Structure

```
stock-price-prediction-lstm-gru/
├─ notebooks/              # Main Jupyter notebooks
│   └─ stock_prediction.ipynb
├─ data/                   # Input data 
├─ docs/                   # Thesis (PDF) and presentation (PPTX)
├─ .gitignore
└─ README.md
```

## Workflow

1. **Data**: Historical AAPL data (1980–2020)  
   - Normalized with MinMaxScaler  
   - Technical indicators added: SMA, EMA, RSI, Volatility, ATR

2. **Models**:
   - Baseline: Linear Regression
   - LSTM
   - GRU

3. **Evaluation**:
   - Train/test split
   - Loss: MSE (Mean Squared Error)
   - Metric: MAE (Mean Absolute Error)

## Results

| Model              | MSE (test) | MAE (test) |
|--------------------|-----------:|-----------:|
| Linear Regression  | 0.0020     | 0.0337     |
| LSTM               | 0.00116    | 0.0190     |
| GRU                | 0.00053    | 0.0187     |

➡️ **GRU performed best**, achieving lower MSE and MAE than LSTM and Linear Regression.

## How to Run

Clone the repository:
```bash
git clone https://github.com/ukiyoriuk/stock-price-prediction-lstm-gru.git
cd stock-price-prediction-lstm-gru
```

Create a virtual environment and install dependencies:
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Open the main notebook:
```bash
jupyter lab
```

## License
 
- **Documents (thesis & slides)**: CC BY-NC-ND 3.0 ES (as stated in the thesis front page).

## Author

- Álvaro Lafuente (*ukiyoriuk*)  
- Bachelor in Computer Science – Universitat Oberta de Catalunya (UOC)  
- Focused on AI, ML, and Data Engineering.
