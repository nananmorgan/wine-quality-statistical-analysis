# Wine Quality Statistical Analysis

## Overview
Comprehensive exploratory data analysis and statistical modeling on the UCI Wine Quality dataset, comparing the chemical properties of 1,599 red wines and 4,898 white wines to understand what drives quality ratings.

## Key Findings
- Alcohol content is the strongest predictor of quality (Pearson correlation: 0.44), with a statistically significant permutation test (p-value: 0.0000)
- Red and white wines differ substantially in fixed acidity (Cohen's d: 1.29) and volatile acidity (Cohen's d: 2.00), but minimally in alcohol content (Cohen's d: -0.08)
- A multiple regression model using alcohol, residual sugar, pH, fixed acidity, and sulphates explained 22.1% of quality variability (adjusted R-squared: 0.221)
- Alcohol and sulphates emerged as the strongest predictors in the multi-variable model

## Methods
- **Descriptive statistics** with outlier detection using IQR for each chemical property
- **Cohen's d** effect sizes to compare red vs. white wine characteristics
- **PMFs and CDFs** (using thinkstats2) to visualize and compare distributions
- **Normal probability analysis** comparing empirical CDF to theoretical normal model
- **Pearson correlation and covariance** to quantify relationships between variables and quality
- **Permutation testing** to assess statistical significance of quality differences
- **Single and multiple linear regression** (OLS via statsmodels) to identify quality predictors

## Dataset
UCI Wine Quality dataset (ID: 186), containing physicochemical properties and quality ratings for Portuguese "Vinho Verde" wines. The dataset is fetched programmatically via the `ucimlrepo` library.

## Tools
Python, pandas, matplotlib, seaborn, scipy, statsmodels, thinkstats2, numpy

## Repository Contents
- `wine_quality_analysis.ipynb`    — Full analysis notebook
- `wine_quality_analysis.pdf`      — Rendered notebook output
- `project_presentation.pptx`      — Presentation slides
- `project_writeup.docx`           — Project write-up
- `winequality-red.csv` / `winequality-white.csv` — Source datasets

## How to Run
1. Install dependencies: `pip install pandas numpy matplotlib seaborn scipy statsmodels ucimlrepo thinkstats2`
2. Open the `.ipynb` notebook in Jupyter or VS Code and run all cells
