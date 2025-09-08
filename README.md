# Stock Price Prediction with LSTM & GRU

## Abstract
This project focuses on stock price prediction using recurrent neural networks (LSTM and GRU) applied to financial time series. Historical data from Apple Inc., enriched with technical indicators, were used to build and evaluate the models. A linear regression model was implemented as a baseline for initial comparison. 

The methodology included comprehensive data preprocessing, temporal sequence generation, and hyperparameter optimization using Grid Search, considering window size, recurrent units, batch size, and learning rate. Models were evaluated using metrics such as MSE and MAE, and differences between LSTM and GRU were analyzed. 

Results indicate that GRU models outperformed LSTM in terms of accuracy, showing lower MSE and MAE, aligning with prior research highlighting GRU efficiency in capturing temporal dependencies. Both models showed significant improvements compared to linear regression.

The critical analysis highlighted limitations such as the lack of external variable integration and reliance on a limited dataset. Future research is suggested to explore hybrid models and additional data sources, such as sentiment analysis and macroeconomic factors, to enhance predictive performance. 

In conclusion, the study validates the effectiveness of recurrent neural networks in stock price prediction and sets a foundation for future research in this domain.

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
