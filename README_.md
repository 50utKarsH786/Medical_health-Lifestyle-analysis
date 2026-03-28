# 🏥 Medical Health & Lifestyle Analytics
### End-to-End Data Science Project | Production-Grade · FAANG-Standard

---

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.x-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-1.x-013243?style=for-the-badge&logo=numpy&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-3-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-11557C?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-4EADF0?style=for-the-badge)

</div>

---

## 📌 Project Overview

This project delivers a **comprehensive, production-grade data science pipeline** on a synthetic population health dataset. The analysis covers everything from raw data ingestion to machine learning model deployment — following the engineering and analytical standards expected at companies like **Google, Meta, Amazon, Microsoft, Apple, Netflix, and the Big 4 consulting firms**.

The goal: extract clinically meaningful insights from lifestyle and biometric data, build predictive models for health outcomes, and translate findings into **actionable public health recommendations**.

---

## 🎯 Objectives

| Objective | Details |
|-----------|---------|
| **Data Quality** | Audit, clean, and preprocess raw health records to production standards |
| **EDA** | Uncover patterns across demographics, lifestyle habits, and chronic disease |
| **Feature Engineering** | Create domain-informed composite features (Health Risk Score, etc.) |
| **SQL Analytics** | Run multi-dimensional cohort queries on a SQLite database |
| **Regression** | Predict Sleep Hours using 8 competing ML models with cross-validation |
| **Classification** | Predict Chronic Disease risk using 7 classifiers with ROC-AUC evaluation |
| **Explainability** | Extract and visualise feature importances for clinical interpretability |
| **Insights** | Produce a population health KPI dashboard and strategic recommendations |

---

## 🛠 Tech Stack

```
Language      : Python 3.10+
Data Wrangling: Pandas, NumPy
ML Framework  : Scikit-learn (Pipelines, GridSearchCV, Cross-Validation)
Visualisation : Matplotlib, Seaborn, Plotly
Database      : SQLite (via sqlite3)
Statistical   : SciPy (outlier analysis)
Environment   : Jupyter Notebook / Google Colab
```

### ML Models Used

**Regression (Sleep Hours Prediction)**
- Linear Regression, Ridge, Lasso, ElasticNet
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- K-Nearest Neighbours Regressor

**Classification (Chronic Disease Risk)**
- Logistic Regression
- Gaussian Naive Bayes
- K-Nearest Neighbours Classifier
- Decision Tree Classifier
- Random Forest Classifier *(class_weight='balanced')*
- Gradient Boosting Classifier
- AdaBoost Classifier

---

## 📂 Project Structure

```
medical-health-analytics/
│
├── Medical_Health_Analytics_Pro.ipynb  ← Main notebook
├── README.md                           ← This file
├── synthetic_health_lifestyle_dataset.csv
│
└── outputs/
    ├── eda_demographics.png
    ├── correlation_heatmap.png
    └── model_comparison.png
```

---

## 🗂 Notebook Structure

```
1. Environment Setup & Data Ingestion
   ├─ Reproducible imports (seeded)
   ├─ Global plotting theme (production-grade aesthetics)
   └─ Colab / local-compatible data loader

2. Data Quality Assessment
   ├─ Missing value audit (counts + %)
   ├─ Duplicate detection
   ├─ Cardinality analysis
   └─ Descriptive statistics dashboard

3. Advanced Data Cleaning & Preprocessing
   ├─ Deduplication
   ├─ Median imputation (numerical) + Mode imputation (categorical)
   └─ IQR-based Winsorization (outlier capping, not dropping)

4. Exploratory Data Analysis (EDA)
   ├─ Demographic Overview Dashboard (6-panel)
   ├─ BMI Category Analysis (by gender)
   ├─ Lifestyle Behaviour Analysis (smoking, exercise, diet, alcohol)
   ├─ Chronic Disease Risk Factor Breakdown
   ├─ Correlation Heatmap (lower-triangle masked)
   ├─ Age Group × Exercise + Stress Violin Plot
   └─ Pairplot by Chronic Disease status

5. Feature Engineering (9 new features)
   ├─ Health Risk Score (composite clinical index)
   ├─ Sleep Deficit Flag (<6 hrs)
   ├─ Overweight / High Stress binary flags
   ├─ Age×BMI and BMI×Stress interaction terms
   └─ Ordinal encodings for lifestyle variables

6. SQL Analytics Layer (5 rich queries)
   ├─ Q1: Population-level health summary KPIs
   ├─ Q2: Chronic disease rate by diet × exercise
   ├─ Q3: High-risk segment identification (overweight smokers)
   ├─ Q4: Healthy cohort profile benchmark
   └─ Q5: Sleep & stress band analysis (window-function style)

7. Machine Learning Pipeline
   ├─ 7a: Regression — 8 models, 5-fold CV, RMSE/MAE/R²
   └─ 7b: Classification — 7 models, stratified split, ROC-AUC/F1

8. Model Evaluation & Comparison
   ├─ ROC curves (all classifiers on one plot)
   ├─ Confusion matrix (best classifier)
   └─ Regression RMSE / R² comparison bar charts

9. Feature Importance & Explainability
   ├─ RF + GB importance — Regression
   └─ RF + GB importance — Classification

10. Clinical Insights & Recommendations
    ├─ Population Health KPI Dashboard
    ├─ Risk Heatmap (Age Group × BMI Category)
    ├─ Lifestyle Factor Impact Charts (4-panel)
    └─ Final Executive Summary
```

