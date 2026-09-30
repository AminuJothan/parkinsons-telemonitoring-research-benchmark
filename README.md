# Parkinson's Disease Telemonitoring: A Benchmarking Study

A machine learning benchmarking project that uses daily voice recordings to track and predict Parkinson's disease progression—**successfully outperforming previous published literature baselines.**

## 🎯 What This Project Is About
Parkinson's disease affects movement and daily life. Doctors use specific scoring scales—**Motor UPDRS** (physical movement) and **Total UPDRS** (overall symptoms)—to measure how advanced the condition is. 

Instead of relying only on in-person hospital visits, this project explores how remote voice data (like pitch, jitter, and vocal tremors) can estimate these clinical scores. More importantly, this study serves as a **rigorous benchmark**, comparing our custom approach directly against previously published articles—and **achieving superior performance results.**

---

## 🏆 What Makes This Study Stand Out (The Benchmarking Edge)
- **Beating Previous Baselines:** Our pipeline achieves higher accuracy and better predictive performance compared to standard metrics reported in prior research articles.
- **Smart Data Safeguards:** We used strict validation techniques (like GroupKFold) to ensure the model was tested on completely unseen patients, proving its real-world reliability.
- **Independent Target Modeling:** Rather than lumping everything together, we built dedicated systems to separately master **Motor UPDRS** and **Total UPDRS** progression scores.

---

## 🛠️ How It Works (Step-by-Step)
1. **Cleaning & Refining:** Real-world telemonitoring data is cleaned to remove background noise and temporary voice anomalies.
2. **Feature Selection:** We use L1 Lasso feature selection to pinpoint the exact voice measurements that truly matter, cutting out unnecessary noise.
3. **Dual Model Training:** We train two distinct, high-performance models for Motor and Total UPDRS scores.
4. **Instant Deployment:** Both final models are saved as ready-to-use `.pkl` files for instant predictions.

---

## 📦 What's Inside This Folder
- 📄 **Parkinson_Disease_Telemonitoring.ipynb:** The complete, step-by-step code notebook showing the data pipeline, feature selection, and model training.
- 🤖 **Serialized Model Files (`.pkl`):** The saved machine learning models for both Motor and Total UPDRS scores.
- 📊 **Dataset Files:** The telemonitoring data used for training and benchmarking.
- 📝 **README.md:** This project guide.

---

## 🚀 Getting Started
To review or run the project:
1. Open **`Parkinson_Disease_Telemonitoring.ipynb`** in VS Code or Jupyter Notebook.
2. Run through the cells to see the entire benchmarking pipeline and how it outperforms traditional baselines!