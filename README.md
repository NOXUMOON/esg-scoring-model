# 🔬 ESG Score Prediction Using Machine Learning

> **MSc Thesis Project** — Istanbul Aydın University  
> **Author:** Muhsin Rezai Shiraze  
> **Advisor:** Dr. Öğr. Üyesi Selçuk Şener  

---

## 📌 Overview

This project investigates the prediction of **ESG (Environmental, Social, and Governance) scores** for companies listed on the **Borsa Istanbul (BIST) Sustainability Index** using supervised Machine Learning algorithms.

The dataset includes **101 companies** with **539 features** covering financial indicators, sustainability report metrics, and ESG scores sourced from **Sustainalytics**, **MSCI**, and **S&P Global**.

---

## 🎯 Objectives

- Collect and preprocess ESG and financial data from BIST Sustainability Index companies
- Apply and compare multiple ML regression algorithms for ESG score prediction
- Evaluate the impact of dimensionality reduction (PCA) on model performance
- Identify the most influential features for ESG score prediction

---

## 🗂️ Project Structure

```
esg-scoring-model/
│
├── 📁 data/
│   ├── final_dataset.csv                          # Main dataset (101 companies, 539 features)
│   ├── sustainanalytics_esg_v1.csv                # ESG scores from Sustainalytics (batch 1)
│   ├── sustainanalytics_esg_v2.csv                # ESG scores from Sustainalytics (batch 2)
│   └── esg-score-calculation-reference.xlsx       # ESG scoring methodology reference
│
├── 📁 notebooks/
│   ├── 01_model_raw.ipynb                         # ML models — full dataset with ESG features
│   ├── 02_model_raw_no_additional_esg.ipynb       # ML models — without additional ESG features
│   ├── 03_model_with_pca.ipynb                    # ML models + PCA — full dataset
│   └── 04_model_with_pca_no_additional_esg.ipynb  # ML models + PCA — without additional ESG features
│
├── requirements.txt
└── README.md
```

---

## 🤖 Machine Learning Models

All notebooks experiment with the following regression algorithms:

| Model | Type |
|---|---|
| Linear Regression | Linear |
| Lasso Regression | Linear + L1 Regularization |
| Ridge Regression | Linear + L2 Regularization |
| Random Forest | Ensemble (Bagging) |
| Gradient Boosting | Ensemble (Boosting) |
| Support Vector Regressor (SVR) | Kernel-based |
| K-Nearest Neighbors (KNN) | Instance-based |

---

## 📊 Results Summary

| Model | Train R² | Test R² | MSE | MAE |
|---|---|---|---|---|
| Linear Regression | 0.72 | 0.68 | 3.2 | 1.3 |
| Lasso Regression | 0.71 | 0.67 | 3.3 | 1.4 |
| Ridge Regression | 0.72 | 0.68 | 3.2 | 1.3 |
| **Random Forest** | **0.95** | **0.84** | **1.1** | **0.7** |
| **Gradient Boosting** | **0.93** | **0.82** | **1.3** | **0.8** |
| SVR | 0.65 | 0.61 | 4.0 | 1.6 |
| KNN | 0.75 | 0.64 | 3.7 | 1.5 |

> ✅ **Random Forest** achieved the best performance with Test R² of **0.84** and MSE of **1.1**

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square&logo=matplotlib&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

---

## ⚙️ Installation & Usage

**1. Clone the repository**
```bash
git clone https://github.com/noxumoon/esg-scoring-model.git
cd esg-scoring-model
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the notebooks**

Open Jupyter Notebook and run in this order:
- Start with `01_model_raw.ipynb` for baseline results
- Run `02_model_raw_no_additional_esg.ipynb` to see the impact of removing ESG-related features
- Run `03_model_with_pca.ipynb` and `04_model_with_pca_no_additional_esg.ipynb` for PCA experiments

---

## 📈 Dataset

- **Source:** BIST Sustainability Index companies — data collected from Sustainalytics, KAP, and financial reports
- **Size:** 101 companies × 539 features
- **Features include:** Financial metrics (revenue, assets, liabilities), ESG scores, risk ratings, industry rankings, and sustainability report indicators (encoded as A1.1, A1.2, B1, B2, etc.)
- **Target variable:** ESG Score

---

## 📄 License

This project is part of an academic MSc thesis. Data sourced from publicly available ESG platforms and financial disclosures.

---

## 📫 Contact

**Muhsin Rezai Shiraze**  
📧 muhsin.shiraze@gmail.com  
💼 [LinkedIn](https://linkedin.com/in/muhsin-rezai-shiraze)  
🐙 [GitHub](https://github.com/noxumoon)
