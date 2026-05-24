# MechSense 🔧⚡

**Industrial Predictive Maintenance AI** — Know before machines break.

Six machine learning models + rule-based baseline, trained on 10,000 real industrial sensor readings (AI4I 2020 dataset) to predict equipment failure before it costs you.

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-Best_Model-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 🎯 Overview

MechSense tackles **predictive maintenance** for industrial machinery using the [AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/ml/datasets/AI4I+2020+Predictive+Maintenance+Dataset). The system predicts equipment failure from sensor data (temperature, RPM, torque, tool wear) before it happens — saving $10,000+ per prevented failure.

### Key Results

| Model | Accuracy | F1 Score | ROC-AUC | Cost |
|-------|----------|----------|---------|------|
| Rule-Based | 8.15% | 0.049 | 0.376 | $1,118,000 |
| Logistic Regression | 82.10% | 0.242 | 0.906 | $283,500 |
| Random Forest | 98.15% | 0.654 | 0.968 | $332,000 |
| Gradient Boosting | 98.50% | 0.750 | 0.968 | $233,500 |
| **XGBoost** ⭐ | **98.45%** | **0.774** | **0.966** | **$158,000** |
| Neural Network | 98.00% | 0.661 | 0.974 | $295,500 |

> **XGBoost wins** with the best F1 score (0.774) and lowest operational cost ($158,000), reducing false alarms by 99% compared to rule-based monitoring.

---

## 🏗️ Project Structure

```
MechSense/
├── index.html                    # Interactive web dashboard (frontend)
├── MechSense_ML_Pipeline.ipynb   # Full ML pipeline (training, evaluation, analysis)
├── ai4i2020.csv                  # AI4I 2020 dataset (10,000 records)
├── README.md
├── .gitignore
└── LICENSE
```

---

## 🚀 Features

### 📊 Interactive Web Dashboard (`index.html`)
- **Live Prediction Engine** — Adjust sensor sliders and get real-time failure predictions from all 6 models simultaneously
- **Exploratory Data Analysis** — Visual breakdowns of torque, tool wear, failure modes, and feature correlations
- **Model Comparison** — Side-by-side metrics for all models with visual indicators
- **Feature Importance** — Random Forest importances showing torque and RPM as top predictors
- **Cost Analysis** — Business impact of each model's prediction errors ($500/false alarm, $10,000/missed failure)

### 🧠 ML Pipeline (`MechSense_ML_Pipeline.ipynb`)
- Data preprocessing & feature engineering
- Class imbalance handling with balanced weighting (28.5:1 ratio)
- 6 model training & hyperparameter tuning
- Evaluation with confusion matrices, ROC curves, and cost analysis
- Feature importance analysis

---

## 📦 Dataset

**AI4I 2020 Predictive Maintenance Dataset**

| Attribute | Value |
|-----------|-------|
| Total samples | 10,000 |
| Failure cases | 339 (3.39%) |
| Machine types | H (High), M (Medium), L (Low) |
| Failure modes | TWF (46), HDF (115), PWF (95), OSF (98), RNF (19) |
| Features | Machine Type, Air Temp, Process Temp, RPM, Torque, Tool Wear |
| Imbalance ratio | 28.5 : 1 |

---

## 🛠️ Tech Stack

- **Python 3.8+** — Core ML pipeline
- **scikit-learn** — ML models and evaluation
- **XGBoost** — Best-performing model
- **Chart.js** — Interactive data visualizations
- **HTML / CSS / JavaScript** — Frontend dashboard (no frameworks needed)

---

## 📖 How to Use

### View the Dashboard
Simply open `index.html` in any modern browser — no server required!

Or visit the live version: [**arnavs10.github.io/MechSense**](https://arnavs10.github.io/MechSense/)

### Run the ML Pipeline
```bash
# Install dependencies
pip install pandas numpy scikit-learn xgboost matplotlib seaborn

# Open the notebook
jupyter notebook MechSense_ML_Pipeline.ipynb
```

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Arnav Shukla**  
GitHub: [@Arnavs10](https://github.com/Arnavs10)

---

*Built as part of Latest Advances in Engineering & Technology (CSET-395)*
