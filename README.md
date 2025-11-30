# Credit Risk Prediction App (XGBoost + Streamlit)

This project predicts the probability that a loan applicant will default, using a model trained on a credit risk dataset.

## 🔍 What this project includes

- End-to-end data preprocessing and model training in a Jupyter/Colab notebook
- Comparison of Logistic Regression, Random Forest, and XGBoost
- Final deployment of the best model (XGBoost) as a Streamlit web app

## 📘 Training Notebook

The full training pipeline is in:

`notebooks/credit_risk_model_training.ipynb`

It includes:
- EDA
- Data cleaning & encoding
- Train/test split
- Model training (LR, RF, XGB)
- Evaluation & feature importance
- Saving the final model and scaler

## 🌐 Web App

The app is defined in `streamlit_app.py`.

It loads:
- `xgboost_credit_model.pkl` (trained model)
- `scaler.pkl` (StandardScaler used during training)

and exposes an interface to input client information and predict default risk in real time.

## 🚀 Run Locally

```bash
pip install -r requirements.txt
streamlit run streamlit_app.py
