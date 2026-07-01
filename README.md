# House Price Predictor

An end-to-end machine learning pipeline predicting house prices using real King County, USA housing data. Built as part of my preparation for an MSc in Data Science and the Anthropic Fellows Program.

## Project Overview
This project explores, cleans, and models a real estate dataset of 21,613 home sales to predict sale price based on property features. Three regression models are compared — Linear Regression, Random Forest, and Gradient Boosting.

## Dataset
King County House Sales dataset — sourced from Kaggle.
Download: kaggle.com/datasets/harlfoxem/housesalesprediction
Place the CSV in the `data/` folder as `kc_house_data.csv` to reproduce this project.

## Notebooks

| Notebook | Description |
|----------|-------------|
| `01_eda.ipynb` | Exploratory data analysis — distributions, correlations, key drivers of price |
| `02_cleaning.ipynb` | Data cleaning, outlier removal, feature engineering |
| `03_model.ipynb` | Regression modelling — Linear Regression, Random Forest, Gradient Boosting |

## Results

| Model | MAE | RMSE | R² |
|-------|-----|------|----|
| Linear Regression | $43,494 | $61,888 | 0.908 |
| Gradient Boosting | $12,707 | $17,913 | 0.992 |
| Random Forest | $2,731 | $7,464 | 0.999 |

Random Forest achieved the highest R² of 0.9987 — explaining 99.87% of price variance. Note: this near-perfect score may indicate overfitting and would require cross-validation in production.

## Key Findings
- `price_per_sqft` and `sqft_living` were the most important features
- Ensemble methods massively outperformed Linear Regression
- House prices are non-linear — complex models capture this better
- Feature engineering directly contributed to model performance

## Feature Engineering
New features created in `02_cleaning.ipynb`:
- `house_age` — years since built
- `was_renovated` — binary flag for renovation history
- `price_per_sqft` — price relative to living space
- `total_rooms` — combined bedrooms and bathrooms

## Stack
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebooks
