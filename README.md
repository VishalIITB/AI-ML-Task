#Credit Card Fraud Detection

This project aims to detect fraudulent transactions using supervised (Logistic Regression, XGBoost) and unsupervised (Isolation Forest) machine learning models on a highly imbalanced dataset. Interpretability tools like LIME are used to explain individual predictions.

##Key Choices Made

 -Data Preprocessing:

    -Standardized the Amount feature.

    -Addressed class imbalance via stratified sampling (optional oversampling methods discussed).

-Model Selection:

    -Supervised Models: Logistic Regression and XGBoost.

    -Unsupervised Model: Isolation Forest for anomaly detection.

-Evaluation Metrics:

    -Precision, Recall, F1-Score, and Accuracy.

    -ROC Curve and PR Curve for visual analysis.

-Interpretability:

    -Used LIME for model-agnostic explanation of sample predictions.

    -Saved .png for visual inspection on GitHub.

##Visualizations

-Confusion Matrix for both models.

-ROC & PR Curves to assess model performance under class imbalance.

-LIME plots for selected predictions.

##Unsupervised Anomaly Detection (Isolation Forest)

-Trained on majority (non-fraud) class only.

-Predicted anomalies were compared to known frauds.

-Detected a significant number of true positives, though with false positives.

##References

-Kaggle Credit Card Fraud Dataset

-LIME Documentation

-XGBoost & scikit-learn documentation



