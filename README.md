# 🫁 Lung Cancer Prediction using Logistic Regression

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0%2B-orange?logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)

A machine learning project that predicts lung cancer risk using a **Logistic Regression** classifier trained on a clinical survey dataset of 309 patients.

---

## 📌 Project Overview

Lung cancer is one of the leading causes of cancer-related deaths globally. Early and accurate detection can save lives. This project builds a binary classification model using **Logistic Regression** to determine whether a patient has lung cancer based on self-reported symptoms and lifestyle habits.

---

## 📊 Dataset

| Property | Detail |
|----------|--------|
| **File** | `survey_lung_cancer.csv` |
| **Records** | 309 patients |
| **Features** | 15 (symptoms + demographics) |
| **Target** | `LUNG_CANCER` — YES / NO |

**Features include:** Gender, Age, Smoking, Yellow Fingers, Anxiety, Peer Pressure, Chronic Disease, Fatigue, Allergy, Wheezing, Alcohol Consuming, Coughing, Shortness of Breath, Swallowing Difficulty, Chest Pain.

> Note: Binary symptom features use a scale of `1 = No` and `2 = Yes`.

---

## 🔬 Methodology

1. **Data Loading & Cleaning** — Load CSV, strip whitespace from headers, handle missing values
2. **Exploratory Data Analysis** — Class distribution, gender/age analysis, symptom prevalence charts
3. **Preprocessing** — Label encode target (`YES→1, NO→0`), one-hot encode categorical features
4. **Train/Test Split** — 80% training / 20% testing (`random_state=42`)
5. **Model Training** — `LogisticRegression(max_iter=500)`
6. **Evaluation** — Accuracy, Precision, Recall, Specificity, ROC-AUC, Confusion Matrix

---

## 📈 Results

| Metric | Score |
|--------|-------|
| **Accuracy** | 96.77% |
| **Precision** | 98.33% |
| **Recall** | 98.33% |
| **Specificity** | 50.00% |
| **ROC-AUC** | 0.9250 |

The model performs exceptionally well at identifying lung cancer patients (high recall and ROC-AUC of 0.925), making it a strong screening tool. Specificity is lower due to severe class imbalance (~87% positive class — only 2 true negatives appeared in the test set).

---

## 📁 Repository Structure

```
lung-cancer-prediction/
│
├── Lung_Cancer_Prediction.ipynb   # Main Jupyter notebook
├── survey_lung_cancer.csv         # Dataset
├── README.md                      # Project documentation
│
└── images/                        # (auto-generated on run)
    ├── class_distribution.png
    ├── gender_age_analysis.png
    ├── symptom_comparison.png
    ├── feature_coefficients.png
    └── model_evaluation.png
```

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Run the Notebook

```bash
git clone https://github.com/YOUR_USERNAME/lung-cancer-prediction.git
cd lung-cancer-prediction
jupyter notebook Lung_Cancer_Prediction.ipynb
```

---

## 🛠️ Technologies Used

- **Python 3.8+**
- **pandas** — Data manipulation
- **NumPy** — Numerical computing
- **Matplotlib / Seaborn** — Data visualization
- **scikit-learn** — Machine learning (Logistic Regression, metrics)

---

## 📌 Key Takeaways

- Logistic Regression is an effective baseline for medical binary classification.
- Features like **Fatigue**, **Chest Pain**, **Shortness of Breath**, and **Wheezing** are the strongest predictors.
- Class imbalance (87% YES) affects specificity — future work could apply SMOTE or ensemble methods.

---

## 👩‍💻 Author

**Florencekumari Makwana**  
Third ML/Data Science Project — Logistic Regression

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
