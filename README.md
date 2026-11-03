# Credit Card Fraud Detection

A machine learning project that compares classification models to identify potentially fraudulent credit card transactions using historical data.

## Project Overview

Fraudulent transactions are rare compared with legitimate ones. This project uses labelled transaction data to train models and evaluate how well they detect fraud while limiting false alerts.

## Dataset

The project uses the public [Credit Card Fraud Detection dataset on Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).

- 284,807 transactions in the original dataset
- Features include `Time`, `V1`–`V28`, and `Amount`
- `Class = 0`: legitimate transaction
- `Class = 1`: fraudulent transaction
- The notebook removed 1,081 duplicate rows and found no missing values.
- The cleaned data contained 283,726 transactions, including 473 labelled as fraud.

The dataset is not included in this repository. Download `creditcard.csv` from Kaggle and upload it when running the notebook.

## Models

The project trains and compares:

- Logistic Regression
- Decision Tree
- Random Forest

Random Forest was selected because it achieved the highest validation F1 score among the three models tested.

## Results

Random Forest test-set results:

- Precision: **88%**
- Recall: **73%**
- F1 score: **0.80**
- Fraud cases detected: **69 of 95**
- Fraud cases missed: **26**
- Legitimate transactions incorrectly flagged: **9**

These results are from one test split and are not a guarantee of future performance.

## How to Run

1. Open the notebook in [Google Colab](https://colab.research.google.com/).
2. Run the cells in order.
3. When prompted, upload `creditcard.csv`.
4. Review the model comparisons, charts, and sample prediction.

## Limitations

- The data represents transactions from a limited time period and may not reflect current fraud patterns.
- Only 473 fraud examples remain after duplicate removal.
- The `V1`–`V28` features are anonymized.
- This is a learning prototype, not a live fraud detection service.

## Tools Used

Python, pandas, NumPy, scikit-learn, Matplotlib, Seaborn, and joblib.

## Disclaimer

This project is for educational purposes. Model predictions should not be used as the sole basis for real financial decisions.
