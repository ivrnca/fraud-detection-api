# 🕵️‍♀️ Fraud Detection API with FastAPI

An end-to-end machine learning API that detects fraudulent credit card transactions.
Built with ❤️ using Python, FastAPI, and a Random Forest classifier.

---

## 🚀 Features

* Detects fraud from real-world credit card transactions
* Trained on Kaggle’s imbalanced dataset using Random Forest
* RESTful API using FastAPI framework
* Accepts JSON input, returns JSON output
* Deploy-ready on platforms like Render or Railway

---

## 🧠 Model Overview

* **Algorithm:** Random Forest Classifier
* **Balancing Method:** Undersampling
* **Dataset:** [Credit Card Fraud Detection (Kaggle)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

> ⚠️ This dataset is not included in this repository due to GitHub’s file size limit.
> Please download it manually from Kaggle and place it in the `data/` folder as `creditcard.csv`.

---

## 📆 Project Structure

```
fraud-detection-api/
│
├── main.py                # FastAPI app (API logic)
├── models/                # Trained model (fraud_model.pkl)
├── data/                  # Dataset (creditcard.csv) - ignored in Git
├── notebooks/             # Jupyter notebook for model training
├── requirements.txt       # Dependencies
├── start.sh               # Render startup script
└── render.yaml            # Render deployment config
```

---

## ⚙️ Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/ivrnca/fraud-detection-api.git
cd fraud-detection-api
```

### 2. Setup virtual environment

```bash
python -m venv venv
.\venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Download dataset

* Get `creditcard.csv` from [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
* Place the file inside `data/` folder

### 4. Train model

Open `train_model.ipynb` or run script (if available).
The result will be saved to `models/fraud_model.pkl`.

### 5. Run the API locally

```bash
uvicorn main:app --reload
```

Open [http://localhost:8000/docs](http://localhost:8000/docs) to access Swagger UI.

---

## 🧪 Sample Request (JSON Payload)

```json
{
  "Time": 0.0,
  "V1": -1.3598,
  "V2": -0.0727,
  "V3": 2.5363,
  "V4": 1.3781,
  "V5": -0.3383,
  "V6": 0.4623,
  "V7": 0.2395,
  "V8": 0.0986,
  "V9": 0.3637,
  "V10": 0.0907,
  "V11": -0.5515,
  "V12": -0.6178,
  "V13": -0.9913,
  "V14": -0.3111,
  "V15": 1.4681,
  "V16": -0.4704,
  "V17": 0.2079,
  "V18": 0.0257,
  "V19": 0.4039,
  "V20": 0.2514,
  "V21": -0.0183,
  "V22": 0.2778,
  "V23": -0.1104,
  "V24": 0.0669,
  "V25": 0.1285,
  "V26": -0.1891,
  "V27": 0.1335,
  "V28": -0.0210,
  "Amount": 149.62
}
```

Response:

```json
{
  "prediction": "not fraud"
}
```

---

## 🌐 Deployment (Optional)

You can deploy this API to [Render](https://render.com) or similar platforms using the included `render.yaml` and `start.sh`.

Example live endpoint:

```
https://fraud-api.onrender.com/docs
```

---

## 👤 About Me

Hi! I'm **Griventh**, an aspiring AI engineer with a background in cybersecurity and full-stack development.
I’m currently exploring the intersection of machine learning, security, and real-world applications—
with a dream of building impactful, remote-friendly solutions.

* 🔗 GitHub: [@ivrnca](https://github.com/ivrnca)
* 🔗 LinkedIn: [Griventh Griffith Agustin](www.linkedin.com/in/griventh-griffith-agustin)

---

## 💡 Motivation

This project was created as part of my journey transitioning from cybersecurity to AI Engineering,
and to build practical, deployable models that could help real-world fraud detection use cases.

---
