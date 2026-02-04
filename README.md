📊 Customer Churn Prediction Project



🔍 Project Overview

This project focuses on predicting customer churn using the Telco Customer Churn dataset.

The goal is to identify customers likely to churn and compare different machine learning models

based on their ability to detect the minority (churn) class.


🧹 Data Preprocessing

Removed features that cause data leakage (e.g. Churn Reason, Churn Score).


Dropped high-cardinality and non-informative features (IDs, location fields).


Handled missing values using most frequent imputation.


Applied:


One-Hot Encoding for low-cardinality categorical features


Ordinal Encoding for binary features


Standard Scaling for numerical features



⚖️ Class Imbalance Handling

Compared class_weight="balanced" vs SMOTE.


Chose class_weight as the final approach to keep data realistic and avoid synthetic samples.



🤖 Models Used

Logistic Regression (baseline, interpretable)


Random Forest (non-linear, feature interactions)


XGBoost (boosting-based ensemble)


All models were tuned using GridSearchCV with F1-score as the main metric.


🎯 Threshold Tuning

Applied threshold tuning (instead of default 0.5), especially for XGBoost.


Improved recall–precision trade-off for the churn class.


Selected the threshold that maximized F1-score.


📈 Results Summary

Model	                F1	    AUC	    Accuracy	 Precision (Churn) 	Recall (Churn)

XGBoost	              0.67	  0.86	   0.77          	0.56             	0.83

Random Forest	        0.66	  0.86	   0.77          	0.56	            0.79

Logistic Regression	  0.65	  0.85	   0.75	          0.54	            0.80



✅ XGBoost achieved the best overall balance, especially after threshold tuning.


🧠 Key Insights

Precision for churn is lower due to class imbalance and overlapping feature patterns.


High recall is preferred in churn prediction to avoid missing churned customers.


Threshold tuning is critical and can be more impactful than changing the model itself.


🚀 Conclusion

The project demonstrates a full end-to-end churn prediction pipeline, including preprocessing, imbalance handling, model comparison, threshold tuning, and performance interpretation.
The results are realistic, well-validated, and suitable for real-world business use.


Author 

Ameen Nasairah

