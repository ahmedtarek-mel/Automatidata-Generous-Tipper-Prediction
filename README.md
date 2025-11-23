<p align="center">
  <img src="https://raw.githubusercontent.com/ahmedtarek-mel/Automatidata-Generous-Tipper-Prediction/main/notebooks/screenshots/Banner_.png" width="100%">
</p>

# 🟨 NYC TLC Generous Tipper Prediction — Automatidata Project  

[![Python](https://img.shields.io/badge/Python-3.10-blue.svg)]()
[![Framework](https://img.shields.io/badge/Model-RandomForest-success)]()
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Build](https://img.shields.io/badge/Build-Passing-brightgreen)
![Repo Size](https://img.shields.io/github/repo-size/ahmedtarek-mel/Automatidata-Generous-Tipper-Prediction)
![Stars](https://img.shields.io/github/stars/ahmedtarek-mel/Automatidata-Generous-Tipper-Prediction?style=social)

---
## 🚕 Project Overview  
Build a predictive machine learning model capable of identifying whether a taxi rider is likely to leave a generous tip (≥20%).
Understanding tipping patterns enables TLC to enhance driver earnings strategies, operational planning, and overall customer experience.

The goal:  
➡️ **Predict whether a NYC taxi rider will be a "generous tipper" (tip ≥ 20%)**  
using 2017 Yellow Taxi trip data.

Deliverables include:

- Cleaned & engineered dataset  
- Full EDA  
- Baseline & tuned Random Forest models  
- Feature importance insights  
- Business-ready Executive Summary (PPTX)

---

## 📂 Repository Structure

```
├── data/
│ └── 2017_Yellow_Taxi_Trip_Data.csv 
│
├── notebooks/
│ └── Automatidata_Project.ipynb
│ └── screenshots/ (plots & outputs)
│
├── reports/
│ └── Automatidata_Executive_Summary.pptx
│
├── environment/
│ └── requirements.txt
│
└── README.md
```


---

## 📊 Dataset  
Dataset: **NYC 2017 Yellow Taxi Trips**  
Key fields used:

- Trip distance  
- Trip duration (engineered)  
- Fare, surcharges, tolls  
- Pickup/dropoff timestamps  
- Payment type  
- Engineered feature: `tip_percent`  
- Binary target: `generous_tip`  

Target definition:

```
1 → generous tip ≥ 20%
0 → tip < 20%
```

Balanced data (~50% generous / ~50% not generous).

---

## 🔧 Methodology

### 1️⃣ Data Cleaning
- Removed negative fares/distances  
- Removed invalid durations (>180 min)  
- Converted timestamp fields to datetime  
- Filtered impossible or corrupted trips  

### 2️⃣ Feature Engineering
- `tip_percent`  
- `trip_duration_min`  
- `generous_tip` target  
- `pickup_hour`, `pickup_day`, `pickup_month`  

### 3️⃣ Modeling
Built **two Random Forest models**:

- Baseline RF  
- Tuned RF (GridSearchCV)

### 4️⃣ Metrics Evaluated
- Accuracy  
- Precision  
- Recall  
- F1 Score  
- Confusion Matrix  

---

## 🧪 Model Performance

### **Baseline Random Forest**
| Metric | Score |
|--------|--------|
| Accuracy | 90.5% |
| Precision | 84.2% |
| Recall | 99.4% |
| F1 Score | 91.1% |

### **Tuned Random Forest**
| Metric | Score |
|--------|--------|
| **Accuracy** | **97.87%** |
| **Precision** | **96.65%** |
| **Recall** | **99.09%** |
| **F1 Score** | **97.86%** |

The tuned model shows exceptional predictive power.

---

# 🔍 Feature Importance Insights

Top predictors of generous tipping:

1. **payment_type**  
2. **total_amount**  
3. **fare_amount**  
4. **extra** (surcharges)  
5. `trip_distance`  
6. `trip_duration_min`  
7. `pickup_hour`  
8. Pickup/dropoff location zones  

**Key insight:**  
> Riders paying by credit card on longer, higher-value trips are the most generous tippers.

---

# 📘 MODEL CARD

## 🛄 Model Name  
**Random Forest Classifier — Generous Tipper Prediction**

## 🎯 Intended Use  
- Predict tipping behavior in NYC taxi trips  
- Assist TLC & app developers with fare/tipping insights  
- Power driver-facing tools showing likelihood of generous tipping  

## 🚫 Out-of-Scope  
- Predicting human emotions or financial status  
- Non-NYC taxi data  
- Predicting exact dollar amount of tip  

## 🧠 Model Details  
- Algorithm: RandomForestClassifier  
- Framework: Scikit-Learn  
- Hyperparameter tuning: GridSearchCV  
- Evaluation: Train/validation/test split  

## 📈 Performance Summary  
- High accuracy (97.9%)  
- Excellent recall (99%)  
- Very low false negatives  
- Minimal bias between classes  

## ⚠️ Ethical Considerations  
- Should not be used for fare discrimination  
- Should not alter fare charges for specific riders  
- Must be communicated as a statistical prediction  

---

# 🧩 Executive Summary  
Full business-facing Executive Summary:  
➡️ `reports/Automatidata_Executive_Summary.pptx`

Includes:

- Client objectives  
- Modeling approach  
- Performance metrics  
- Insights  
- Recommendations for TLC  

---

# 🚀 Future Work  
- Add weather & traffic data  
- Try XGBoost or LightGBM  
- Deploy real-time API  
- Build dashboard for TLC  
- Add SHAP explainability  

---

# 📎 Files Included  
- `Automatidata_Project.ipynb`  
- `Automatidata_Executive_Summary.pptx`  
- `requirements.txt`  

---


