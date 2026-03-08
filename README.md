# E-commerce Customer Churn Prediction

End-to-end ML pipeline for predicting e-commerce customer churn. This project demonstrates a complete data science workflow — from raw data cleaning and exploratory analysis through feature engineering to model training and evaluation — to identify at-risk customers and the key factors driving attrition.

## Skills Demonstrated

Data Cleaning | EDA | Feature Engineering | Machine Learning | Binary Classification | Logistic Regression | Random Forest | Gradient Boosting | scikit-learn | Model Evaluation | Business Insights

## Pipeline Overview

```
Raw Data (.xlsx) --> Data Quality Assessment --> EDA (8+ visualizations)
    --> Data Cleaning & Preprocessing --> Feature Engineering (5 new features)
    --> Train/Test Split & Scaling --> Model Training (3 models)
    --> Evaluation & Comparison --> Business Recommendations
```

## Dataset

**E-commerce Customer Churn Analysis and Prediction** from [Kaggle](https://www.kaggle.com/datasets/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction).

- **5,630 customers** with 20 features
- Demographics, order behavior, satisfaction scores, complaint history
- Binary target: Churn (1) vs Non-Churn (0)

## Key Findings

1. **16.8% churn rate** -- nearly 1 in 6 customers left the platform
2. **New customers are most vulnerable** -- tenure under 3 months has the highest churn rate; the first 90 days are the critical retention window
3. **Complaints are the strongest churn signal** -- customers who filed complaints churn at ~3x the rate of those who didn't
4. **Delivery distance matters** -- greater warehouse-to-home distance is associated with higher churn, suggesting logistics friction drives customers away

## Model Performance

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| Logistic Regression | 0.8961 | 0.7664 | 0.5526 | 0.6422 |
| Gradient Boosting | 0.9583 | 0.9181 | 0.8263 | 0.8698 |
| **Random Forest** | **0.9787** | **0.9826** | **0.8895** | **0.9337** |

Random Forest achieved the best overall performance with an F1-score of 0.93, balancing precision and recall effectively.

## Top Churn Factors

Based on Gradient Boosting feature importance:

1. **Tenure / TenurePerAddress** -- customer maturity and stability
2. **CashbackAmount** -- loyalty program engagement
3. **Complain** -- unresolved customer issues
4. **NumberOfAddress** -- account instability indicator
5. **DaySinceLastOrder** -- recency of engagement

## Project Structure

```
ecommerce-churn-prediction/
|-- data/
|   |-- raw/                  # Original dataset (.xlsx)
|   +-- processed/            # Cleaned dataset (.csv)
|-- notebooks/
|   +-- churn_prediction.ipynb  # Full analysis notebook
|-- README.md
+-- requirements.txt
```

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ecommerce-churn-prediction.git
   cd ecommerce-churn-prediction
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Open and run the notebook:
   ```bash
   jupyter notebook notebooks/churn_prediction.ipynb
   ```
   Run all cells sequentially. The notebook will load data from `data/raw/`, process it, and save cleaned data to `data/processed/`.
