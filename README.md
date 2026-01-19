
# Heart Disease Prediction with PySpark

A distributed machine learning project developed for the **Distributed Data Analysis and Mining (DDAM)** course at the University of Pisa. This work applies scalable ML techniques to predict heart disease using a synthetic dataset of over **1 million patient records**, based on an expanded version of the UCI Statlog Heart dataset.

## 🎯 Objective
Predict the presence (class = 1) or absence (class = 0) of heart disease using **PySpark** on a large-scale medical dataset, while ensuring robust preprocessing, exploratory analysis, and model evaluation—with a focus on **recall** to minimize missed diagnoses.

## 📊 Dataset
- **Source**: OpenML (Dataset ID: 267), synthetic extension of UCI Statlog Heart
- **Size**: >1,000,000 records
- **Features**: Age, sex, chest pain type, resting blood pressure, cholesterol, fasting blood sugar, ECG results, max heart rate, exercise-induced angina, ST depression (oldpeak), slope, vessel count, thalassemia
- **Target**: Binary (`0` = no disease, `1` = disease)
- **Balance**: Perfectly balanced classes → no resampling needed

## 🛠️ Tech Stack
- **Framework**: Apache Spark via **PySpark**
- **Algorithms**: 
  - Supervised: **Random Forest**, **Logistic Regression** (with 3-fold cross-validation + grid search)
  - Unsupervised: **K-means Clustering** (Elbow method + silhouette score)
- **Preprocessing**: Custom data cleaning (e.g., float-to-int conversion, byte decoding), one-hot encoding, feature scaling
- **Evaluation Metrics**: **Recall** (primary), F1-score, confusion matrices, feature importance

## 🔍 Key Insights
- **Males** show higher incidence of heart disease in this dataset.
- Most patients are aged **55–65**, with a peak at **60**.
- **No strong feature correlations** → all features retained (no dimensionality reduction).
- **Random Forest** outperformed Logistic Regression:
  - RF Recall: **0.8849**
  - LR Recall: **0.8775**

## 📁 Repository Structure
```
.
├── data/                     # Sample of synthetic dataset (if included)
├── notebooks/
│   └── DDAM_HeartDisease_PySpark.ipynb  # Full pipeline: EDA, preprocessing, modeling
├── docs/
│   └── DDAM_Report_Group9.pdf           # Technical report with visualizations and results
└── README.md
```

## 📄 Report Highlights
- Data cleaning strategy for synthetic artifacts (e.g., float-encoded categories)
- Feature importance ranking from Random Forest
- Clustering analysis to uncover hidden patient subgroups
- Emphasis on **clinical relevance** of high recall in diagnostic contexts

---

*Group ID_09 | Sana Afreen (681744), Zhiqi Zhu (702295)*  
*Course: Distributed Data Analysis and Mining (DDAM), University of Pisa – December 2024*
```
