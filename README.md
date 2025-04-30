# Loan Approval Project 💸💰
This project aims to predict loan approval outcomes based on applicant data using supervised machine learning models. The dataset, sourced from Kaggle, contains a variety of features such as applicant income, credit history, education level, and loan amount.
The goal is to build a predictive model that can assist financial institutions in automating loan eligibility assessments, reducing manual workload, and making faster, data-driven decisions. By analyzing key patterns through Exploratory Data Analysis (EDA) and applying classification models (e.g., Logistic Regression, Random Forest, Decision Tree, and XGBoost), this project seeks to uncover the most influential factors behind loan approvals ✔️ and denials ❌.


## **Dataset**  
- **Source**: 👉 [Kaggle Loan Approval Dataset](https://www.kaggle.com/datasets/lorenzozoppelletto/financial-risk-for-loan-approval) 👈
- **Features**: Includes applicant details (e.g., income, credit history, loan amount, etc.).  
- **Target Variable**: `LoanApproved` (Approved/Rejected).

## **Tech Stack**  
- **Python** (Pandas, NumPy, Scikit-learn)  
- **Visualization**: Matplotlib/Seaborn  
- **Model**: Logistic Regression, Random Forest, Decision Tree and XGBoost

## **Project Steps**  📈
1. **Data Cleaning**: Handling missing values, outliers, etc.  
2. **EDA**: Exploratory Data Analysis (visualizations, correlations).  🔍
3. **Feature Engineering**: Scaling, encoding categorical variables.  ⚛️
4. **Model Training**: Comparison of multiple algorithms.  📖
5. **Evaluation**: Metrics like accuracy, precision, ROC-AUC. 📚

## **Exploratory Data Analysis** 🔍
### 1. **Loan Status**
23.83% loan approved
![Loan Approval](Image%20Chart/Loan%20Approval.png)
----

### 2. **Age Distribution**
People aged 30–45 represent the group with the highest number of debitors. It shows that individu in the productive age group tend to apply more loans.
![Age Distribution](Image%20Chart/Age%20Distribution.png)
----

### 3. **Education Distribution**
There is a clear positive correlation between annual income and education level. Borrowers who have education level as Doctorate and Master’s earn significantly more than those with lower degrees.
![Education Distribution](Image%20Chart/Edu%20distribution.png)
----

### 4. **Employment Status**
The majority of borrowers are employees, with a total of 16,911 loan requests.
![Age Distribution](Image%20Chart/Employment.png)
----

### 5. **Loan Purpose**
The primary purpose for most borrowers applying for personal loans is for home-related expenses, with a total of 5,881 loans. However, a portionof borrowers also use their loans for
debt consolidation.
![Loan Purpose](Image%20Chart/Loan%20Purpose.png)
----

### 6. **Feature Importance**
![Feature Importance](Image%20Chart/Feature%20Important.png)
----

## **🧠 Modeling**
This project applies various classification models to predict whether a loan application will be approved. The modeling pipeline follows a systematic approach:
### 1. Baseline
  * Model: Logistic Regression
  * Purpose: Establish a benchmark for evaluating advanced models
  * Result: Served as a sanity check with interpretable outputs

### 2. Advance Models
  ✅ Decision Tree
  ✅ Random Forest
  ✅ XGBoost Classifier

### 3. Handling Imbalance Data
  * Method : SMOTE
  * Applied only during training to prevent data leakage

### 4. Cross Validation Strategy
Stratified K-Fold Cross-Validation was used to ensure the model's robustness and avoid overfitting. A classification threshold of 0.8 was applied to make final predictions, focusing on reducing false positives

### 5. Hyperparameter Tuning
  * Method: RandomizedSearchCV
  * Tuned models for optimal performance using metrics such as precision and ROC-AUC

### 6. Evaluation Metrix
  * Precision
  * Recall
  * F1 Score
  * ROC-AUC

### 7. Best Model

| Model            | Precision | Recall | F1 Score | ROC-AUC |
|------------------|-----------|--------|----------|---------|
| Logistic Reg     | 0.802      | 0.745   | 0.772     | 0.894    |
| Decision Tree    | 0.648      | 0.680   | 0.664     | 0.834    |
| Random Forest 🌟 | **0.829**  | 0.692   | 0.754     | 0.891    |
| XGBoost          | 0.749      | 0.734   | 0.763     | 0.890    |

The Random Forest classifier outperformed other models, showing strong precision and stable performance across folds.
