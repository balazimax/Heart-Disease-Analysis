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

- <img width="695" height="448" alt="download (1)" src="https://github.com/user-attachments/assets/9cffc355-9272-4bd2-a56d-cd4e29f2cdfb" />
<img width="695" height="468" alt="download (2)" src="https://github.com/user-attachments/assets/cbf5bfde-d160-4493-8228-aeea3cd18442" />
<img width="571" height="432" alt="download (3)" src="https://github.com/user-attachments/assets/53dc4558-5ad5-4aa9-adfb-25a095f63dc8" />
<img width="576" height="432" alt="download (4)" src="https://github.com/user-attachments/assets/72ffbaeb-43c1-4afe-bc71-2fc86d8dc53e" />
<img width="695" height="468" alt="download (5)" src="https://github.com/user-attachments/assets/0d165b22-8065-48a0-b230-f353a286b1a6" />
<img width="571" height="432" alt="download (6)" src="https://github.com/user-attachments/assets/c7fe6103-fb31-4da6-bdae-ca4cbc2a9d1f" />
<img width="571" height="432" alt="download (7)" src="https://github.com/user-attachments/assets/99833fd6-1eb4-45f6-a369-ebe196f091b2" />
<img width="543" height="413" alt="download (8)" src="https://github.com/user-attachments/assets/b02892d2-9e77-4cb6-8886-25563096cfcf" />
<img width="552" height="413" alt="download (10)" src="https://github.com/user-attachments/assets/85484d91-68ae-4371-946f-e2bfa9879812" />
<img width="1490" height="989" alt="download (11)" src="https://github.com/user-attachments/assets/d196398d-e2e9-4ee1-a3b5-7a8ccc6933e2" />
<img width="1490" height="590" alt="download (12)" src="https://github.com/user-attachments/assets/fef79eef-61ea-427f-9f26-0ebd10557e28" />
<img width="3435" height="3436" alt="download (13)" src="https://github.com/user-attachments/assets/e78611d4-d4b0-406e-b6c5-e7f8f7deb7c4" />
<img width="1276" height="511" alt="download" src="https://github.com/user-attachments/assets/6becce7b-1cde-4ca8-a6a2-5378f4871c71" />





