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

