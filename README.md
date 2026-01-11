<<<<<<< HEAD
***Credit Card Fraud Detection***

This project implements a machine learning model to identify fraudulent credit card transactions. The primary focus of this project was navigating the challenges of highly imbalanced data and ensuring high recall to catch as many fraudulent cases as possible.

**📊 Dataset Overview**

The project uses a dataset containing transactions made by European cardholders.
Total Transactions: 284,807
Genuine Transactions: 284,315
Fraudulent Transactions: 492
Imbalance: Fraud represents only 0.17% of the total data.

**🛠️ Project Workflow**

**1. Data Preprocessing & Scaling**

Initially, the Logistic Regression model failed to converge due to the diverse scales of features like Time and Amount.
Solution: Applied StandardScaler to normalize the feature set.
Result: Reduced training time from 1.9s to 0.2s and resolved the ConvergenceWarning.

**2. Handling Class Imbalance**

The baseline model struggled to identify fraud cases because they were so rare.
Approach: Implemented class_weight='balanced' within the Logistic Regression classifier.
Impact: This penalized the model more heavily for missing a fraud case than for misclassifying a genuine one.

**📈 Results & Performance**

The final model achieved a significant improvement in detecting fraudulent activity.
Metric         Result
Recall (Fraud)  93%
Accuracy        97.5%
Missed Frauds   12
Caught Frauds   159

**Confusion Matrix**

The final confusion matrix demonstrates the model's high sensitivity to the fraud class

**🚀 Key Takeaways**

Recall vs. Precision: In fraud detection, a high recall is often prioritized over precision to minimize the financial loss from undetected fraud.
Feature Scaling: Essential for gradient-based solvers like Logistic Regression to converge efficiently.
Cost-Sensitive Learning: Adjusting class weights is an effective way to handle extreme class imbalance without needing to generate synthetic data.

**💻 Tech Stack**

Language: Python 3.11
Libraries: Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
=======
# credit_card_fraud_detection
Credit Card Fraud Detection
>>>>>>> 84339642f68d97c4a3e4d237204cdad263da4368
