# parkinsons-telemonitoring-research-benchmark
A reproducible machine learning benchmarking study using the Parkinson's Telemonitoring dataset, evaluating multiple regression approaches for predicting motor and total UPDRS scores and comparing results with previously reported research.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Framework](https://img.shields.io/badge/Benchmarking-XGBoost%20%7C%20Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Active%20Research%20%2F%2F%20WIP-yellow)

## 🔬 Study Overview
This repository hosts a reproducible machine learning benchmarking study utilizing the **Parkinson’s Telemonitoring Dataset**. The primary objective is to rigorously evaluate and compare multiple regression architectures (such as XGBoost, regularized linear models, and ensemble methods) for predicting motor and total **UPDRS** (Unified Parkinson's Disease Rating Scale) progression scores. 

By enforcing strict data engineering safeguards—including leakage-free `GroupKFold` cross-validation, fold-specific scaling, and temporal feature extraction—this benchmark aims to provide an objective performance comparison against previously reported literature baselines.

> **Research Status Note:** This project is under active development. Experimental scripts, model evaluation metrics, and comparative baseline logs are continuously updated.

---

## ⚙️ Core Methodological Safeguards

* **Leakage-Free Validation (`GroupKFold`):** Partitions cross-validation strictly by unique patient identifiers (`subject#`), ensuring models are evaluated solely on unseen human subjects.
* **Longitudinal Feature Engineering:** Extracts short-term acoustic momentum (`velocity`) and moving averages (`rolling window = 3`) to filter out environmental noise and temporary vocal artifacts.
* **Fold-Specific Preprocessing:** Applies `StandardScaler` and `Lasso (L1)` feature selection exclusively *inside* training partitions to prevent data leakage and multicollinearity.
* **Independent Target Modeling:** Treats `motor_UPDRS_delta` and `total_UPDRS_delta` as separate regression tasks to honor clinical distinctions.

---

## 📊 Benchmarking Scope & Architecture

parkinsons-telemonitoring-research-benchmark/
├── data/               # Raw and processed dataset directory (see Data Access)
├── notebooks/          # Exploratory analysis and baseline prototyping scripts
├── MPS/                # Modular pipeline scripts (preprocessing, validation, models)
├── results/            # Performance evaluation logs and comparative metrics
├── requirements.txt    # Project dependencies
└── README.md           # Project documentation
