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
LayeredAlpha/
├── data/                     # Raw data and processed datasets (macroeconomic & financial data)
│   ├── stock_data/           # Stock market data (Yahoo, Quandl, etc.)
│   └── macro_data/           # Macroeconomic data (GDP, CPI, etc.)
│
├── features/                 # Feature engineering scripts to extract relevant factors
│   ├── factor_engineering.ipynb   # Scripts for constructing key factors (PE, PB, ROE, etc.)
│   ├── factor_filtering.ipynb    # Factor filtering using Lasso, IC method
│
├── model/                    # Machine learning models for stock prediction
│   ├── return_prediction.ipynb    # Training XGBoost, Random Forest, etc. for return prediction
│   └── models/                   # Saved models and training outputs
│
├── backtest/                 # Backtesting and performance evaluation
│   ├── backtest_evaluation.ipynb   # Scripts for backtesting and comparing models
│
├── notebooks/                # Jupyter notebooks for exploratory analysis and experiments
│   ├── exploratory_analysis.ipynb  # Data exploration and initial analysis
│
├── utils/                    # Utility functions (data loaders, metrics, helpers)
│   ├── data_loader.py         # Functions for loading and cleaning data
│   ├── metrics.py             # Functions for calculating model evaluation metrics
│   └── helpers.py             # Helper functions used across the codebase
│
├── LICENSE                   # License file (e.g., MIT License)
└── README.md                 # Project overview and documentation

```

## Installation

```bash
git clone https://github.com/AnAAnnie/MacroSignal.git
cd MacroSignal
pip install -r requirements.txt
```

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

