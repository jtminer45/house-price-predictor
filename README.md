# House Price Predictor

An end-to-end machine learning pipeline predicting house prices using real King County, USA housing data. Built as part of my preparation for an MSc in Data Science and the Anthropic Fellows Program.

## Project Overview
This project explores, cleans, and models a real estate dataset of 21,613 home sales to predict sale price based on property features.

## Dataset
King County House Sales dataset — sourced from Kaggle.
Download: kaggle.com/datasets/harlfoxem/housesalesprediction
Place the CSV in the `data/` folder as `kc_house_data.csv` to reproduce this project.

## Progress

| Notebook | Description |
|----------|-------------|
| `01_eda.ipynb` | Exploratory data analysis — distributions, correlations, key drivers of price |

## Key Findings (EDA)
- House prices are heavily right-skewed
- `sqft_living` is the strongest predictor of price (+0.70 correlation)
- `grade` (build quality) is the second strongest predictor (+0.67 correlation)
- Location (zipcode) drives significant price variation independent of house features
- Waterfront properties command a clear price premium

## Stack
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (upcoming — modelling stage)
- Jupyter Notebooks

## Next Steps
- Data cleaning and feature engineering
- Regression modelling (Linear Regression, Random Forest, Gradient Boosting)
- Model evaluation and comparison
