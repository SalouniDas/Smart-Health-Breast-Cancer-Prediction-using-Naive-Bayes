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

This repository contains a data mining project focused on predicting and classifying breast cancer tumors as either **Malignant** or **Benign**. The project was developed as part of a Master's course curriculum utilizing the **Naive Bayes** classification algorithm.

## 📌 Project Overview
Early detection of breast cancer significantly increases the chances of successful treatment. This project implements a Gaussian Naive Bayes classifier to analyze clinical characteristics of breast mass features extracted from digitized images of fine needle aspirates (FNA).

### Key Features:
* **Exploratory Data Analysis (EDA):** Feature distribution, correlation matrix visualization, and dataset balancing checks.
* **Data Preprocessing:** Handling missing values, feature scaling, and train-test splitting.
* **Model Implementation:** Scikit-Learn's Gaussian Naive Bayes model.
* **Evaluation Metrics:** Detailed analysis using Accuracy, Precision, Recall, F1-Score, and a Confusion Matrix.

---

## 📊 Dataset
The project utilizes the **Wisconsin Diagnostic Breast Cancer (WDBC)** dataset. 
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
├── docs/
│   └── Smart_Health_Paper.docx          # Project documentation/report
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
1. Clone this repository:
```bash
git clone [https://github.com/SalouniDas/Smart-Health-Breast-Cancer-Prediction-using-Naive-Bayes.git](https://github.com/SalouniDas/Smart-Health-Breast-Cancer-Prediction-using-Naive-Bayes.git)
```

2. Navigate to the directory:
```bash
cd Smart-Health-Breast-Cancer-Prediction-using-Naive-Bayes
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook
```
Open and run notebooks/NaiveBayes.ipynb.

---

## 📈 Results & Insights
### 📊 Model Evaluation Results

After training the Gaussian Naive Bayes model, the following performance metrics were achieved on the test dataset:

| Metric | Score |
| :--- | :--- |
| **Accuracy** | 94.7% |
| **Precision (Malignant)** | 93.5% |
| **Recall / Sensitivity** | 92.1% |
| **F1-Score** | 92.8% |

### Confusion Matrix Insights
* **True Positives (TP):** Correctly identified malignant tumors.
* **False Positives (FP):** Benign tumors misclassified as malignant (Type I Error).
* **False Negatives (FN):** Malignant tumors misclassified as benign (Type II Error — *critical to minimize in healthcare!*).

Key Takeaways: Naive Bayes performs exceptionally well as a baseline classifier because of its speed and efficiency, despite its underlying assumption of feature independence.
