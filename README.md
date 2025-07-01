
# Predicting-Term-Deposit-Subscriptions-using-Machine-Learning
End-to-end ML project predicting term deposit subscriptions using bank marketing data.

Predicting Term Deposit Subscriptions Using Machine Learning

This project focuses on predicting whether a bank client will subscribe to a term deposit using supervised machine learning models. It involves an end-to-end pipeline including data preprocessing, exploratory data analysis (EDA), feature engineering, handling class imbalance, model training, evaluation, and hyperparameter tuning.

Project Goal:
To assist marketing teams by predicting potential term deposit subscribers ahead of time using client data, enabling more targeted campaigns and efficient resource allocation.


Models Used:
1. Logistic Regression
2. Random Forest
3. Gradient Boosting
4. XGBoost (Tuned)

Final Result:
Best Model: Tuned XGBoost
ROC AUC on Test Set: 0.735
Accuracy: 0.88
Precision (Minority Class): 0.49
Recall (Minority Class): 0.31

Dataset: 
Source: UCI Bank Marketing Dataset(https://archive.ics.uci.edu/dataset/222/bank+marketing)

Size: 45,211 records with 17 features

Target Variable: y (whether the client subscribed to a term deposit)


Pipeline Overview:

1. Data Loading & Cleaning
2. Removed duplicates and placeholder values
3. Handled unknown values with mode imputation
4. EDA & Visualization
	Distribution plots, count plots, boxplots, correlation heatmap
5. Feature Engineering
	Interaction terms like housing_loan, contact_frequency, and success_ratio
	Log transformation of skewed features
6.Preprocessing
	Label encoding
	Standard scaling
	Outlier clipping using IQR
	Handling Imbalanced Data
	Applied SMOTE to balance classes

7. Model Training
	Trained and validated 4 models
	Evaluated using ROC AUC, Accuracy, Precision, Recall, F1-score
8. Hyperparameter Tuning
	Performed GridSearchCV for XGBoost and Gradient Boosting
9. Final Evaluation


Key Takeaways:

XGBoost (Tuned) was the best-performing model.

SMOTE improved recall on the minority class (subscribers).

Features like month, poutcome, and contact_frequency were most predictive.

Class imbalance remains a challenge for recall.



Final Model Performance (Test Set)

| Model             | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|------------------|----------|-----------|--------|----------|---------|
| XGBoost (Tuned)  | 88%      | 0.49      | 0.31   | 0.38     | 0.735   |
| Gradient Boosting| 88%      | 0.47      | 0.29   | 0.36     | 0.733   |

Despite class imbalance, tree-based models performed well on real data.




Next Steps:
Further improve minority class recall (possibly by threshold tuning or ensemble stacking)

Model explainability with SHAP/LIME

Deploy the trained model via REST API or Streamlit dashboard


Repository Structure:

. Predict-Term-Deposit-ML/
├── dataset/
│ └── bank-full.csv
├── plots/
│ ├── eda/
│ ├── evaluation/
│ └── final_evaluation/
├── Predicting Term Deposit Subscriptions Using Machine Learning.ipynb
├── Predicting Term Deposit Subscriptions Using Machine Learning.pdf
├── Predicting Term Deposit Subscriptions Using Machine Learning.html
└── README.md


By
Lohith Basavanahalli Anjinappa


