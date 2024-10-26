# MeXE402_Midterm_Catambay_De-Leon
# Credit Card Fraud Detection
# Problem Statement
As for many banks, keeping highly profitable customers is their top priority. However, banking fraud significantly threatens this objective across various institutions. This issue raises concerns regarding financial losses, trust, and credibility for both banks and their customers.

In the banking sector, using machine learning for credit card fraud detection has become essential for implementing proactive monitoring and fraud prevention strategies. Machine learning aids these institutions in minimizing the time spent on manual reviews, reducing costly chargebacks and fees, and preventing the denial of legitimate transactions.

In this project, we aim to identify fraudulent credit card transactions using machine learning models. We will examine customer-level data gathered during a research partnership between Worldline and the machine learning group.

# Dataset Content
The dataset includes credit card transactions from European cardholders that took place in September 2013. It encompasses transactions over two days, with a total of 284,807 transactions, of which 492 are fraudulent. This dataset is highly imbalanced, with the fraudulent transactions representing only 0.172% of the total.

The dataset consists solely of numerical input variables resulting from a PCA transformation. Due to confidentiality concerns, we cannot disclose the original features or provide additional background information. Features V1, V2, ..., V28 represent the principal components derived from PCA, while the features 'Time' and 'Amount' have not undergone PCA transformation. The 'Time' feature indicates the seconds that have passed since the first transaction, and the 'Amount' feature represents the transaction amount, which can be utilized for example-dependent cost-sensitive learning. The 'Class' feature serves as the response variable, with a value of 1 indicating fraud and 0 indicating a legitimate transaction.

Given the class imbalance, we suggest evaluating accuracy using the Area Under the Precision-Recall Curve (AUPRC), as the accuracy derived from a confusion matrix is not a reliable measure for imbalanced classifications.

