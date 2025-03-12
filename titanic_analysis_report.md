# Titanic Dataset Analysis Report

## 1. Introduction
The Titanic dataset provides information about the passengers aboard the Titanic, including demographic details, ticket information, and survival status. The objective of this analysis is to identify key factors that influenced survival rates using data cleaning techniques and exploratory data analysis (EDA). The study focuses on univariate, bivariate, and multivariate analysis to derive meaningful insights from the data.

---

## 2. Data Cleaning
### 2.1 Handling Missing Values
- `Age`: 177 missing values were **imputed with the median (28.0)** to preserve the distribution.
- `Embarked`: 2 missing values were **filled with the most frequent value ('S')**.
- `Deck`: 688 missing values led to its **removal due to excessive missing data**, avoiding potential bias.
- `Embark_town`: 2 missing values, **dropped as it duplicated information found in 'Embarked'**.

### 2.2 Removing Duplicates
- **116 duplicate rows** were detected and removed, reducing the dataset size from **891 to 775 rows**.

### 2.3 Standardizing Categorical Variables
- Typos and inconsistencies in categorical columns such as `Sex`, `Embarked`, and `Class` were corrected.
- Ensured uniform formatting to maintain data consistency and integrity.

---

## 3. Exploratory Data Analysis (EDA)

### 3.1 Univariate Analysis
#### Summary of Numerical Features:
| Feature   | Mean  | Median | Std Dev | Min | Max |
|-----------|-------|--------|---------|-----|-----|
| Age       | 27.7  | 28.0   | 12.0    | 0.42| 58.0|
| Fare      | 19.1  | 13.0   | 14.4    | 0.0 | 69.5|
| SibSp     | 0.52  | 0.0    | 1.03    | 0   | 8   |
| Parch     | 0.40  | 0.0    | 0.85    | 0   | 6   |

#### Categorical Feature Distribution:
- **Sex:** Around **65% male**, **35% female**.
- **Pclass:** **Third class passengers were the majority (~55%)**.
- **Embarkation:** Most passengers embarked from **Southampton (~75%)**.

### 3.2 Bivariate Analysis
#### Correlation Matrix of Numerical Features:
- **Fare & Pclass**: Strong **negative correlation (-0.55)** → Higher-class passengers paid higher fares.
- **Age & Survival**: Weak correlation, suggesting that age alone was not a strong predictor of survival.

#### Survival Rate by Key Features:
| Feature  | Survival Rate |
|----------|--------------|
| Female   | **73%** |
| Male     | **18%** |
| 1st Class| **63%** |
| 3rd Class| **24%** |
| Embarked C | **55%** |
| Embarked S | **33%** |

Key Findings:
- **Women had significantly higher survival chances than men**.
- **First-class passengers had a much better survival rate than third-class passengers**.
- **Passengers embarking from Cherbourg (C) had the highest survival rate**.

### 3.3 Multivariate Analysis
#### Combined Effects of Class, Gender, and Fare
- **First-class women had the highest survival rate (~96%)**.
- **Men in third class had the lowest survival rate (~13%)**.
- **Higher fares correlated with better survival rates, particularly among women**.
- **Family size (SibSp + Parch) influenced survival, with small family groups faring better than individuals or large families**.

---

## 4. Conclusion
- **Women and first-class passengers had the highest survival probabilities, aligning with the "women and children first" evacuation protocol**.
- **Men, particularly those in third class, had the lowest survival rates**.
- **Embarkation location played a role, with Cherbourg passengers experiencing better survival odds, possibly due to a higher proportion of first-class travelers**.
- **Fare and class were strong determinants of survival, reflecting a socioeconomic advantage**.
- **Family size had a non-linear effect on survival—passengers with small families had better odds compared to solo travelers or those in large families**.

This structured analysis provides a comprehensive understanding of survival determinants on the Titanic, reinforcing the historical narratives of the disaster while offering a statistical perspective.

