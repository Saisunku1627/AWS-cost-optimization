# AWS Infrastructure Cost Prediction

Predict monthly AWS infrastructure costs using machine learning to enable proactive budget planning and cost optimization.

## Problem Statement

AWS infrastructure costs can spike unexpectedly due to changing usage patterns, new services, and misconfigurations.  
The goal of this project is to build a model that predicts future monthly AWS costs from historical usage so teams can plan budgets and identify optimization opportunities.

## Dataset

- Synthetic or anonymized AWS usage and billing data at monthly or daily granularity  
- Features: service-wise spend (EC2, S3, RDS, Lambda, etc.), usage hours, storage, data transfer, and account metadata  
- Target: total monthly AWS cost (USD)

## Approach

1. Performed exploratory data analysis to understand trends, seasonality, and main cost drivers.  
2. Engineered features such as lagged costs, rolling statistics, service-level aggregates, and normalized usage metrics.  
3. Trained baseline models (e.g., Linear Regression, Random Forest, Gradient Boosting) and tuned hyperparameters with cross-validation.  
4. Selected the best model using MAE / RMSE on a held-out test set.  
5. Interpreted feature importances to highlight actionable cost optimization levers.

## Results

- Best model: **Random Forest Regressor** (200 estimators, 100K training samples)  
- Achieved **MAE = $28,457** and **RMSE = $75,226** on held-out test set  
- Model explains **5.7% of cost variance** (R² = 0.057), indicating baseline performance with room for feature engineering improvements  
- Identified **Normalization Size Factor (59.8%)**, vCPU (15.4%), and Memory (5.7%) as top cost drivers  
- Analysis revealed **up to 42% regional cost savings** potential by migrating workloads to 
