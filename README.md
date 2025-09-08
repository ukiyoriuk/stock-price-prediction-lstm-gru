# Stock Price Prediction with LSTM & GRU

## Abstract
This project focuses on stock price prediction using recurrent neural networks (LSTM and GRU) applied to financial time series. Historical data from Apple Inc., enriched with technical indicators, were used to build and evaluate the models. A linear regression model was implemented as a baseline for initial comparison. 

The methodology included comprehensive data preprocessing, temporal sequence generation, and hyperparameter optimization using Grid Search, considering window size, recurrent units, batch size, and learning rate. Models were evaluated using metrics such as MSE and MAE, and differences between LSTM and GRU were analyzed. 

Results indicate that GRU models outperformed LSTM in terms of accuracy, showing lower MSE and MAE, aligning with prior research highlighting GRU efficiency in capturing temporal dependencies. Both models showed significant improvements compared to linear regression.

The critical analysis highlighted limitations such as the lack of external variable integration and reliance on a limited dataset. Future research is suggested to explore hybrid models and additional data sources, such as sentiment analysis and macroeconomic factors, to enhance predictive performance. 

In conclusion, the study validates the effectiveness of recurrent neural networks in stock price prediction and sets a foundation for future research in this domain.

## Features
- Data preprocessing: normalization and technical indicators.
- Models: LSTM and GRU for time series forecasting.
- Metrics: MSE, MAE, RMSE.
- Visualization of predictions vs. real stock prices.
- Executed Jupyter Notebook with saved outputs.

## Project Structure

```
├── data
│ ├── aapl_normalized_with_indicators.csv
│ ├── aapl_normalized.csv
│ ├── aapl_visualization.png
│ ├── aapl_with_indicators.csv
│ ├── aapl.csv                                # Input data 
│ └── linear_regression_baseline.png
├── docs                                      # Thesis (PDF) and presentation (PPTX)
│ ├── presentacion.pptx
│ └── TFG.pdf
├── README.md
├── requirements-apple-silicon.txt
├── requirements-generic.txt
└── stock_prediction.ipynb
```

## Data
- `aapl.csv`: raw Apple stock prices dataset.  
- `aapl_with_indicators.csv`: prices + technical indicators.  
- `aapl_normalized.csv`: normalized prices.  
- `aapl_normalized_with_indicators.csv`: normalized dataset with indicators.  

All CSVs are included in `data/` for full reproducibility.

## Notebook
- **Executed notebook**: [`stock_prediction.ipynb`](stock_prediction.ipynb) already contains outputs (plots, metrics, predictions).  
- To re-run it:
  1. Create environment (see below).  
  2. Install dependencies.  
  3. Open the notebook in VSCode or Jupyter and select the correct kernel.  
  4. Run all cells.

## Environment & Requirements

### Apple Silicon
```bash
conda create -n stocks python=3.10 -y
conda activate stocks
pip install -r requirements-apple-silicon.txt
python -m ipykernel install --user --name=stocks --display-name "Python (stocks)"
```

### Generic (Linux/Windows/Intel Mac)
```bash
conda create -n stocks python=3.10 -y
conda activate stocks
pip install -r requirements-generic.txt
python -m ipykernel install --user --name=stocks --display-name "Python (stocks)"
```

Then, in VSCode/Jupyter:
- Select kernel: **Python (stocks)**  
- Run the notebook

📄 The full thesis is available in [`/docs/TFG.pdf`](docs/TFG.pdf).  
🎞️ The final presentation is available in [`/docs/presentacion.pptx`](docs/presentacion.pptx).

## License
 
- **Documents (thesis & slides)**: CC BY-NC-ND 3.0 ES (as stated in the thesis front page).

## Author

- Álvaro Lafuente (*ukiyoriuk*)  
- Bachelor in Computer Science – Universitat Oberta de Catalunya (UOC)  
- Focused on AI, ML, and Data Engineering.
