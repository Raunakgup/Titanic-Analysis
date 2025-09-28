# Titanic Dataset Analysis

## Project Overview
This project analyzes the Titanic dataset to understand the factors that influenced passenger survival. The analysis includes data cleaning, exploratory data analysis (EDA), and statistical insights to identify key determinants of survival.

## Dataset Information
The dataset contains the following key features:
- **Survival**: (0 = No, 1 = Yes)
- **Pclass**: Ticket class (1st, 2nd, 3rd)
- **Sex**: Passenger gender
- **Age**: Passenger age
- **SibSp**: Number of siblings/spouses aboard
- **Parch**: Number of parents/children aboard
- **Fare**: Ticket fare paid
- **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

## Steps Performed
### 1. Data Cleaning
- Handled missing values by imputing the median (`Age`) and mode (`Embarked`), while removing excessive missing data (`Deck`).
- Removed **116 duplicate rows**.
- Standardized categorical values to ensure consistency.

### 2. Exploratory Data Analysis (EDA)
- **Univariate Analysis:** Summary statistics, histograms, and box plots.
- **Bivariate Analysis:** Correlation matrices, scatter plots, and survival rate comparisons.
- **Multivariate Analysis:** Pair plots, heatmaps, and grouped survival comparisons.

### 3. Key Findings
- **Women and first-class passengers had the highest survival rates.**
- **Men, particularly those in third class, had the lowest survival rates.**
- **Embarkation location played a role, with Cherbourg passengers having better survival chances.**
- **Fare and class were strong survival determinants, highlighting socioeconomic advantages.**
- **Family size had a non-linear effect on survival, where small families had better survival odds than solo travelers or large families.**

## Requirements
To run this analysis, install the following dependencies:
```bash
pip install pandas seaborn matplotlib numpy
```

## How to Run
1. Open the Jupyter Notebook (`titanic_analysis.ipynb`).
2. Run all the cells to execute the data cleaning and analysis.
3. View generated visualizations and insights in the output.

## Repository Structure
```
📂 Titanic-Analysis
│── titanic_analysis.ipynb  # Jupyter Notebook with full code
│── titanic_analysis_report.md               # Detailed report of findings
│── titanic_analysis_readme.md               # Project summary and instructions
```

## GitHub Upload Instructions
To upload this project to GitHub, use the following commands:
```bash
git init
git add .
git commit -m "Added Titanic dataset analysis"
git branch -M main
git remote add origin <your_github_repo_link>
git push -u origin main
```
