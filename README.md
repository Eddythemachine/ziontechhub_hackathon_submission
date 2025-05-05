# ZionTechhub Hackathon Submission

Official submission for the ZionTechhub Hackathon 2025 (Data Science Category).  
A 3-week challenge focused on solving real-world problems using data-driven insights, analytics, and machine learning.  
**Submission Deadline:** May 6th, 2025

---

## Loan Risk Assessment Model

A machine learning solution to predict customer loan default risk based on demographic and financial attributes.

---

## Introduction

This project addresses the need for accurate and scalable credit risk assessment by financial institutions.  
Using applicant data such as income, profession, location, and ownership details, we train classification models to predict loan risk and enable smarter credit decisions.

---

## Objective

- Build a classification model to predict whether an applicant is "risky" or "not risky".
- Identify the most influential features contributing to applicant risk.
- Enhance decision-making capabilities in the credit approval process.

---

## Dataset Overview

The dataset consists of the following key features:

| Feature               | Description                                      |
|-----------------------|--------------------------------------------------|
| `Income`              | Applicant's annual income                        |
| `Age`                 | Applicant's age in years                         |
| `Experience`          | Total years of work experience                   |
| `Married/Single`      | Marital status                                   |
| `House_Ownership`     | Type of house ownership                          |
| `Car_Ownership`       | Whether the applicant owns a car                 |
| `Profession`          | Occupation type                                  |
| `CITY`, `STATE`       | Geographical information                         |
| `CURRENT_JOB_YRS`     | Years in current job                             |
| `CURRENT_HOUSE_YRS`   | Years at current residence                       |
| `Risk_Flag`           | Target variable — 1: Risky, 0: Not Risky         |

---

## Exploratory Data Analysis (EDA)

- Visualized distributions of income, age, and job experience.
- Plotted feature relationships with the target variable (`Risk_Flag`).
- Used histograms, boxplots, heatmaps, and pie charts to identify trends and patterns.

---

## Data Preprocessing

- Categorical features encoded using LabelEncoder, OneHotEncoder, and TargetEncoder.
- Numerical features scaled using `StandardScaler`.
- Addressed class imbalance using `SMOTE` to improve recall for the minority (risky) class.
- Split data into training and validation sets using `train_test_split`.

---

## Modeling and Evaluation

Trained and compared several classification algorithms:
- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost
- K-Nearest Neighbors
- Support Vector Machine
- Naive Bayes

Models were evaluated based on accuracy, ROC AUC score, and classification reports.

---

## Model Performance

**Best Model:** XGBoost Classifier



=== Model Performance ===
Accuracy: 0.8936
ROC AUC: 0.9338
Classification Report:
precision recall f1-score support


       0       0.97      0.91      0.94     35466
       1       0.54      0.77      0.64      4854

accuracy                           0.89     40320


macro avg 0.75 0.84 0.79 40320
weighted avg 0.92 0.89 0.90 40320


---

## Conclusion

- Ensemble models (Random Forest and XGBoost) demonstrated superior performance.
- Risk prediction was strongly influenced by income, profession, job tenure, and location.
- SMOTE significantly improved recall for the minority (risky) class.

---

## Future Improvements

- Perform hyperparameter optimization using `GridSearchCV`.
- Add model explainability with SHAP or LIME.
- Deploy the model via a web interface using Streamlit or Flask.
- Incorporate external financial and credit history data if available.

---

## How to Run

## 1. Clone this repository:

   ```bash
   git clone https://github.com/Eddythemachine/ziontechhub_hackathon.git
   cd ziontechhub_hackathon
```

## 2. Install dependencies:
pip install -r requirements.txt


## 3. Launch the notebook:
jupyter notebook loan_risk_assessment.ipynb

## Folder Structure

ziontechhub_hackathon/
├── data/
│   ├── train.csv
│   └── test.csv
├── models/
├── notebooks/
│   └── loan_risk_assessment.ipynb
├── README.md
└── requirements.txt

License
This project is licensed under the MIT License.

Acknowledgments
ZionTechhub Hackathon organizers

scikit-learn and imbalanced-learn

Kaggle and open-source contributors
