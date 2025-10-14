# Telecom Customer Churn Prediction

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

- `churn_training.ipynb`: Complete analysis and model training notebook
- `churn_data.csv`: Generated synthetic dataset (10,000 records)
- `README.md`: Project documentation

## Technologies Used

- **Python**: pandas, numpy, scikit-learn
- **ML Libraries**: XGBoost, CatBoost, scikit-learn
- **Visualization**: matplotlib, seaborn
- **Model Evaluation**: ROC curves, Precision-Recall analysis

## Usage

1. Open `churn_training.ipynb` in Jupyter Notebook
2. Run all cells to reproduce the analysis
3. Use the trained model to predict churn for new customers

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
