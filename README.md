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

- Best model: Random Forest Regressor  
- Achieved strong predictive performance on held-out test data  
- Identified key drivers of cost spikes such as EC2 on-demand hours, data transfer, and storage growth

## Project Structure

- `notebooks/aws_infrastructure_cost_prediction.ipynb` – main end-to-end notebook  
- `src/` – (optional) reusable Python modules for data loading, feature engineering, and model training  
- `models/` – saved model artifacts (kept small; large models stored outside Git)  
- `reports/` – generated figures or summary reports  
- `data/` – local data directory (excluded from Git to avoid large files)

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Saisunku1627/AWS-cost-optimization.git
   cd AWS-cost-optimization
   ```
2. (Optional) Create and activate a virtual environment, then install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the main notebook:
   ```bash
   jupyter notebook notebooks/aws_infrastructure_cost_prediction.ipynb
   ```
4. Configure the data path at the top of the notebook and run all cells.

## Tech Stack

- Python, pandas, NumPy, scikit-learn  
- Jupyter / Google Colab  
- AWS billing data and cloud cost concepts
