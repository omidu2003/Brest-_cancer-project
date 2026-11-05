# Breast Cancer Diagnostic Model

A machine learning project that classifies breast tumours as **benign or malignant** using the **Breast Cancer Wisconsin (Diagnostic)** dataset (569 samples, 30 features computed from digitised images of fine-needle aspirates). The project covers the full workflow: exploratory data analysis, unsupervised clustering, training and comparing nine classifiers, and hyperparameter tuning.

## Results

Best model — **tuned XGBoost** (held-out test set, 114 patients):

| Metric | Result |
|---|---|
| Accuracy | **98%** |
| AUC-ROC | **0.99** |
| Malignant precision | **1.00** (no benign tumours wrongly flagged) |
| Malignant recall | 0.95 |
| Benign recall | 1.00 |

Tuned Random Forest also performed strongly: 97% accuracy, AUC-ROC 0.996.

### Model comparison (StandardScaler, test set)

| Model | Accuracy | AUC-ROC |
|---|---|---|
| Logistic Regression | 96% | 0.994 |
| SVM (RBF kernel) | 96% | 0.994 |
| Random Forest | 97% | 0.995 |
| K-Nearest Neighbours | 94% | 0.968 |
| Gradient Boosting | 96% | 0.996 |
| Decision Tree | 93% | 0.920 |
| AdaBoost | 96% | 0.983 |
| Extra Trees | 96% | 0.997 |
| XGBoost | 97% | 0.992 |
| **XGBoost (tuned)** | **98%** | **0.990** |

All models were also tested with Min-Max scaling for comparison.

## Workflow

1. **Exploratory data analysis** – distributions, correlations and class balance.
2. **Unsupervised analysis** – K-Means and hierarchical (agglomerative) clustering with PCA visualisation and silhouette scores, to see how naturally the tumour types separate.
3. **Preprocessing** – label encoding, stratified train/test split, StandardScaler and MinMaxScaler.
4. **Model training & evaluation** – nine classifiers compared using classification reports, confusion matrices and ROC curves.
5. **Hyperparameter tuning** – randomised search with 5-fold cross-validation for Random Forest and XGBoost.

## Tech stack

Python · pandas · NumPy · scikit-learn · XGBoost · SciPy · Matplotlib · Seaborn · Jupyter

## Repository contents

| File | Description |
|---|---|
| `Breast_Cancer_Wisconsin_(Diagnostic)_Predictive_Model.ipynb` | Full analysis and modelling notebook |
| `data.csv` | Breast Cancer Wisconsin (Diagnostic) dataset |
| `Breaths Canser (1).pptx` | Project presentation |
| `breats canser (2).docx` | Project report |

## Running it

Open the notebook in Jupyter or Google Colab and run all cells. Required packages:

```bash
pip install pandas numpy scikit-learn xgboost scipy matplotlib seaborn
```

> This is an academic project and is not intended for clinical use.

## Author

**Omidu Dulen Jayasinghe** — BSc Applied Artificial Intelligence, University of Bradford
[GitHub](https://github.com/omidu2003) · [LinkedIn](https://www.linkedin.com/in/omidu-jayasinghe-88589a32b/)
