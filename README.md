# Credit Card Fraud Detection

## Overview
This project aims to detect fraudulent credit card transactions using machine learning techniques. The dataset used is the "creditcard.csv," which contains various features related to transactions, including a class label indicating whether a transaction is fraudulent.

## Table of Contents
- [Installation](#installation)
- [Data Exploration](#data-exploration)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Techniques Used](#techniques-used)
- [Conclusion](#conclusion)

## Installation
To run the project, ensure you have Python installed along with the required libraries. You can install the necessary libraries using:

```bash
pip install pandas numpy scikit-learn seaborn matplotlib imbalanced-learn
```

## Data Exploration
The dataset consists of 284,807 transactions and 31 features, including:

Time: Time elapsed since the first transaction.
V1-V28: Anonymized features.
Amount: Transaction amount.
Class: Indicates if the transaction is fraudulent (1) or not (0).
The dataset is imbalanced, with significantly more legitimate transactions than fraudulent ones.

## Data Preprocessing
Data Loading: The dataset is loaded using Pandas.
Handling Missing Values: Checked for and removed any missing values.
Normalization: The 'Amount' column is normalized using StandardScaler.
Dropping Irrelevant Features: The 'Time' column is dropped since it's not relevant for analysis.
Removing Duplicates: Duplicate records are removed to ensure data integrity.

## Modeling
Various machine learning models are implemented, including:

Logistic Regression
Decision Tree Classifier
Random Forest Classifier
Train-Test Split
The data is split into training and testing sets (80% train, 20% test).

### Model Training
Each model is trained on the training set, and predictions are made on the test set.

### Evaluation
Model performance is evaluated using metrics such as:

- Accuracy Score
- F1 Score
- Precision Score
- Recall Score

## Results
### Logistic Regression:
Accuracy: ~99.93%
F1 Score: ~0.74
### Decision Tree Classifier:
Accuracy: ~99.89%
F1 Score: ~0.69
### Random Forest Classifier:
Accuracy: ~99.94%
F1 Score: ~0.81
## Techniques Used
- Under-sampling: Balancing the dataset by randomly selecting a subset of legitimate transactions.
- Over-sampling: Using SMOTE (Synthetic Minority Over-sampling Technique) to generate synthetic examples of fraudulent transactions.


## Conclusion
This project demonstrates the application of machine learning techniques in detecting credit card fraud. The models provide high accuracy, but challenges remain due to the imbalanced nature of the dataset. Further work could include more advanced techniques for tackling class imbalance and exploring additional features.
