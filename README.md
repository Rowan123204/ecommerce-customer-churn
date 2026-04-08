# E-Commerce Customer Churn Prediction

Predict whether an e-commerce customer will churn using behavioral and transactional features. This project includes exploratory analysis (EDA), preprocessing, baseline modeling, and evaluation with actionable business insights.

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

- `ecommerce_customer_churn.ipynb` — main notebook (analysis + modeling)  
  *(If your repo still shows `ecommerce_customer_churn (1).ipynb`, rename it for a more professional filename.)*
- `ecommerce_customer_churn_dataset.csv` — dataset
- `requirements.txt` — Python dependencies
- `README.md` — project description and instructions
- `LICENSE` — license info
- `.gitignore` — git ignore rules

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

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook
   ```

### Option 2 — Run in Google Colab

1. Open the notebook in GitHub.
2. Download it or open it in Colab.
3. Ensure `ecommerce_customer_churn_dataset.csv` is available in the runtime:
   - upload it manually, or
   - mount Google Drive, or
   - clone the repo inside Colab.

## Workflow Summary

1. **Exploratory Data Analysis (EDA)**
   - Inspect distributions, missing values, and churn rate
   - Visualize churn patterns across key customer segments

2. **Data Preprocessing**
   - Impute missing values (median for numeric, mode for categorical)
   - Encode categorical variables (one-hot encoding)
   - Scale numeric features (StandardScaler)

3. **Modeling**
   - Train/test split
   - Baseline model: Logistic Regression
   - (Optional) Compare against tree-based models (e.g., Random Forest, Gradient Boosting)

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

For churn problems, **recall for churned customers** is often especially important (catching as many likely churners as possible). Future improvements should focus on:
- class weighting / resampling,
- feature engineering,
- threshold tuning,
- and model comparison.

## Next Steps / Improvements (Recommended)

- Improve reproducibility (pinned versions, configuration, script entry point)
- Hyperparameter tuning (GridSearchCV / RandomizedSearchCV)
- Address class imbalance (e.g., `class_weight="balanced"`, SMOTE)
- Add ROC-AUC / PR-AUC and calibration checks
- Model interpretability: permutation importance or SHAP values
- Package the model as a small API (FastAPI) or batch scoring pipeline

## License

See `LICENSE`.
MIT
## Contact
rowanaymn0284@gmail.com
If you have questions or suggestions, please open an issue in this repository.
