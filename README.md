# E-Commerce Customer Churn Prediction

Predict whether an e-commerce customer will churn using behavioral and transactional features. This project includes exploratory analysis, preprocessing, baseline modeling, and evaluation with actionable business insights.

## Project Overview

Customer churn is costly for e-commerce businesses. The goal of this project is to:
- explore churn patterns,
- build a predictive model to identify customers at risk,
- and highlight the strongest churn drivers to support retention strategies.

## Dataset

- **File:** `ecommerce_customer_churn_dataset.csv`
- **Rows:** 50,000 customers
- **Target:** `Churned` (1 = churned, 0 = not churned)
- **Feature types:** demographics, engagement/behavior, transactions, and customer service interactions.

## Repository Contents

- `ecommerce_customer_churn (1).ipynb` — main notebook (analysis + modeling)
- `ecommerce_customer_churn_dataset.csv` — dataset
- `README.md` — project description and instructions
- `LICENSE` — license info
- `.gitignore` — git ignore rules

> Recommended cleanup: rename `ecommerce_customer_churn (1).ipynb` to `ecommerce_customer_churn.ipynb` for a more professional filename.

## How to Run

### Option 1 — Run locally (Jupyter)

1. Clone the repo and enter the folder:
   ```bash
   git clone https://github.com/Rowan123204/ecommerce-customer-churn.git
   cd ecommerce-customer-churn
   ```

2. (Recommended) Create a virtual environment:
   ```bash
   python -m venv .venv
   # macOS/Linux
   source .venv/bin/activate
   # Windows (PowerShell)
   .venv\Scripts\Activate.ps1
   ```

3. Install dependencies (create `requirements.txt` if you don’t have one yet):
   ```bash
   pip install -r requirements.txt
   ```

4. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook
   ```

### Option 2 — Run in Google Colab

1. Open the notebook in GitHub.
2. Click “Open in Colab” (or upload the notebook to Colab).
3. Ensure `ecommerce_customer_churn_dataset.csv` is available in the runtime:
   - upload it manually, or
   - mount Google Drive, or
   - clone the repo inside Colab.

## Workflow Summary

1. **Exploratory Data Analysis (EDA)**
   - Check distributions, missing values, and churn rate
   - Visualize churn patterns across key segments

2. **Data Preprocessing**
   - Impute missing values (median for numeric, mode for categorical)
   - Encode categorical variables (one-hot encoding)
   - Scale numeric features (StandardScaler)

3. **Modeling**
   - Train/test split
   - Baseline model: Logistic Regression
   - (Optional) Compare against tree-based models (e.g., Random Forest)

4. **Evaluation**
   - Confusion matrix
   - Classification report (precision, recall, F1-score)
   - Accuracy
   - (Recommended additions) ROC-AUC / PR-AUC, threshold tuning

## Key Insights (from analysis)

Common churn drivers found in this dataset include:
- **Days_Since_Last_Purchase**: inactivity is strongly associated with churn
- **Customer_Service_Calls**: frequent support calls may indicate dissatisfaction
- **Returns_Rate** and **Cart_Abandonment_Rate**: higher values correlate with churn
- **Engagement metrics** (login frequency, session duration): lower engagement increases churn risk

## Results (Baseline)

The notebook reports baseline classification metrics using Logistic Regression.
For churn problems, **recall for churned customers** is often especially important (catching as many likely churners as possible), so future improvements should focus on:
- class weighting / resampling,
- feature engineering,
- threshold tuning,
- and model comparison.

## Next Steps / Improvements (Recommended)

- Add `requirements.txt` for full reproducibility
- Add a script version (`ecommerce_customer_churn.py`) so it can be run from the command line
- Hyperparameter tuning (GridSearchCV / RandomizedSearchCV)
- Address class imbalance (e.g., `class_weight="balanced"`, SMOTE)
- Add ROC-AUC / PR-AUC and calibration checks
- Model interpretability: permutation importance or SHAP values
- Package the model as a small API (FastAPI) or batch scoring pipeline

## License

See `LICENSE`.

## Contact

If you have questions or suggestions, please open an issue in this repository.n issue or contact [Rowan123204/github].
