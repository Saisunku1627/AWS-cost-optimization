# AWS Infrastructure Cost Prediction

Predict AWS infrastructure costs using machine learning to enable proactive budget planning and cost optimization.

## Problem Statement
AWS infrastructure costs can spike unexpectedly, making it difficult to forecast budgets and control spend. This project builds a model that predicts monthly AWS costs from usage patterns so teams can plan ahead and identify optimization opportunities.

## Dataset
- Source: [briefly describe: e.g. simulated AWS Cost Explorer export]
- Time period: [e.g. Jan 2023 – Dec 2025]
- Rows: [approx number of records]
- Features: compute hours, storage (GB), data transfer (GB), region, instance type, etc.
- Target: Monthly total cost (USD)

## Approach
- Cleaned raw usage and billing data.
- Engineered features (lags, rolling averages, utilization ratios).
- Trained a Random Forest regressor to predict monthly cost.
- Evaluated using RMSE, MAE, R², and inspected feature importance.

## Results
- RMSE: $[value]
- MAE: $[value]
- R²: [value]
- Key drivers of cost: [e.g. data_transfer_gb, storage_gb, compute_hours].

## Project Structure
- `data/` – raw and cleaned data (or a note if data is not included)
- `notebooks/` – EDA and modeling notebooks
- `src/` – Python modules for data prep, feature engineering, training, prediction
- `models/` – saved model artifacts
- `reports/` – business summary, figures

## How to Run
1. Install dependencies: `pip install -r requirements.txt`
2. Run training: `python src/train.py`
3. Use `src/predict.py` to generate cost predictions for new data.

## Future Work
- Deploy model as an API (Flask/FastAPI).
- Add automated retraining pipeline.
- Compare with XGBoost / time-series models.
