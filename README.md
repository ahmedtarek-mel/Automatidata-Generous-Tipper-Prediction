
# 🟨 NYC TLC Generous Tipper Prediction — Automatidata Project

This repository contains the full end-to-end machine learning project completed for the **Google Advanced Data Analytics Certificate — Course 6 (Machine Learning)**. 
The goal is to predict whether a NYC taxi rider will be a **generous tipper (tip ≥ 20%)** using 2017 Yellow Taxi trip data.

---

## 🚕 Project Overview

The NYC Taxi & Limousine Commission (TLC) partnered with Automatidata to identify patterns in tipping behavior and develop a predictive machine-learning model.  
This project builds:

- A cleaned and engineered dataset  
- Exploratory Data Analysis (EDA)  
- Baseline & tuned Random Forest models  
- Feature importance interpretation  
- Executive Summary for business stakeholders  

---

## 📂 Repository Structure

```
├── data/
│   └── 2017_Yellow_Taxi_Trip_Data.csv
├── notebooks/
│   └── Automatidata_Project.ipynb
├── reports/
│   ├── Automatidata_Executive_Summary.pptx
│   └──PACE_Strategy_Document.docs
└── README.md
```

---

## 📊 Dataset

The project uses the **2017 NYC Yellow Taxi Trip Dataset**.  
Key features include:

- Trip distance & duration  
- Fare, tolls, surcharges  
- Pickup/dropoff datetimes  
- Location IDs  
- Payment type  
- Engineered features (tip %, trip duration, etc.)

The target variable:

```
generous_tip = 1 (tip ≥ 20%)
generous_tip = 0 (tip < 20%)
```

Dataset is balanced: ~50% generous, ~50% not generous.

---

## 🔧 Methodology

### 1️⃣ Data Cleaning
- Removed negative fares/distances  
- Removed invalid durations (>180 minutes)  
- Converted timestamps  
- One-hot encoding of categorical variables  

### 2️⃣ Feature Engineering
- tip_percent  
- generous_tip (binary target)  
- trip_duration_min  
- pickup_hour, pickup_day, pickup_month  

### 3️⃣ Modeling
Two Random Forest models were built:

- **Baseline Model**  
- **Tuned Model** (GridSearchCV)

### 4️⃣ Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1 Score  
- Confusion Matrix  

---

## 🧪 Model Performance

### **Baseline Random Forest**
- Accuracy: 90.5%  
- Precision: 84.2%  
- Recall: 99.4%  
- F1 Score: 91.1%

### **Tuned Random Forest**
- Accuracy: **97.87%**  
- Precision: **96.65%**  
- Recall: **99.09%**  
- F1 Score: **97.86%**

The tuned model offers exceptional predictive performance.

---

## 🔍 Feature Importance Insights

Top predictors of generous tipping:

1. **payment_type**  
2. **total_amount**  
3. **fare_amount**  
4. **extra (surcharges)**  
5. trip_distance  
6. trip_duration_min  
7. pickup_hour  
8. pickup/dropoff zones  

Main insight:  
> Credit card riders + long/high-value trips = most generous tippers.

---

## 🧩 Executive Summary

A full business-facing Executive Summary is provided in:  
`reports/Automatidata_Executive_Summary.pptx`

It includes:
- Business objective  
- Modeling approach  
- Final metrics  
- Key insights  
- Recommendations for TLC  

---

## 🚀 Future Work

Potential expansions:

- Add weather & traffic features  
- Try XGBoost or LightGBM  
- Build real-time prediction API  
- Deploy via Docker / Cloud  

---

## 📎 Files Created

- `Automatidata_Executive_Summary.pptx`  
- `README.md` (this file)

