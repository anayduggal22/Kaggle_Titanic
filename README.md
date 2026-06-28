# 🚢 Titanic Survival Prediction — Kaggle Competition

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![Kaggle](https://img.shields.io/badge/Kaggle-Titanic-20BEFF?style=flat-square&logo=kaggle)
![scikit-learn](https://img.shields.io/badge/scikit--learn-RandomForest-F7931E?style=flat-square&logo=scikit-learn)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

> End-to-end Kaggle competition notebook — EDA, feature engineering, modeling, and submission.  
> Part of my Phase 6 Data Science Roadmap.

---

## 📌 Problem Statement

Predict which passengers survived the Titanic shipwreck using passenger data (age, sex, class, fare, etc.).  
Binary classification: `Survived = 1` or `Survived = 0`

---

## 📁 Project Structure

```
kaggle-titanic/
├── train.csv                      # Kaggle training data
├── test.csv                       # Kaggle test data
├── titanic_kaggle.ipynb           # Main notebook
├── submission.csv                 # Final Kaggle submission
├── feature_importance.png         # Feature importance plot
└── README.md
```

---

## 🔧 Feature Engineering

| Feature | Description |
|---|---|
| `FamilySize` | SibSp + Parch + 1 |
| `IsAlone` | 1 if FamilySize == 1 |
| `Title` | Extracted from Name (Mr, Mrs, Miss, Master, Rare) |
| `AgeBand` | Age bucketed into 5 groups (Child → Senior) |
| `FareBand` | Fare quartile-binned into 4 groups |

---

## 🤖 Model

- **Algorithm:** Random Forest Classifier
- **Cross-validation:** 5-fold CV
- **CV Accuracy:** 0.8294 +- 0.0146
- **Kaggle Score:** 0.78229

---

## 📊 Key EDA Insights

- Average passenger age was ~30
- Class 3 had the most passengers but Class 1 had the highest survival rate
- Female survival rate was ~2.5x higher than male survival rate

---

## 🚀 How to Run

```bash
git clone https://github.com/anayduggal22/kaggle-titanic
cd kaggle-titanic
python -m venv venv
venv\Scripts\activate
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook titanic_kaggle.ipynb
```

---

## 📦 Dependencies

```
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

---

*Part of my self-taught Data Science roadmap — Phase 6: Kaggle EDA + Portfolio*
