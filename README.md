# Marketing ROI Analysis - Simple Linear Regression

## Project Overview
This project analyzes the relationship between different marketing channels (TV, Radio, Social Media) and Sales. Using Python and `statsmodels`, we built a Simple Linear Regression model to identify the most impactful channel and provide data-driven budget recommendations.

## Key Findings
- **Best Predictor:** TV advertising shows a near-perfect correlation (0.999) with Sales.
- **ROI:** For every $1 spent on TV advertising, sales increase by approximately 3.56 units.
- **Model Accuracy:** The R-squared value of 0.999 indicates the model explains 99.9% of the variance in sales.

## Technical Implementation
1. **Data Cleaning:** Handled missing values in the marketing dataset.
2. **EDA:** Performed correlation analysis and visualization using Seaborn.
3. **Regression:** Built an Ordinary Least Squares (OLS) model using `statsmodels`.
4. **Diagnostics:** Verified linearity, normality of residuals (Q-Q plots), and homoscedasticity.

## Setup Instructions
To run this analysis locally, install the following dependencies:
```bash
pip install pandas matplotlib seaborn statsmodels scipy
```

## Conclusion
Based on the statistical evidence, we recommend prioritizing the marketing budget toward TV advertising to maximize ROI.
