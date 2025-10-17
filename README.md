# Telecom Customer Churn Prediction

### Live link - https://web-app-churn-prediction-1.onrender.com/

A machine learning project to predict customer churn in the telecommunications industry using various classification algorithms.

## Overview

This project analyzes customer data to identify patterns that lead to customer churn and builds predictive models to help telecom companies retain customers proactively.

## Features

- **Data Analysis**: Comprehensive EDA with correlation heatmaps, churn rate analysis by demographics
- **Multiple Algorithms**: Logistic Regression, Random Forest, XGBoost, CatBoost, and more
- **Model Optimization**: Hyperparameter tuning and threshold optimization for improved precision
- **Visualization**: ROC curves, Precision-Recall curves, and performance metrics
- **Feature Engineering**: Missing value handling and categorical encoding

## Dataset Features

- **Demographics**: Age, Gender, Income
- **Usage**: Data usage (GB), Tenure (months)
- **Service**: Plan type (Prepaid/Postpaid), Number of complaints
- **Target**: Customer churn (0 = retained, 1 = churned)

## Key Insights

- **Plan Type Impact**: Prepaid customers show 28% churn rate vs 20% for Postpaid
- **Complaints Correlation**: Strong positive correlation between complaints and churn
- **Tenure Effect**: Longer tenure customers are less likely to churn
- **Model Performance**: Achieved 78.2% AUC with optimized Logistic Regression

## Model Performance

- **Best Model**: Tuned Logistic Regression
- **AUC Score**: 0.782
- **Average Precision**: 0.552
- **Key Features**: Complaints, tenure, plan type, usage patterns

## Files

- `BEST_MODEL.ipynb`: Main end-to-end notebook (training, tuning, export artifacts)
- `datasets/churn_data.csv`: Generated synthetic dataset (10,000 records)
- `README.md`: Project documentation

## Technologies Used

- **Python**: pandas, numpy, scikit-learn
- **ML Libraries**: XGBoost, CatBoost, scikit-learn
- **Visualization**: matplotlib, seaborn
- **Model Evaluation**: ROC curves, Precision-Recall analysis

## Streamlit App

A ready-to-run Streamlit app is provided to interactively predict churn for a single customer.

### Prerequisites

- Python 3.10+
- Recommended: a virtual environment

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Export Model Artifacts (if not already present)

Run the `BEST_MODEL.ipynb` to generate and save artifacts into `deployment/` (preferred) or `models/` directories. The app will automatically pick the latest artifacts.

Expected files:
- `deployment/best_model_*.pkl` (or `models/best_*.pkl`)
- `deployment/preprocessor_*.pkl` (or `models/enhanced_preprocessor.pkl`)
- `deployment/model_metadata_*.pkl` (optional)

### Run the App

```bash
streamlit run app.py
```

Open the URL shown in the terminal (typically `http://localhost:8501`).

### Notes

- The app recreates the same feature engineering used in training to ensure consistency.
- If a full pipeline was saved, it is used directly. Otherwise, the app loads the preprocessor and applies it before prediction.
- Artifacts are auto-discovered from `deployment/` first, then `models/` as a fallback.

## Business Impact

This model can help telecom companies:
- Identify high-risk customers for targeted retention campaigns
- Optimize customer service resources
- Reduce churn rates and improve customer lifetime value
- Make data-driven decisions about customer retention strategies

## Future Enhancements

- Real-time prediction API
- Customer segmentation analysis
- A/B testing framework for retention strategies
- Integration with CRM systems
