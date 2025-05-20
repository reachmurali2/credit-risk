# Lauki Finance: Credit Risk Modeling

A Streamlit-based web application to predict the credit default risk, credit score, and risk rating for loan applicants. This tool helps financial institutions assess the risk profile of individuals before loan approval.

---

## 📊 Overview

This application uses a logistic regression model to predict:
- **Default Probability**
- **Credit Score** (Scaled from 300 to 900)
- **Risk Rating** (Poor, Average, Good, Excellent)

---

## 🧾 Input Parameters

The app collects the following inputs from users:
- **Age**
- **Income**
- **Loan Amount**
- **Loan Tenure (in months)**
- **Avg Days Past Due (DPD) per Delinquency**
- **Delinquency Ratio (%)**
- **Credit Utilization Ratio (%)**
- **Number of Open Loan Accounts**
- **Residence Type** (Owned, Rented, Mortgage)
- **Loan Purpose** (Education, Home, Auto, Personal)
- **Loan Type** (Secured or Unsecured)

---

## ⚙️ Features

- Dynamic calculation of **Loan to Income Ratio**
- Uses pre-trained logistic regression model for prediction
- Scales inputs using a `MinMaxScaler`
- Computes the credit score and maps it to a rating

---

## 📂 Project Structure

```
.
├── main.py                    # Streamlit frontend app
├── prediction_helper.py       # Contains model prediction logic
├── artifacts/
│   └── model_data.joblib      # Serialized model, scaler, and config
```

---

## 🚀 How to Run

### 1. Install Dependencies

```bash
pip install streamlit pandas numpy scikit-learn joblib
```

### 2. Launch the App

```bash
streamlit run main.py
```

---

## 📈 Output

On submission, the app displays:
- 📉 **Default Probability** (chance of the user defaulting)
- 💳 **Credit Score** (range: 300–900)
- 🏅 **Risk Rating** (Poor, Average, Good, Excellent)

---

## 📌 Notes

- The app uses dummy values for some features needed by the scaler to ensure compatibility.
- You can extend this by replacing the dummy values with actual user inputs in a production system.

---

## 📩 Attribution

Developed using concepts from the [ML Course](https://codebasics.io).
