
# Car Insurance Claim Prediction

## Project Overview
This project predicts whether a car insurance policyholder will file a claim based on demographic, behavioral, and vehicle-related features. The goal is to help insurance companies identify high-risk customers and price policies more accurately.

## Research Question
**Can we predict whether a car insurance policyholder will file a claim using features such as driving experience, age, vehicle type, and credit score?**

## Dataset
- **Source:** [Car Insurance Data — Kaggle (sagnik1511)](https://www.kaggle.com/datasets/sagnik1511/car-insurance-data)
- **Size:** ~10,000 rows
- **Target Variable:** `OUTCOME` — 1 if a claim was filed, 0 if not
- **Key Features:** AGE, GENDER, DRIVING_EXPERIENCE, VEHICLE_TYPE, CREDIT_SCORE, VEHICLE_OWNERSHIP, ANNUAL_MILEAGE

## Repository Structure
```
├── README.md
├── capstone_eda.ipynb        # Main EDA and baseline model notebook
├── data/
│   └── Car_Insurance_Claim.csv
└── images/                   # Saved plots (optional)
```

## Methodology
1. **Data Cleaning** — handled missing values via median/mode imputation, removed duplicates
2. **EDA** — visualized distributions, claim rates by category, correlations
3. **Feature Engineering** — encoded categorical variables, created AGE_GROUP and EXP_RISK features
4. **Baseline Modeling** — Logistic Regression with StandardScaler

## Results
### EDA Findings
- Younger drivers (under 25) show higher claim rates than experienced drivers
- Lower credit scores are associated with higher claim likelihood
- Driving experience is one of the strongest predictors of claim behavior
- Vehicle ownership status and annual mileage also show meaningful differences in claim rates

### Baseline Model Performance
| Metric | Score |
|--------|-------|
| Accuracy | [fill in after running] |
| ROC-AUC | [fill in after running] |

**Evaluation Metric Rationale:** ROC-AUC was selected as the primary metric because:
- It is robust to class imbalance
- It evaluates model performance across all classification thresholds
- In insurance, missing high-risk customers (false negatives) is costly — AUC captures this better than accuracy alone

## Tools and Libraries
- Python 3.11
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

## Link to Notebook
[capstone_eda.ipynb](./capstone_eda.ipynb)
