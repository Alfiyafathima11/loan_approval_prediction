# 🏦 Loan Approval Prediction System
> Automating Banking Decisions with Machine Learning

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?style=for-the-badge&logo=scikit-learn)
![Accuracy](https://img.shields.io/badge/Accuracy-98%25-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

---

## 📌 Project Overview

This project builds an intelligent **Loan Approval Prediction System** that automates banking decisions using a **Random Forest Classifier**. It eliminates manual bottlenecks, reduces human bias, and delivers consistent, data-driven loan decisions with **~98% accuracy**.

---

## 🎯 Objectives

- ✅ **Automate** loan approval decisions using ML
- ✅ **Improve accuracy** and eliminate human bias
- ✅ **Deploy** a fully functional prediction system

---

## 📊 Dataset

| Feature | Type |
|---|---|
| no_of_dependents | Numeric |
| education | Categorical |
| self_employed | Categorical |
| income_annum | Numeric |
| loan_amount | Numeric |
| loan_term | Numeric |
| cibil_score | Numeric |
| residential_assets_value | Numeric |
| commercial_assets_value | Numeric |
| luxury_assets_value | Numeric |
| bank_assets_value | Numeric |

**Target Variable:** `loan_status` → Approved (1) or Rejected (0)

> 💡 **Key Insight:** CIBIL score and annual income are the strongest predictors of loan approval.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core programming language |
| Pandas & NumPy | Data manipulation |
| Matplotlib & Seaborn | Data visualization |
| Scikit-learn | ML model training & evaluation |
| Google Colab | Development environment |

---

## 🤖 Model — Random Forest Classifier

Random Forest is an **ensemble learning** method that builds 100+ independent decision trees and merges their outputs via **majority voting** for the final prediction.

**Why Random Forest?**
- Reduces variance and prevents overfitting
- Handles both numeric and categorical features
- Provides feature importance rankings
- Robust to outliers

---

## ⚙️ How It Works

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import LabelEncoder

# Label Encoding
le = LabelEncoder()
for col in ['education', 'self_employed', 'loan_status']:
    df[col] = le.fit_transform(df[col])

# Train-Test Split (80/20)
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42)

# Train Model
model = RandomForestClassifier()
model.fit(X_train, y_train)
```

---

## 📈 Model Performance

| Metric | Score |
|---|---|
| ✅ Accuracy | ~98% |
| ✅ Precision | 0.98 |
| ✅ Recall | 0.98 |
| ✅ F1-Score | 0.98 |

### Confusion Matrix Results
- **531** True Negatives — correctly rejected high-risk applicants
- **306** True Positives — correctly approved creditworthy applicants
- **5** False Positives — risky applicants mistakenly approved
- **12** False Negatives — valid applicants incorrectly rejected

> Only **17 errors** out of **854 predictions** — a remarkably low misclassification rate.

---

## 🚀 How to Run

**1. Clone the repository**
```bash
git clone https://github.com/Alfiyafathima11/loan_approval_prediction.git
cd loan_approval_prediction
```

**2. Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

**3. Open the notebook**
```bash
jupyter notebook loan_approval_datasetipynb.ipynb
```

Or open directly in **Google Colab**:  
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

---

## 🔭 Future Scope

- 🌐 Deploy as a **web app** using Flask or Streamlit
- 🧠 Explore **XGBoost, LightGBM, or Neural Networks**
- 📂 Incorporate **repayment history** and **transaction patterns**
- 📱 Build a **mobile-friendly** prediction interface

---

## 👩‍💻 Author

**Alfiya Fathima S**  
[![GitHub](https://img.shields.io/badge/GitHub-Alfiyafathima11-black?style=flat&logo=github)](https://github.com/Alfiyafathima11)

---

## 📄 License

This project is licensed under the **MIT License** — feel free to use and modify it.

---

⭐ *If you found this project helpful, please give it a star!*