---

## 📊 Key Findings

### 🔴 High-Risk Flags
- Chronic disease prevalence is clinically significant in the population
- Obese smokers aged 50–60 carry the **highest composite risk scores**
- High-stress individuals consistently show shorter average sleep hours

### 🟢 Protective Factors
- Excellent diet + Daily exercise + Non-smoker → **lowest chronic disease rates**
- Maintaining BMI in the 18.5–24.9 range is the single strongest controllable health lever
- Even a shift from "Poor" to "Good" diet quality meaningfully reduces risk

### 🤖 Model Performance
| Task | Best Model | Metric |
|------|-----------|--------|
| Sleep Hours Prediction | Gradient Boosting / Random Forest | R², RMSE |
| Chronic Disease Classification | Random Forest / Gradient Boosting | ROC-AUC, F1 |

> Note: Sleep Hours has inherently high variance — genetic and psychological factors not present in the dataset drive much of the variability. This is consistent with published clinical literature.

---

## ⚙️ How to Run

### Option 1 — Google Colab (Recommended)
1. Upload `Medical_Health_Analytics_Pro.ipynb` to [Google Colab](https://colab.research.google.com)
2. Upload the CSV when prompted by the first cell
3. Run All (`Runtime → Run All`)

### Option 2 — Local Jupyter
```bash
# Clone / download the project
git clone https://github.com/your-username/medical-health-analytics.git
cd medical-health-analytics

# Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn plotly jupyter

# Launch
jupyter notebook Medical_Health_Analytics_Pro.ipynb
```

### Option 3 — VS Code
Open the `.ipynb` file directly — VS Code's Jupyter extension handles it natively.

---

## 📦 Dependencies

```text
pandas>=1.5
numpy>=1.23
scikit-learn>=1.2
matplotlib>=3.6
seaborn>=0.12
plotly>=5.0        # optional — for interactive charts
jupyter>=1.0
```

Install all at once:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn plotly jupyter
```

---

## 🧠 Skills Demonstrated

| Domain | Skills |
|--------|--------|
| **Data Engineering** | Ingestion, deduplication, type casting, IQR Winsorization, median/mode imputation |
| **Statistics** | Correlation analysis, outlier detection, distributional analysis |
| **EDA** | Multi-panel dashboards, pairplots, violin plots, heatmaps, KDE plots |
| **Feature Engineering** | Composite scoring, interaction terms, ordinal encoding, binary flags |
| **SQL** | Cohort analysis, GROUP BY + HAVING, CASE WHEN, multi-join style aggregations |
| **Machine Learning** | Pipelines, StandardScaler, 5-Fold CV, GridSearchCV-ready structure |
| **Model Evaluation** | ROC-AUC, Confusion Matrix, Classification Report, RMSE, MAE, R² |
| **Explainability** | Feature importance (RF + GB), residual analysis |
| **Communication** | KPI dashboards, executive summaries, clinical recommendations |

---

## 🏆 Why This Project Stands Out

✅ **Reproducible** — Seeded randomness, modular code, environment-agnostic loader  
✅ **Production patterns** — Sklearn Pipelines, StandardScaler applied correctly (fit on train only)  
✅ **Multi-model comparison** — 8 regression + 7 classification models, not just one  
✅ **Domain expertise** — BMI classification follows WHO standards, Health Risk Score uses clinical weights  
✅ **SQL fluency** — 5 complex analytical queries, not just `SELECT *`  
✅ **Visualisation quality** — Consistent theme, 30+ charts, publication-ready layouts  
✅ **Business translation** — Raw numbers converted to KPIs and actionable recommendations  

---

## 📄 Dataset

**Synthetic Health & Lifestyle Dataset**  
- Records: Population sample (~1,000–5,000 patients)  
- Features: 15+ including Age, BMI, Sleep Hours, Stress Level, Chronic Disease, Smoking, Exercise Frequency, Diet Quality, Alcohol Consumption  
- Source: Synthetic data (no patient privacy concerns)  
- Target variables: `Sleep_Hours` (regression), `Chronic_Disease` (classification)

---

## 📬 Contact

**Portfolio Project** — built to demonstrate end-to-end data science capability  

> ⭐ If you found this useful, please star the repository!

---

*Built with ❤️ following FAANG/MAANG-level data science best practices.*
