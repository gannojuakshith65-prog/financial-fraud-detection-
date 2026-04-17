Statistical Fraud Detection using Mahalanobis Distance and EWMA

📌 Overview

This project presents a statistical fraud detection model for financial transactions using Mahalanobis Distance and Exponentially Weighted Moving Average (EWMA). The model detects both global anomalies and behavioral changes in user transactions.

🚨 Problem Statement

Traditional fraud detection systems rely on rule-based or machine learning approaches, which often lack interpretability and require labeled data. This project aims to develop an explainable statistical model to detect suspicious transactions.

⚙️ Methodology

1. Mahalanobis Distance

Used to detect multivariate anomalies in transaction data.

2. EWMA (Exponentially Weighted Moving Average)

Used to track recent behavior and detect sudden changes.

3. Final Risk Score

Risk Score = 0.6 × Mahalanobis + 0.4 × EWMA

Transactions are classified into:

- Low Risk
- Medium Risk
- High Risk

📊 Dataset

A finance-specific synthetic dataset was created with features such as:

- Transaction amount
- International transaction flag
- Failed login count
- Device change flag
- New beneficiary flag
- IP risk score

📈 Results

- Most transactions are low risk
- A small number of transactions are flagged as high risk
- The model successfully detects anomalous behavior patterns

▶️ How to Run

1. Open the notebook:
   fraud_detection.ipynb

2. Run all cells

3. Use the interactive dropdown to select an account and analyze behavior

📌 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib

📎 Repository Link

(Add your GitHub link here)

👨‍💻 Contributors

(Add your team member names)
