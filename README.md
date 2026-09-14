#  FraudShield AI — Credit Card Fraud Detection

## About the Project

FraudShield AI is a machine learning project focused on detecting potentially fraudulent credit card transactions.

The main idea behind the project is simple: given transaction data, can we build a model that can distinguish between a normal transaction and a fraudulent one?

Since fraudulent transactions are much fewer than legitimate transactions, the project also looks at the challenge of imbalanced data and how it affects model performance.

We experimented with different machine learning approaches, compared their results, and built a simple fraud-risk scoring system to make the predictions easier to understand.

---

## What We Built

The project covers the complete machine learning workflow:

- Understanding and exploring the transaction dataset
- Studying the imbalance between fraud and legitimate transactions
- Preparing the data for machine learning
- Training Logistic Regression and Random Forest models
- Improving the training approach by balancing only the training data
- Applying feature scaling
- Comparing model performance
- Using Precision-Recall analysis
- Generating a fraud probability for a transaction
- Converting the probability into a simple risk level
- Looking at which features influence the model's predictions

---

## Why Fraud Detection?

Credit card fraud is a real-world problem where missing a fraudulent transaction can be costly.

One of the challenges is that fraudulent transactions are rare compared with normal transactions. Because of this, a model can have high accuracy while still failing to identify enough fraudulent transactions.

For this reason, we looked at metrics such as:

- Precision
- Recall
- F1-Score
- Precision-Recall AUC
- Confusion Matrix

rather than relying only on accuracy.

---

## Our Approach

We started by exploring the dataset and understanding the distribution of legitimate and fraudulent transactions.

To handle the class imbalance during training, we used under-sampling of legitimate transactions. In the improved approach, the original data is first divided into training and testing sets, and balancing is performed only on the training data.

We then trained and compared different models and applied feature scaling to Logistic Regression.

The final notebook also demonstrates how a model's fraud probability can be used to assign a simple risk level.

---

## Models Used

### Logistic Regression

Used as a baseline classification model and later as the main model for the improved approach.

### Random Forest

Used as a second machine learning approach so that we could compare its performance with Logistic Regression.

### Scaled Logistic Regression

Feature scaling was added to improve the consistency of the input features before training the Logistic Regression model.

---

## Risk Scoring

As a simple demonstration, the predicted fraud probability is converted into three risk levels:

| Fraud Probability | Risk Level |
|---|---|
| Below 30% | Low Risk |
| 30% – 70% | Medium Risk |
| Above 70% | High Risk |

These thresholds are only used for demonstration in this project and are not intended to represent production fraud thresholds.

---

## Dataset

The dataset contains:

- 284,807 transactions
- 492 fraudulent transactions
- 284,315 legitimate transactions
- 30 input features
- 1 target variable (`Class`)

The `Class` column represents:

- `0` → Legitimate transaction
- `1` → Fraudulent transaction

---

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Logistic Regression
- Random Forest

---

## Project Files

```text
credit-card-fraud-detection/
│
├── FraudShield_AI_Credit_Card_Fraud_Detection.ipynb
├── README.md
└── IBM_Bob_Usage.md
