# 💳 Credit Risk Prediction App (XGBoost + Streamlit)

This project predicts the probability that a loan applicant will default using a machine learning model trained on a credit risk dataset.  
It includes an end-to-end ML pipeline (EDA → preprocessing → modeling → evaluation → deployment) and a fully interactive **Streamlit web app**.

---

## 🚀 Live Demo

Click here to try the app:

[![Open in Streamlit](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://credit-risk-app-ckmoeuuqmtubycj54skwvw.streamlit.app/)

---

## 📌 Project Overview

This is a complete, production-style ML project covering:

### **✔ Data Preprocessing**
- Missing value handling  
- Ordinal encoding (loan grade, default history)  
- One-hot encoding (intent, home ownership)  
- Outlier treatment  
- Feature scaling (StandardScaler)  

### **✔ Exploratory Data Analysis (EDA)**
- Distribution plots  
- Correlation analysis  
- Class imbalance visualization  
- Income, DTI, interest rate patterns  

### **✔ Machine Learning Models**
The following models were trained and compared:

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|------|----------|-----------|--------|----|---------|
| Logistic Regression | 0.79 | 0.52 | 0.78 | 0.62 | 0.86 |
| Random Forest | 0.93 | 0.95 | 0.73 | 0.82 | 0.93 |
| **XGBoost (Final)** | **0.91** | **0.79** | **0.80** | **0.80** | **0.94** |

👉 **XGBoost** was selected as the final model for deployment.

---

## 🧠 App Features

The deployed Streamlit app includes:

### ✔ Real-time prediction  
Users enter applicant & loan data and get instant default probability.

### ✔ Automatically applies the training pipeline  
- Categorical encoding  
- Ordinal mapping  
- One-hot alignment  
- Feature scaling (9 features)  
- Model prediction  

### ✔ Risk interpretation
- 🟢 Low Risk  
- 🟡 Medium Risk  
- 🔴 High Risk  

### ✔ Clean, modern UI  
Enhanced using custom CSS and multi-column layout.

---

## 📘 Training Notebook

The full model training pipeline is available here:

📁 `notebooks/Loan_default_prediction.ipynb`

It contains:

- EDA  
- Data cleaning  
- Preprocessing  
- Model training  
- Hyperparameter tuning  
- ROC curves & confusion matrices  
- Feature importance  
- Saving `xgboost_credit_model.pkl` and `scaler.pkl`

---

## 🏗 Project Structure

```text
credit-risk-streamlit/
│
├── streamlit_app.py # Streamlit UI + prediction pipeline
├── xgboost_credit_model.pkl # Trained XGBoost model
├── scaler.pkl # StandardScaler (fitted on 9 columns)
├── requirements.txt # Dependencies for deployment
├── README.md # Project documentation
└── notebooks/
└── Loan_default_prediction.ipynb
```


---

## ⚙️ Run the App Locally

```bash
pip install -r requirements.txt
streamlit run streamlit_app.py
