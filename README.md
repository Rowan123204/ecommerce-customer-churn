# ecommerce-customer-churn
Predict and analyze customer churn in e-commerce using Python and ML.
# E-Commerce Customer Churn Prediction

Predict customer churn for an e-commerce platform using behavioral and transactional data.

---

## Project Overview

Churn is very costly for e-commerce businesses. This project analyzes customer churn patterns using a real-world dataset, builds machine learning models, and identifies key behaviors associated with churn. The goal is to predict which customers are at the highest risk of leaving so that retention efforts can be more targeted and effective.

---

## Dataset

- **File:** `ecommerce_customer_churn_dataset.csv`
- **Rows:** 50,000 customers
- **Features:** 25 columns including demographics, behavioral, transactional, and engagement data, and the target column:
  - `Churned` (1 if customer churned, 0 otherwise)

---

## Workflow

1. **Exploratory Data Analysis (EDA)**
    - Understand the data structure
    - Summary statistics and visualization (e.g., churn rate by gender, inactivity)
2. **Data Preprocessing**
    - Handle missing values (median for numeric, mode for categorical)
    - Remove duplicates
    - One-hot encode categorical features
3. **Modeling**
    - Train/test split (80/20)
    - Standardize numeric features
    - Train Logistic Regression and Random Forest Classifier
4. **Evaluation**
    - Confusion matrix, classification report (precision/recall/f1/accuracy)
    - Feature importance analysis (identify the most predictive features)
5. **Interpretability & Business Insights**
    - Key drivers of churn highlighted
    - Visualizations to communicate findings

---

## Key Insights

- **Days_Since_Last_Purchase** is the top churn predictor: inactive customers are most at risk.
- **Customer_Service_Calls** are closely linked to churn, indicating possible dissatisfaction.
- **Returns_Rate** and **Cart_Abandonment_Rate** are negative indicators and strongly correlate with leaving.
- **Engagement metrics** like Login Frequency and Session Duration matter; less engaged users churn more.
- No major churn rate difference between genders.

---

## Requirements

- Python 3.7+
- pandas, numpy, scikit-learn, matplotlib, seaborn

Install dependencies:
```bash
pip install -r requirements.txt
```

---

## Usage

**Notebook**  
Open and run `ecommerce_customer_churn.ipynb` (or the similarly-named file) in Jupyter/Colab.

**Script**  
For reproducibility or batch runs, use the `.py` version:
```bash
python ecommerce_customer_churn.py
```
Make sure `ecommerce_customer_churn_dataset.csv` is in the same directory.

---

## Files

- `ecommerce_customer_churn.ipynb` – Main Jupyter/Colab notebook with analyses and visualizations
- `ecommerce_customer_churn.py` – Script version (auto-generated from notebook)
- `ecommerce_customer_churn_dataset.csv` – The input data
- (Optional) Exported plots, model pickles, etc.

---

## Next Steps / Possible Improvements

- Hyperparameter tuning for optimal accuracy
- SMOTE or class weighting for imbalanced data
- Deploy as a scoring API or automated report service
- Deeper segmentation (by geography, tenure, etc.)

---

## License

MIT or your preferred license here.

---

## Contact

For questions or contributions, open an issue or contact [Rowaneissa/github].
