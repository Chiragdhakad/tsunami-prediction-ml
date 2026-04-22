# 🌊 Tsunami Prediction Using Machine Learning

A supervised machine learning framework for binary classification of 
earthquake events as tsunami-generating or non-tsunami-generating, 
using imbalanced learning techniques on a 26-year global seismic dataset.

---

## 📌 Project Overview

Tsunamis are rare but devastating natural events. This project addresses 
the challenge of predicting tsunami occurrence from earthquake parameters 
using machine learning, with a specific focus on handling severe class 
imbalance through SMOTE-based oversampling.

---

## 📂 Dataset

| Source | Description |
|--------|-------------|
| [USGS Earthquake Catalog](https://earthquake.usgs.gov/earthquakes/search/) | Earthquake records from 2000–2026 |
| [NOAA Tsunami Database](https://www.ngdc.noaa.gov/hazel/hazard-service/api/v1/) | Historical tsunami event records |

The datasets are not publicly redistributed here due to size.  
Please download them directly from the official sources above.

---

## ⚙️ Methodology

- **Physical Filtering:** Magnitude ≥ 5.5, Depth ≤ 100 km
- **Spatiotemporal Matching:** Time window of ±6 hours, Distance window of 600 km
- **Class Imbalance Handling:** SMOTE (Synthetic Minority Over-sampling Technique)
- **Validation:** Stratified 10-Fold Cross Validation
- **Models Evaluated:** Logistic Regression, Random Forest, Decision Tree, SVM

---

## 📊 Results Summary

| Model | ROC-AUC | Recall | Precision | F1 |
|-------|---------|--------|-----------|----|
| Logistic Regression | 0.902 | 0.78 | 0.066 | — |
| Random Forest | 0.897 | 0.61 | 0.115 | — |
| Decision Tree | 0.758 | 0.61 | 0.063 | — |
| SVM | 0.846 | 0.53 | 0.08 | — |

> Logistic Regression selected as final model due to highest recall — 
> critical for early warning systems where missing a tsunami is unacceptable.

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/tsunami-prediction-ml.git
cd tsunami-prediction-ml

# 2. Install dependencies
pip install -r requirements.txt

# 3. Add datasets to the data/ folder
# (Download from USGS and NOAA links above)

# 4. Open the notebook
jupyter notebook tsunami_prediction_research_main.ipynb
```

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.9+-blue)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Pandas](https://img.shields.io/badge/Pandas-Data-green)
![SMOTE](https://img.shields.io/badge/SMOTE-Imbalanced-red)

---

## 📁 Repository Structure
