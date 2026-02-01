#  Sampling Techniques & Model Performance Analysis

## Overview
This project analyzes the impact of different **sampling techniques** on **binary classification performance** using a **Credit Card Fraud Detection** dataset.  
Since the dataset is **highly imbalanced**, appropriate sampling and evaluation strategies are applied to ensure reliable and unbiased model performance.

---

## 📂 Dataset

The dataset used in this project was obtained from the following GitHub repository:

🔗 **Dataset Source:**  
https://github.com/AnjulaMehto/Sampling_Assignment/blob/main/Creditcard_data.csv

### Dataset Description
- **Dataset Name:** Credit Card Transactions  
- **Target Variable:** `Class`  
  - `0` → Non-Fraudulent Transaction  
  - `1` → Fraudulent Transaction  
- **Key Challenge:** Severe class imbalance, where fraudulent transactions are significantly fewer than non-fraudulent ones.

This imbalance makes the dataset well-suited for studying the impact of different sampling techniques and evaluation strategies on binary classification performance.

---

##  Methodology Workflow

The following diagram illustrates the **complete workflow implemented in `code.ipynb`**, from data loading to final evaluation and visualization.

![Methodology Flowchart](images/flowchart.png)

---

## Sampling & Evaluation Techniques Used

The following techniques were implemented and analyzed:

1. **Simple Random Sampling**  
2. **Cross-Validation (Stratified K-Fold)**  
3. **Stratified Sampling**  
4. **Cluster Sampling**  
5. **Bootstrap Sampling**

> ⚠️ **Note:** Cross-Validation is treated as an **evaluation technique**, not as a fixed dataset.

---

## Machine Learning Models

The following classification models were trained and evaluated:

- Logistic Regression  
- Decision Tree  
- Random Forest  
- Support Vector Machine (SVM)  
- Naive Bayes  

---

## 📈 Performance Metric
- **Accuracy (%)**
- Cross-Validation scores represent the **average accuracy across all folds**

---

## 📉 Visualizations

### 📈 Model Accuracy Comparison (Line Plot)
![Accuracy Line Plot](images/accuracy_line_plot.png)

---

###  Performance Results (Accuracy %)
![Accuracy Table](images/table.png)

---

## Key Observations
- **Random Forest** consistently achieved the highest accuracy and stability.
- **Bootstrap Sampling** improved performance for tree-based models.
- **Cross-Validation** provided the most reliable and unbiased performance estimate.
- **Stratified Sampling** effectively preserved class balance.
- Accuracy alone can be misleading for imbalanced datasets; sampling choice is crucial.

---

## 🛠️ Technologies Used
- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  

---

## 📁 Repository Structure
```
Ass2/
├── code.ipynb
├── Creditcard_data.csv
├── README.md
└── images/
    ├── flowchart.png
    ├── accuracy_line_plot.png
    └── table.png
```


---

##  Model-wise Best Sampling Technique Analysis

Based on the experimental results obtained from different sampling and evaluation techniques, the following observations identify **which sampling technique yields the highest accuracy for each model**.

### 🔹 Logistic Regression
- **Best Technique:** Cross-Validation  
- **Highest Accuracy:** **98.70%**

### 🔹 Decision Tree
- **Best Technique:** Bootstrap Sampling  
- **Highest Accuracy:** **98.71%**

### 🔹 Random Forest
- **Best Technique:** Bootstrap Sampling  
- **Highest Accuracy:** **100.00%**

### 🔹 Support Vector Machine (SVM)
- **Best Technique:** Stratified Sampling  
- **Highest Accuracy:** **98.28%**

### 🔹 Naive Bayes
- **Best Technique:** Cluster Sampling  
- **Highest Accuracy:** **97.87%**

---

## Final Insight
The results clearly demonstrate that **no single sampling technique is optimal for all models**.  
Tree-based models perform best with **Bootstrap Sampling**, linear models benefit from **Cross-Validation**, and imbalance-sensitive models gain from **Stratified Sampling**.  
Therefore, selecting an appropriate sampling and evaluation strategy is essential for achieving reliable and robust performance on imbalanced classification problems.
