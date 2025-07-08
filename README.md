# MacroSignal

**MacroSignal** is a machine learning-based framework for extracting and evaluating macroeconomic signals as alpha factors for U.S. equity selection.

## Project Highlights

- Use macroeconomic indicators (e.g., GDP growth, CPI, unemployment, interest rate spread, ISM) as **non-traditional alpha factors**
- Construct stock-level factor exposures based on macro data
- Evaluate predictive power using IC, IR, and long-short portfolio backtests
- Compare macro factors with traditional value/momentum factors
- Fully reproducible, modular, and academic-oriented
  
## Project Structure
```
MacroSignal/
├── data/                     
│   ├── macro_data/              # Raw macroeconomic data (e.g., GDP, CPI, interest rates) in CSV or Parquet format
│   ├── stock_data/              # Equity market data (e.g., prices, volumes, market cap from Yahoo, Quandl, etc.)
│   └── processed/               # Cleaned and merged datasets used for modeling
│
├── features/                   
│   ├── macro_factor_construction.ipynb  # Construct macro factor exposures, e.g., mapping GDP growth to industries
│   ├── exposure_mapping.py              # Map macro indicators to stock- or sector-level exposure matrices
│   └── factor_summary_stats.py          # Calculate IC, IR, volatility, and distribution stats for macro factors
│
├── model/                     
│   ├── return_prediction.ipynb         # Train models (XGBoost, Random Forest, Lasso) to predict future returns
│   ├── macro_factor_model.py           # Define model pipeline, structure, training procedure, and hyperparameters
│   └── models/                         # Saved model files, checkpoints, and predictions
│
├── backtest/                 
│   ├── backtest_evaluation.ipynb       # Backtest performance and visualize cumulative returns, turnover, Sharpe ratio
│   ├── portfolio_simulator.py          # Simulate portfolios using equal-weight, factor-weighted, or IC-weighted schemes
│   └── performance_metrics.py          # Compute IC, IR, max drawdown, win rate, and other evaluation metrics
│
├── notebooks/                
│   ├── exploratory_macro.ipynb         # Explore relationships between macro variables and stock returns
│   ├── macro_vs_traditional.ipynb      # Compare macro-driven factors with traditional alpha factors
│   └── signal_stability.ipynb          # Analyze signal stability and robustness over time
│
├── utils/                    
│   ├── data_loader.py                  # Load and align macro and stock data; support frequency conversion
│   ├── factor_utils.py                 # Normalize, winsorize, and preprocess macro factors
│   └── visualization.py                # Plot factor returns, correlation matrices, heatmaps, and performance charts
│
├── LICENSE                             # License file (e.g., MIT License)
└── README.md                           # Project overview, methodology, usage instructions, and documentation

```

## Installation

To install the project and its dependencies, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/AnAAnnie/MacroSignal.git
   cd MacroSignal
   ```
2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```
3. If you prefer, you can create a virtual environment:
   ```python -m venv venv
   source venv/bin/activate  # On Windows, use venv\Scripts\activate
   pip install -r requirements.txt
   ```
## Usage
After the installation, you can start working with the notebooks to train the model or analyze the data:
  1. Data preparation: data_preparation.ipynb will help you clean and prepare the stock and macroeconomic data.
  2. Feature Engineering: factor_engineering.ipynb allows you to create key financial and macroeconomic factors for stock prediction.
  3. Model Training: Use return_prediction.ipynb for training machine learning models like XGBoost and Random Forest to predict stock returns.
  4. Backtesting: Evaluate the performance of your models with backtest_evaluation.ipynb.

## Citation
If you use this framework in your research, please cite it as follows:
```bibtex
@misc{MacroSignal2025,
  title={MacroSignal: Extracting Predictive Macroeconomic Signals for U.S. Equity Alpha Generation},
  author={Qing(Sunny) Luo},
  year={2025},
  url={https://github.com/AnAAnnie/MacroSignal}
}
```
## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements
Special thanks to the following projects that helped shape MacroSignal:
  1. XGBoost
  2. Random Forest
  3. Macroeconomic Data from FRED and Quandl

