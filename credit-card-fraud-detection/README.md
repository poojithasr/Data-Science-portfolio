Credit-card-fraud-detection/README.md
# 💳 Credit Card Fraud Detection & Prevention

This project uses a real-world credit card transaction dataset from the western United States to build machine learning models for detecting fraudulent transactions.
The primary objective is to accurately identify fraud while prioritizing high recall, reflecting a business requirement to minimize missed fraud even if it results in additional false positives.

## 📂 Dataset Overview

The dataset contains credit card transactions made by customers in the western United States.
Each record represents a single transaction, including customer information, merchant details, transaction location, and a fraud label.

1. Training dataset: fraudTrain.csv
2. Test dataset: fraudTest.csv

The data was sourced from Kaggle and partially cleaned and adapted by DataCamp.

## 📑 Column Descriptions

1. trans_date_trans_time: Date and time of the transaction
2. merchant: Merchant name
3. category: Merchant category (e.g., grocery_pos, shopping_net)
4. amt: Transaction amount
5. city: City of the credit card holder
6. state: State of the credit card holder
7. lat: Latitude of the transaction location
8. long: Longitude of the transaction location
9. city_pop: Population of the card holder’s city
10. job: Job of the credit card holder
11. dob: Date of birth of the credit card holder
12. trans_num: Unique transaction identifier
13. merch_lat: Latitude of the merchant location
14. merch_long: Longitude of the merchant location
15. is_fraud: Target variable (1 = Fraud, 0 = Legitimate transaction)

## 🎯 Project Goal

1. Perform Exploratory Data Analysis (EDA) to understand fraud patterns across:
  - Transaction amount
  - Time of day and day of week
  - Merchant category
  - Geography and merchant distance
  - Customer age and city population
2. Engineer meaningful behavioral and contextual features.
3. Train and evaluate multiple machine learning models.
4. Select a model that maximizes fraud recall while maintaining an acceptable false-positive rate.
5. Translate model performance into business-relevant insights.

## 🔍 Exploratory Data Analysis Highlights

- Fraud is strongly concentrated during late-night and early-morning hours.
- Online shopping categories show significantly higher fraud rates.
- Fraudulent transactions tend to involve larger transaction amounts.
- Geographic features (state, city population, merchant distance) provide contextual rather than standalone predictive power.
- Customer age shows a mild U-shaped relationship with fraud risk.

## ⚙️ Feature Engineering

1. Created log-transformed features for skewed variables:
  - Transaction amount
  - Merchant distance
  - City population
2. Extracted temporal features:
  - Cyclical encoding of hour (sin, cos)
  - Late-night activity indicator
  - Weekend indicator
3. Derived customer age from date of birth.
4. One-hot encoded merchant category.
5. Ensured consistent preprocessing for both training and test datasets.

## 🤖 Models Trained

Logistic Regression (baseline model)
Random Forest Classifier
Gradient Boosting Classifier

## 📊 Model Evaluation Metrics

Each model was evaluated using:
- Fraud Recall
- False Positives
- Missed Fraud Cases (False Negatives)
- Precision–Recall AUC (PR-AUC)

## 🏆 Final Model Selection
Gradient Boosting was selected as the final model, achieving:
  - 98%+ fraud recall on the test dataset
  - Very low missed fraud cases
  - Comparable false-positive rates to Random Forest
This model best satisfied the requirement to err on the side of caution while maintaining operational feasibility.

## ⚙️ Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook for analysis and modeling

# 🚀 How to Run

Clone the repository:
```bash
git clone https://github.com/poojithasr/Data-Science-portfolio.git
cd Data-Science-portfolio
cd credit-card-fraud-detection
```

Install dependencies:
```bash
pip install -r requirements.txt
```

Run the notebooks:
```bash
jupyter notebook
```

## 📌 Notes

- The dataset is highly imbalanced, making accuracy an unreliable metric.
- Recall and business impact were prioritized over precision.
- Threshold tuning plays a critical role in balancing fraud detection and operational cost.
- This project emphasizes real-world tradeoffs and ethical considerations in financial fraud detection.
