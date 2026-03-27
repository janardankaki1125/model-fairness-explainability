# Model Fairness, Bias & Explainability Analysis

Analysis of the Breast Cancer Classification model (Logistic Regression) using SHAP for interpretability.

## Deliverables
- `model_fairness_explainability.ipynb` → Main notebook with SHAP plots
- Feature importance analysis
- Global and local explanations using SHAP

## Key Findings

**Feature Importance:**
- Top features: `worst area`, `worst concave points`, `mean concave points` — medically relevant.

**SHAP Analysis:**
- Global: Shows which features push predictions toward malignant/benign.
- Local: Explains individual patient predictions.

**Bias Check:**
- Dataset has no explicit sensitive attributes (gender, race, age).
- No major proxy bias detected.
- Model relies on clinically accepted features → low risk of unfair bias.

## Mitigation Recommendations
1. Continuously monitor model performance across different patient demographics.
2. Use SHAP values in clinical decision support to increase doctor trust.
3. If sensitive attributes become available in future, perform group fairness checks (Equal Opportunity, Demographic Parity).
4. Consider ensemble methods or calibration for even better explainability.

## How to Run
Open `model_fairness_explainability.ipynb` in Google Colab or Jupyter Notebook.
