# Heart Disease Risk — EDA & Baseline Models

This repository contains a compact, reproducible analysis of the classic heart disease dataset and two baseline models (Linear Regression and Random Forest Regressor), plus a simple HTML intake form.

## Dataset

- **File:** `heart-1.csv`
- **Rows/Columns:** 303 × 14 (no missing values detected in the source analysis)  
- **Target:** `output` — 0 = low risk, 1 = high risk  
- **Features:** `age, sex, cp, trtbps, chol, fbs, restecg, thalachh, exng, oldpeak, slp, caa, thall`

> Feature meanings (short):  
> - `age`: age in years  
> - `sex`: 1 = male, 0 = female  
> - `cp`: chest pain type (1–4)  
> - `trtbps`: resting blood pressure (mm Hg)  
> - `chol`: serum cholesterol (mg/dl)  
> - `fbs`: fasting blood sugar > 120 mg/dl (1/0)  
> - `restecg`: resting ECG results (0–2)  
> - `thalachh`: max heart rate achieved  
> - `exng`: exercise induced angina (1/0)  
> - `oldpeak`: ST depression induced by exercise  
> - `slp`: slope of peak exercise ST segment  
> - `caa`: number of major vessels (0–3)  
> - `thall`: thalassemia (categorical encoding)

## What’s inside

- **`heart_disease_analysis.ipynb`** — loads the data, runs a quick EDA, trains LR & RF baseline regressors, reports MSE/R² and optional classification metrics via a 0.5 threshold.
- **`heart_form.html`** — a lightweight HTML form (no backend) to collect the same feature inputs as the dataset.

## Quick start

1. Ensure the `heart-1.csv` file is present in the repo root (or update the path in the notebook).
2. Open the notebook:
   ```bash
   pip install -r requirements.txt  # optional; see minimal deps below
   jupyter lab  # or jupyter notebook
   ```
3. Run all cells. You’ll get summary tables, quick visuals, and metrics for both models.

### Minimal dependencies

- Python ≥3.9
- pandas, numpy, scikit-learn, matplotlib

You can install them with:
```bash
pip install pandas numpy scikit-learn matplotlib
```

## Results (baseline, will vary with random state)

- Linear Regression: ~MSE ~0.098, R² ~0.60  
- Random Forest Regressor: ~MSE ~0.107, R² ~0.56

If you binarize predictions at 0.5 (for a **rough** classifier), you can compute accuracy, precision, recall, F1, and a confusion matrix as demonstrated in the notebook.

## Notes

- These are **baseline** models for learning/replication. Try feature engineering, regularization, class-balancing methods, or stronger models (e.g., Gradient Boosting) to improve performance.
- The HTML form is front‑end only. Hook it up to a FastAPI/Flask endpoint or a cloud function to serve a trained model.

- 
