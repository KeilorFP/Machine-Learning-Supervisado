# ⚕️ Cardiac Rhythm Classification using Supervised Machine Learning

This project addresses a real-world biomedical challenge: **classifying ECG signals to detect anomalies in heart rhythms** using machine learning. It simulates the core predictive component of an **Automated External Defibrillator (AED)** — a device designed to analyze a patient’s heart rhythm and determine whether a life-saving shock is needed.

Developed as part of a practical assignment at **IMMUNE Technology Institute**, this solution leverages data science and supervised learning to support rapid and accurate decision-making in emergency healthcare settings.

---

## 🧠 Problem Statement

AEDs are deployed in public spaces to treat cardiac arrest cases. These devices must:

- Analyze short ECG segments (~4 seconds)
- Determine if the rhythm is normal (`0`) or abnormal (`1`)
- Make this decision **instantly** and **without human supervision**

The goal is to train a model that can **accurately classify ECG patterns** based on numerical features extracted from real signals.

---

## 📁 Dataset Description

We worked with:
- `datos_reto.csv`: Labeled dataset (training/testing)
- `datos_onu.csv`: Unlabeled dataset (final prediction)

Each row represents an ECG signal window, described by **30 features** derived from temporal, spectral, time-frequency, and complexity analyses.

### Feature Categories

- **Temporal**: TCI, TCSC, MAV, Exp, Expmod, etc.
- **Spectral**: vFleak, A1–A3, M, x3–x5, etc.
- **Time-Frequency**: Li, bWT  
- **Complexity**: CM, CVbin, PSR, HILB, SamEn, Kurt, etc.

---

## 🔍 Project Structure

### 1. 📦 Data Preparation
- Imported libraries (`pandas`, `numpy`, `sklearn`, `xgboost`)
- Loaded the datasets
- Cleaned and explored the data
- Checked for class distribution and missing values

### 2. 📊 Exploratory Data Analysis (EDA)
- Visualized distribution of classes (normal vs. affected)
- Correlation matrix for feature redundancy
- Standardization with `StandardScaler` for model consistency

### 3. 🤖 Model Training & Selection
Evaluated the following models:

- **Logistic Regression**
- **K-Nearest Neighbors (KNN)**
- **Random Forest**
- **XGBoost Classifier**
- **GridSearchCV** for hyperparameter tuning

✅ Best model selected based on **accuracy ≥ 85%**, and consistent performance across metrics.

### 4. 🧪 Validation
- Evaluated metrics: **accuracy, precision, recall, F1-score**
- Plotted confusion matrix and ROC curves
- Interpreted feature importance (where applicable)

### 5. 🔮 Final Prediction
- Used the trained model to generate predictions for `datos_onu.csv`
- Exported results in CSV format

---

## ✅ Results

- **Best model**: [Insert name here if available — e.g., `XGBoost Classifier`]
- **Validation accuracy**: ~**[Insert exact value]**%
- **Prediction time**: Under 1 second per sample (suitable for AED use)

---

## 🧰 Technologies Used

- Python 3.x
- Jupyter Notebook
- Scikit-learn
- XGBoost
- Pandas, NumPy
- Matplotlib, Seaborn

---
