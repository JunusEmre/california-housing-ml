# California Housing — Price Prediction ML

Machine learning project for predicting California district housing values.
Built as a reproducible decision-support workflow for area valuation.

## Author
Yunus Emre Capar — Data Science student, EC Utbildning Sweden

## Python version
Python 3.11.9

## Project structure
## Project structure
california-housing-ml/
├── data/
│   └── raw/
│       └── housing.csv
├── notebooks/
│   └── housing_price_prediction_california.ipynb
├── reports/
│   └── figures/
│       ├── model_comparison.png
│       ├── final_model_evaluation.png
│       ├── feature_importance.png
│       ├── error_analysis.png
│       ├── pca_explained_variance.png
│       └── pca_2d.png
├── .gitignore
├── requirements.txt
└── README.md

## Setup
```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/california-housing-ml.git
cd california-housing-ml

# Create virtual environment
python -m venv .venv

# Activate (Windows)
.venv\Scripts\activate

# Activate (Mac/Linux)
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

## How to run

Open and run the notebook from top to bottom:
```
notebooks/housing_price_prediction_california.ipynb
```

Use **Kernel → Restart & Run All** to reproduce all results from scratch.

## Models compared
- Baseline (DummyRegressor)
- Linear Regression
- Random Forest ← selected model
- Gradient Boosting

## Final results
| Metric | Value |
|--------|-------|
| MAE    | $32,374 |
| RMSE   | $48,854 |
| R²     | 0.818 |

## Key findings
- `median_income` is the strongest predictor of house value
- Engineered ratio features outperformed raw count features
- Model performs best in the $100k–$300k price range
- PCA shows 4 components capture 80% of data variance
