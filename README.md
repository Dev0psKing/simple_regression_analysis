# Simple Linear Regression Analysis: Marketing ROI

## 📊 Project Overview

This project performs a comprehensive **Simple Linear Regression Analysis** on a marketing dataset to identify which advertising channel (TV, Radio, or Social Media) has the strongest impact on Sales. The analysis includes exploratory data analysis (EDA), model building, assumption testing, and business recommendations for marketing budget allocation.

### Key Objectives
✅ Load and clean marketing dataset with missing value handling
✅ Perform exploratory data analysis (EDA) with visualizations  
✅ Identify the independent variable with strongest correlation to Sales
✅ Build an Ordinary Least Squares (OLS) regression model
✅ Test regression assumptions using diagnostic plots
✅ Validate model reliability and statistical significance
✅ Generate actionable ROI-based recommendations for marketing strategy

---

## 📁 Project Structure

```
simple_regression_analysis/
├── regression_analysis.ipynb                 # Main Jupyter notebook with full analysis
├── README.md                                 # This file
├── Simple linear regression mini project.csv # Dataset (4,573 records)
│
├── Output Files (Generated after running notebook):
│   ├── 01_distribution_plots.png            # Distribution of variables
│   ├── 02_correlation_heatmap.png           # Correlation matrix visualization
│   ├── 03_scatter_plots.png                 # Scatter plots with trend lines
│   ├── 04_diagnostic_plots.png              # Regression assumption tests (6 plots)
│   ├── 05_prediction_intervals.png          # Fitted line with confidence intervals
│   ├── ANALYSIS_REPORT.txt                  # Detailed text report
│   ├── regression_results_summary.csv        # Key metrics summary table
│   └── channel_correlations.csv              # Channel correlations with sales
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.7 or higher
- Jupyter Notebook or JupyterLab
- Required packages (see Installation section)

### Installation

#### 1. Clone/Download Repository
```bash
cd simple_regression_analysis
```

#### 2. Create Virtual Environment (Recommended)
```bash
# Using venv
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

#### 3. Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn statsmodels scipy jupyter
```

Or create a `requirements.txt` file:
```
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
statsmodels>=0.13.0
scipy>=1.7.0
jupyter>=1.0.0
```

Then install:
```bash
pip install -r requirements.txt
```

#### 4. Launch Jupyter Notebook
```bash
jupyter notebook regression_analysis.ipynb
```

---

## 📊 Dataset Information

### File: `Simple linear regression mini project.csv`

**Data Structure:**
| Column | Description | Data Type | Non-null Count |
|--------|-------------|-----------|---|
| TV | TV advertising spending | float64 | ~1,900 |
| Radio | Radio advertising spending | float64 | ~1,900 |
| Social_Media | Social media advertising spending | float64 | ~1,900 |
| Sales | Sales revenue | float64 | ~1,900 |

**Summary:**
- Total Records: 4,573
- Records with missing values: ~2,800
- Clean records after removal: ~1,700-1,800
- Handling: Rows with ANY missing value are removed

---

## 📋 Analysis Workflow

### Step 1-3: Data Preparation
- Load CSV dataset
- Identify and quantify missing values
- Remove rows with NaN values
- Verify data quality of clean dataset

### Step 4-6: Exploratory Data Analysis
- Descriptive statistics (mean, std, skewness, kurtosis)
- Distribution plots for all variables
- Correlation matrix calculation
- Heatmap visualization of correlations

### Step 7-9: Model Development
- Rank variables by correlation strength
- Select best predictor of Sales
- Fit OLS regression model
- Extract regression coefficients and statistics

### Step 10-12: Assumption Testing
- Linearity check (Residuals vs Fitted)
- Normality test (Q-Q plot, Shapiro-Wilk test)
- Homoscedasticity test (Scale-Location, Breusch-Pagan)
- Autocorrelation test (Durbin-Watson)
- Outlier detection and analysis

### Step 13-17: Insights & Recommendations
- Generate predictions for different scenarios
- Confidence and prediction intervals
- Business case analysis
- Marketing budget allocation recommendations

---

## 📈 Key Regression Model

**General Form:**
```
Sales = β₀ + β₁ × Best_Predictor + ε
```

Where:
- β₀ = Intercept (baseline sales)
- β₁ = Slope (sales increase per unit of predictor)
- ε = Residual error

**Metrics Reported:**
- R² (Coefficient of Determination)
- Adjusted R²
- F-statistic and p-value
- Coefficients with t-statistics and p-values
- Confidence intervals for coefficients

---

## 🔍 Regression Assumptions Tested

1. **Linearity**: Is the relationship linear?
   - Method: Residual plot inspection
   - Visual check: Points should scatter randomly around zero line

2. **Normality**: Are residuals normally distributed?
   - Tests: Shapiro-Wilk test, Q-Q plot
   - Expected: p-value > 0.05 (fail to reject null hypothesis of normality)

3. **Homoscedasticity**: Is variance constant?
   - Test: Breusch-Pagan test, Scale-Location plot
   - Expected: No systematic pattern in residuals

4. **Autocorrelation**: Are residuals independent?
   - Test: Durbin-Watson statistic
   - Expected: DW ≈ 2 (range 1.5-2.5 acceptable)

5. **No Multicollinearity**: (Not applicable for simple regression)

6. **Outlier Detection**: Are there extreme values?
   - Method: Standardized residuals > |3|
   - Expected: < 1% of observations

---

## 📊 Output Files Generated

### Visualizations (PNG)
- **01_distribution_plots.png**: Histograms of all 4 variables
- **02_correlation_heatmap.png**: Color-coded correlation matrix
- **03_scatter_plots.png**: 3 scatter plots with trend lines and r values
- **04_diagnostic_plots.png**: 6 diagnostic plots (residuals, Q-Q, etc.)
- **05_prediction_intervals.png**: Fitted line with confidence/prediction bands

### Data Files (CSV)
- **regression_results_summary.csv**: Key model metrics table
- **channel_correlations.csv**: Correlation rankings of channels

### Reports (TXT)
- **ANALYSIS_REPORT.txt**: Comprehensive findings and recommendations

---

## 💡 How to Interpret Results

### R-squared (R²)
```
R² = 0.678 → Model explains 67.8% of sales variation
       ↑ Better model fit
       ↓ Other factors also influence sales
