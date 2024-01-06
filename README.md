# Credit Card Fraud Detection
This model is based on anonymized credit card transactions.

It is important that credit card companies are able to recognize fradulent credit card transactions so that customers are not charged for times that they did not purchase.

## Data Understanding
The dataset contains transactions made by credit cards in Sep 2013 by Europen cardholers.
This data presents transactions that occured in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly imbalanced.

It contains only numerical inpur variable which are the result of PCA transformation, due to confidentiality purpose. Features V1 to V28 are the principal components obtained with PCA.
Feature 'Time' contains the seconds elasped between each transaction and the first transaction in dataset.
The feature 'Amount' is the transaction amount, this feature can be used for example-dependent cost-sensitive learning.
The feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 for legitimate transaction.

## Approach
This is a classic class-imbalance problem where the number of fraud transactions is much lesser than number of legitimate transactions.
If model built on such imbalanced data, chances of overfitting and model failing on unseen data gets significantly higher.
Hence, it can be approached as anomaly detection problem, where relation between different variables can be seen and based on that we can built model for better understanding.
For balancing the data, I have used SMOTE.

For evaluation used AUC-ROC Score, Classification Report, Accuracy, and F1-score.
