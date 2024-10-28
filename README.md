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




# World Happiness Report
# Problem Statement
The World Happiness Report utilizes data from the Gallup World Poll to assess and rank the happiness levels of countries based on respondents' evaluations of their current lives using the Cantril ladder method. Despite the comprehensive rankings, there is a need to better understand how specific factors—such as economic production, social support, life expectancy, freedom, absence of corruption, and generosity—contribute to variations in happiness scores. This analysis aims to identify the underlying relationships between these factors and happiness levels, offering insights into why some countries achieve higher rankings than others compared to a hypothetical baseline (Dystopia). Ultimately, the goal is to leverage these findings to inform policy decisions that enhance overall well-being and quality of life on a national scale.

# Dataset Content
The happiness scores and rankings are derived from data collected by the Gallup World Poll. These scores are based on responses to a key life evaluation question included in the poll. This question, referred to as the Cantril ladder, asks participants to envision a ladder where a rating of 10 represents their best possible life and 0 represents the worst. Respondents then rate their current lives on this scale. The scores come from nationally representative samples collected between 2013 and 2016, using Gallup's weighting methods to ensure accurate representation. Following the happiness scores, additional columns detail how six factors—economic production, social support, life expectancy, freedom, absence of corruption, and generosity—affect life evaluations in each country compared to Dystopia, a hypothetical nation with values equivalent to the world’s lowest averages for these factors. While these factors do not alter the total happiness score for each country, they help explain the reasons behind varying rankings.
