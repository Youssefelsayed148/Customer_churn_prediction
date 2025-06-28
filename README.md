
# 📊 Customer Churn Prediction with XGBoost

This machine learning project predicts customer churn using the Telco Customer Churn dataset. It includes a full-featured model for performance and a simplified deployment using Gradio for real-time predictions.

---

## 🚀 Project Overview

The goal is to predict whether a customer will churn based on account and service usage features. The project includes:

- Data preprocessing (imputation, encoding)
- Model training using XGBoost
- Feature selection based on importance
- Hyperparameter tuning with RandomizedSearchCV
- A user-friendly Gradio app with selected top features

---


---

## 🔍 Features Used

### Full Model:
Trained on all cleaned numerical and categorical features.

### Gradio App (Top 5 Categorical Features):
Selected by feature importance:
- `StreamingMovies`
- `Contract`
- `MultipleLines`
- `InternetService`
- `DeviceProtection`

---

## 🧠 Model Details

- **Model**: XGBoost Classifier (`XGBClassifier`)
- **Encoding**: OrdinalEncoder
- **Pipeline**: Scikit-learn `Pipeline` (preprocessing + model)
- **Tuning**: RandomizedSearchCV

---

## 📈 Model Performance

| Metric       | XGBoost (rs_xgb) |
|--------------|------------------|
| Accuracy     | ~78%             |
| F1 Score     | ~0.59 (Churn)    |
| Balanced     | Reasonably balanced across churn classes |

---

## 🌐 Gradio App

Interactive web app built using Gradio:
- Users select key categorical inputs
- App returns churn prediction and probability

### Run Locally

```bash
pip install -r requirements.txt
python app.py
