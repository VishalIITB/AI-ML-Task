# Credit Card Fraud Detection - Documentation

##  Model Performance Summary

### Supervised Models Performance

#### Logistic Regression
- Accuracy: 92%
- Precision (Fraud): 0.02
- Recall (Fraud): 0.95
- F1-Score (Fraud): 0.04

#### XGBoost
- Accuracy: 99.9%
- Precision (Fraud): 0.84
- Recall (Fraud): 0.96
- F1-Score (Fraud): 0.90

Clearly, XGBoost performs best in detecting fraudulent transactions with high precision and recall.


##  Visualizations

### Included:
- Confusion Matrix for Logistic Regression and XGBoost
- ROC & PR curves comparing classifiers
- Feature importance using LIME for model interpretability

##  Unsupervised Model: Isolation Forest

### Unsupervised Model: Isolation Forest
- Number of anomalies detected: 102
- True fraudulent transactions among those: 89
- Precision: 87.3%
- Recall: 90.8%

The model is effective as an early detector of frauds when labeled data is scarce.

##  Model Explainability

### Example 1: Predicted as Fraud (1.00)
- Actual Label: Fraud

- Predicted Probability: 1.00 (Highly confident)

Rank    	Feature	   Value	  Contribution
1	         V4	        3.32	   +0.02
2	         V14	     -9.07	   +0.01
3          V8	       -37.35	   +0.01
4         V12	      -4.61	     +0.01
5	        V20	      -3.49	     +0.01
6	        V11	       4.41	     +0.01
7	        V9	       -0.39	   +0.01
8	        V2	       12.79	   +0.01
9	       V13	      -1.91	     +0.00
10	   Std_Amount	  -0.29	     +0.00

These features, especially high positive V4 and very negative V14, V8, indicate an abnormal pattern, often associated with fraud.


### Example 2: Predicted as Non-Fraud (0.23)
- Actual Label: Non-Fraud

- Predicted Probability: 0.23 (Low fraud risk)

Rank	  Feature	    Value	  Contribution
1	     Std_Amount	  -0.22	    0.00
2	       V13	      -0.16	    0.00
3	       V3	         1.55	    0.00
4	       V21	       -0.15	  0.00
5	       V26	       0.08	    0.00
6       V19	       -0.05	    0.00
7	      V28	        0.11	    0.00
8	      V17	       -0.36	    0.00
9	      V5	        0.18	    0.00
10	   V15	        0.41	    0.00

These feature values fall within common/benign ranges, which the model associates with normal behavior.
