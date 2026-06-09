# Marketing ROI Analysis Using Simple Linear Regression

## Project Overview

This project analyzes the relationship between marketing expenditures and sales performance using Simple Linear Regression. The objective is to determine which advertising channel has the strongest impact on sales and provide data-driven recommendations for marketing budget allocation.

Using Python, exploratory data analysis (EDA), and Ordinary Least Squares (OLS) regression, the analysis evaluates the predictive power of different marketing channels and identifies the channel most strongly associated with increased sales.

---

## Project Objectives

The goals of this project are to:

* Load and clean the marketing dataset
* Explore relationships between advertising channels and sales
* Identify the marketing channel most correlated with sales
* Build a Simple Linear Regression model using OLS
* Validate regression assumptions through diagnostic analysis
* Interpret model performance and statistical significance
* Provide actionable business recommendations for marketing investment

---

## Dataset Description

The dataset contains advertising expenditures across multiple marketing channels and corresponding sales performance.

### Features

| Variable     | Description                     |
| ------------ | ------------------------------- |
| TV           | TV advertising budget           |
| Radio        | Radio advertising budget        |
| Social Media | Social media advertising budget |
| Sales        | Product sales generated         |

---

## Exploratory Data Analysis (EDA)

The following analyses were performed:

* Data quality assessment
* Missing value inspection
* Distribution analysis using histograms
* Pairwise relationship analysis using pairplots
* Correlation analysis using a heatmap

The exploratory analysis revealed that TV advertising exhibited the strongest positive relationship with Sales and was therefore selected as the independent variable for the regression model.

---

## Model Development

A Simple Linear Regression model was developed using:

* Independent Variable (X): TV Advertising Spend
* Dependent Variable (Y): Sales

The model was implemented using the `statsmodels` OLS (Ordinary Least Squares) framework.

---

## Model Evaluation

The model was evaluated using:

* R-squared
* Regression coefficients
* p-values
* Residual analysis

### Diagnostic Checks

To verify the validity of regression assumptions, the following diagnostic plots were generated:

* Residuals vs Fitted Values (Linearity)
* Q-Q Plot (Normality)
* Scale-Location Plot (Homoscedasticity)
* Residual Distribution Histogram

Results indicated that the regression assumptions were reasonably satisfied.

---

## Key Findings

* TV advertising demonstrated the strongest correlation with sales.
* The regression model explained a substantial portion of sales variability.
* The TV coefficient was statistically significant (p < 0.05).
* Increased TV advertising expenditure was associated with increased sales performance.

---

## Business Recommendation

Based on the analysis, TV advertising appears to be the most influential marketing channel in predicting sales performance.

Organizations seeking to maximize marketing effectiveness should consider prioritizing TV advertising investments while continuing to monitor performance across other channels.

It is important to note that regression analysis identifies statistical associations and should not be interpreted as definitive proof of causation.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* Jupyter Notebook

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/marketing-roi-analysis.git
cd marketing-roi-analysis
```

Install required dependencies:

```bash
pip install pandas numpy matplotlib seaborn statsmodels
```

---

## Project Structure

```text
marketing-roi-analysis/
│
├── regression_analysis.ipynb
├── README.md
├── marketing_dataset.csv
└── requirements.txt
```

---

## Author

**Uwabor Collins**

Project/Operations Manager | Supplychain Analystics | Business Analyst

Passionate about using data, analytics, and technology to solve business problems and support strategic decision-making.
