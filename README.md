# Smart Health: Breast Cancer Prediction using Naive Bayes
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Ubuntu&weight=600&size=22&pause=1200&color=1E40AF&center=true&vCenter=true&width=850&lines=Smart+Health%3A+Breast+Cancer+Prediction+%7C+Naive+Bayes;Data+Mining+Approach+for+Diagnostic+Classification;Wisconsin+Breast+Cancer+Dataset+(WDBC)+Analysis" alt="Typing SVG" />
</p>

---

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![Jupyter Notebook](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=flat&logo=Jupyter)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=flat&logo=numpy&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-green)

---

This repository contains a data mining project focused on predicting and classifying breast cancer tumors as either **Malignant** or **Benign**. The project was developed as part of a Master's course curriculum utilizing the **Naive Bayes** classification algorithm.

## 📌 Project Overview
Early detection of breast cancer significantly increases the chances of successful treatment. This project implements a Gaussian Naive Bayes classifier to analyze clinical characteristics of breast mass features extracted from digitized images of fine needle aspirates (FNA).

### 🚀 Key Features

* **Exploratory Data Analysis (EDA):** Comprehensive analysis of the WDBC dataset including feature distribution modeling, correlation matrix heatmaps to detect multicollinearity, and class balance checks.
* **Data Preprocessing Pipeline:** Automated pipeline handling missing value audits, feature scaling (Standardization), and stratified train-test splitting to maintain class proportions.
* **Multi-Model Machine Learning Framework:** Implemented and optimized four distinct classification algorithms to bench-test baseline performance:
  * 🧠 **Gaussian Naive Bayes** (Core Algorithm)
  * 📈 **Logistic Regression**
  * 🌲 **Decision Tree Classifier**
  * 👥 **K-Nearest Neighbors (KNN)**
* **Rigorous Evaluation Metrics:** Comparative performance analysis using cross-validation alongside multiple evaluation metrics including Accuracy, Precision, Recall (Sensitivity), F1-Score, and Confusion Matrix breakdowns to evaluate clinical safety (minimizing False Negatives).

---

## 📊 Dataset
The project utilizes the **Wisconsin Diagnostic Breast Cancer (WDBC)** dataset. 
🔗 https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic
* **Target Variable:** `Diagnosis` (M = Malignant, B = Benign)
* **Features:** 30 real-valued features computed from nuclear characteristics (e.g., radius, texture, perimeter, area, smoothness, concavity).

---

## 🧠 Theoretical Background

The Naive Bayes classifier is based on **Bayes' Theorem**, with the "naive" assumption of conditional independence between every pair of features given the value of the class variable.

The probability model for a classifier is a conditional model:

$$P(y \mid x_1, \dots, x_n) = \frac{P(y) \prod_{i=1}^{n} P(x_i \mid y)}{P(x_1, \dots, x_n)}$$

Where:
* $y$ represents the class variable (Malignant or Benign).
* $x_1, \dots, x_n$ represent the feature vectors (tumor radius, texture, etc.).

---

## 🛠️ Tech Stack & Dependencies
* **Language:** Python
* **Environment:** Jupyter Notebook
* **Libraries:** * `pandas` & `numpy` (Data manipulation)
  * `scikit-learn` (Machine Learning & Evaluation)
  * `matplotlib` & `seaborn` (Data Visualization)

---

## 📁 Project Structure

```text
├── data/
│   └── wdbc.csv                         # Raw Wisconsin Breast Cancer Dataset
├── notebooks/
│   └── NaiveBayes.ipynb                 # Jupyter Notebook with full EDA & Model
├── requirements.txt                     # Project dependencies
└── README.md                            # Project documentation
```

## 🚀 Getting Started

### Prerequisites
Ensure you have Python installed. You can install the required packages using:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn notebook
```
### Running the Project
Clone this repository:
```bash
git clone [https://github.com/SalouniDas/Smart-Health-Breast-Cancer-Prediction-using-Naive-Bayes.git](https://github.com/SalouniDas/Smart-Health-Breast-Cancer-Prediction-using-Naive-Bayes.git)
```
Open and run notebooks/NaiveBayes.ipynb.

---


## 📊 Model Comparison & Results

To evaluate the effectiveness of the **Gaussian Naive Bayes** classifier, it was benchmarked against three other standard machine learning models: **Decision Tree**, **K-Nearest Neighbors (KNN)**, and **Logistic Regression**. 

All models were evaluated on the same train-test split using the Wisconsin Diagnostic Breast Cancer dataset.

### 📈 Performance Comparison Matrix

| Model | Accuracy | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **K-Nearest Neighbors (KNN)** | **96.49%** | **0.96** | **0.96** | **0.96** |
| **Gaussian Naive Bayes** | 94.74% | 0.95 | 0.95 | 0.95 |
| **Logistic Regression** | 93.86% | 0.94 | 0.94 | 0.94 |
| **Decision Tree** | 93.86% | 0.94 | 0.94 | 0.94 |

---

### 🔍 Key Insights & Discussion
* **Why Naive Bayes?**
While models like Logistic Regression or Decision Trees may offer slightly different accuracy profiles, Naive Bayes serves as an excellent baseline because it requires minimal training time and works exceptionally well with low variance.
* **Why the Healthcare Context?**
In medical diagnoses like breast cancer screening, **Recall** (minimizing False Negatives) is often prioritized over overall accuracy, as missing a malignant tumor is far more dangerous than running a follow-up test on a false positive.

---

## 🔧 Future Extensions & Customization

This repository is designed to be an extensible framework for clinical data mining. You can easily adapt or scale this project in the following ways:

* **Incorporate Alternative Datasets:** Replace `wdbc.csv` in the `data/` folder with other clinical or oncology datasets (e.g., the MIAS Mammography dataset) to test model generalizability.
* **Advanced Feature Engineering:** Experiment with Principal Component Analysis (PCA) or recursive feature elimination (RFE) to reduce the 30 dimensional feature space and see how it impacts Naive Bayes performance.
* **Hyperparameter Tuning:** Utilize `GridSearchCV` to optimize hyperparameters for the benchmark models (such as tuning $k$ in KNN or adjusting the max depth of the Decision Tree).
* **Alternative Naive Bayes Variants:** If you discretize the continuous clinical features into categorical bins, you can experiment with swapping `GaussianNB` out for `MultinomialNB` or `ComplementNB` to compare variations of the core algorithm.

---
## 👩‍💻 Author
Salouni Das