```

### P-values
```
p < 0.001 → Highly significant ✓✓✓
p < 0.05  → Significant at 95% confidence ✓
p > 0.05  → Not significant ✗
```

### Confidence Interval (95%)
```
Coefficient: 2.89 [2.81, 2.97]
→ We're 95% confident the true effect lies between 2.81 and 2.97
```

### Prediction Interval (95%)
```
Wider than confidence interval
→ Individual predictions have more uncertainty than mean
```

---

## 🎯 Business Applications

### 1. Budget Allocation
Identify which channel to fund more aggressively based on ROI metrics

### 2. Forecasting
Predict expected sales for different spending levels

### 3. Sensitivity Analysis
Understand how changes in spending affect sales

### 4. Performance Monitoring
Track actual vs. predicted sales monthly

### 5. Strategic Planning
Make data-driven marketing mix decisions

---

## ⚠️ Important Limitations

1. **Correlation ≠ Causation**
   - High correlation doesn't prove one variable causes changes in another
   - Could be a third variable affecting both

2. **Linearity Assumption**
   - Model assumes linear relationship
   - May not work for non-linear data
   - Consider polynomial regression if relationship is curved

3. **Past ≠ Future**
   - Historical patterns may not continue
   - Market conditions change
   - External shocks can alter relationships

4. **Data Quality**
   - ~38% of data removed due to missing values
   - Results only valid for complete data

---

## 🔄 Recommendations for Use

1. ✅ Run notebook quarterly with fresh data
2. ✅ Compare predictions vs. actual outcomes monthly
3. ✅ Validate findings with domain experts
4. ✅ Monitor R² to ensure model maintains predictive power
5. ✅ Consider multivariate regression for more complex relationships
6. ⚠️ Don't make major decisions based solely on this model
7. ⚠️ Always consider external factors (competition, seasonality, etc.)

---

## 📚 Technologies & Libraries

| Tool | Purpose |
|------|---------|
| Python 3.7+ | Programming language |
| Pandas | Data manipulation & cleaning |
| NumPy | Numerical computations |
| Matplotlib | Basic plotting |
| Seaborn | Statistical visualizations |
| Statsmodels | OLS regression & diagnostics |
| SciPy | Statistical tests |
| Jupyter | Interactive notebook environment |

---

## 🎓 Learning Outcomes

After running this project, you will understand:
- ✓ Data loading and cleaning workflows
- ✓ Exploratory data analysis techniques
- ✓ Simple linear regression theory and practice
- ✓ Regression assumption testing
- ✓ Statistical interpretation of p-values and R²
- ✓ Confidence and prediction intervals
- ✓ Business decision-making with data science
- ✓ Professional presentation of analytical findings

---

## 📧 Questions & Support

### For Statistical Questions:
- See interpretation guide section above
- Consult statsmodels documentation
- Review diagnostic plots carefully

### For Data/Code Issues:
- Check that all packages are installed correctly
- Ensure dataset file is in correct location
- Review error messages carefully

### For Business Application:
- Discuss results with marketing team
- Validate assumptions with domain experts
- Consider piloting recommendations before full rollout

---

## 📄 Repository Contents

```
┌─ regression_analysis.ipynb (Main Analysis - Run this!)
├─ README.md (This file - Documentation)
├─ Simple linear regression mini project.csv (Input Data)
└─ Output/ (Generated after running notebook)
   ├─ PNG plots (5 visualization files)
   ├─ CSV summaries (2 data files)
   └─ TXT report (1 comprehensive report)
```

---

## ✅ Verification Checklist

Before starting analysis:
- [ ] Python 3.7+ installed
- [ ] All packages installed (see requirements.txt)
- [ ] Dataset file present in working directory
- [ ] Jupyter Notebook installed and working

After running notebook:
- [ ] No error messages in output
- [ ] All 5 PNG files generated
- [ ] 2 CSV files created with data
- [ ] ANALYSIS_REPORT.txt file created
- [ ] Review regression summary statistics
- [ ] Check diagnostic plots for assumption violations

---

**Status**: ✅ Production Ready
**Last Updated**: June 2026
**Python Version**: 3.7+
**Data Records**: ~1,700-1,800 (after cleaning)
