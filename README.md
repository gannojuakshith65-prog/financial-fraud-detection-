# 📊 Statistical Fraud Detection in Financial Transactions

## 🚀 Project Overview

This project presents a **statistical and explainable fraud detection model** for financial transactions using a hybrid approach combining:

* **Mahalanobis Distance** (global anomaly detection)
* **Exponentially Weighted Moving Average (EWMA)** (behavior tracking over time)

The goal is to identify **suspicious transactions** by analyzing both:

* how unusual a transaction is compared to all users
* how much it deviates from a user's recent behavior

---

## 🎯 Loopholes in existing systems

Traditional fraud detection systems in financial institutions suffer from:

* ❌ Over-reliance on static rule-based systems
* ❌ Lack of adaptability to new fraud patterns
* ❌ Dependency on labeled datasets in ML models
* ❌ Poor interpretability of decisions

This project aims to **address these gaps** using a statistical, interpretable approach.

---

## 💡 Proposed Solution

We propose a **hybrid fraud detection model** that combines:

### 1️⃣ Mahalanobis Distance

* Detects **global anomalies**
* Considers correlations between multiple features
* Identifies transactions far from normal behavior distribution

### 2️⃣ EWMA (Exponentially Weighted Moving Average)

* Tracks **user-specific behavior over time**
* Detects sudden spikes or deviations in transaction patterns

### 🔗 Final Risk Score

The final fraud risk score is computed as:

[
Risk Score = 0.6 × Mahalanobis + 0.4 × EWMA
]

Transactions are classified as:

* 🟢 Low Risk
* 🟡 Medium Risk
* 🔴 High Risk

---

## 📂 Dataset
File name is financial_fraud_synthetic.csv

A **finance-specific synthetic dataset** was generated to simulate real-world banking scenarios.

### Key Features:

* `amount` – transaction value
* `is_international` – foreign transaction indicator
* `failed_login_count` – number of failed login attempts
* `device_change_flag` – whether a new device was used
* `new_beneficiary_flag` – transfer to new beneficiary
* `ip_risk_score` – risk level of IP address
* `amount_to_balance_ratio` – transaction size relative to balance

### Engineered Features:

* `time_gap_minutes` – time between transactions
* `account_txn_count` – number of transactions per account
* `amount_deviation` – deviation from average behavior

---

## ⚙️ Methodology

### Step 1: Data Preprocessing

* Convert timestamps
* Sort transactions by account and time

### Step 2: Feature Engineering

* Compute behavioral and temporal features
* Capture user-level transaction patterns

### Step 3: Anomaly Detection (Mahalanobis Distance)

* Compute mean vector and covariance matrix
* Measure multivariate distance of each transaction

### Step 4: Behavior Tracking (EWMA)

* Calculate smoothed transaction trends
* Measure deviation from recent behavior

### Step 5: Risk Scoring

* Normalize scores
* Combine into final fraud risk score

---

## 📈 Results & Insights

* Majority of transactions are classified as **low risk**
* A small number of transactions show **high-risk spikes**
* Fraud patterns appear as **sudden deviations**, not continuous behavior

### Key Observation:

> Fraud is sparse — accounts appear normal most of the time but exhibit occasional high-risk transactions.

---

## 🔍 Interactive Analysis

The project includes an **interactive account-level analysis feature**:

* Select an `account_id`
* View:

  * transaction history
  * risk scores
  * EWMA vs actual amount graph
  * suspicious transactions

This helps in understanding **why a transaction is flagged as risky**.

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Jupyter Notebook / Google Colab

---

## 📊 Visualizations

* Mahalanobis score distribution
<img width="706" height="560" alt="WhatsApp Image 2026-04-18 at 00 40 38" src="https://github.com/user-attachments/assets/5fb928b1-f6bc-4dff-a1cd-8288d3a92139" />

* EWMA vs transaction amount graph(graph of most suspicious account in our data set)
<img width="715" height="605" alt="WhatsApp Image 2026-04-18 at 00 40 51" src="https://github.com/user-attachments/assets/7eaf9de1-ba5f-4c9d-b27a-8b242c313c7d" />

* Risk level distribution
<img width="696" height="600" alt="WhatsApp Image 2026-04-18 at 00 41 09" src="https://github.com/user-attachments/assets/10b1f902-e5cc-493c-a2ec-5010e2bcd0b0" />

---

## ✅ Advantages

* ✔️ No need for labeled data
* ✔️ Explainable and interpretable
* ✔️ Captures both global and user-level anomalies
* ✔️ Easy to extend and deploy

---

## ⚠️ Limitations

* Synthetic dataset (not real banking data)
* Sensitive to covariance matrix stability
* Not optimized for real-time systems

---

## 🔮 Future Work

* Integrate machine learning classifiers
* Use real-world financial datasets
* Deploy as a real-time fraud detection system
* Improve normalization and scaling techniques

---

## 📁 Project Structure

```
📦 Fraud-Detection-Project
 ┣ 📜 fraud_detection.ipynb
 ┣ 📜 financial_fraud_synthetic.csv
 ┣ 📜 README.md
```

---

## ▶️ How to Run

1. Open the notebook in **Google Colab** or Jupyter
2. Upload the dataset
3. Run all cells
4. Use the dropdown to analyze specific accounts

---

## 📌 Conclusion

This project demonstrates that a **hybrid statistical approach** can effectively detect fraud by combining:

* global anomaly detection
* temporal behavior analysis

while maintaining **interpretability**, which is crucial in financial systems.

---

## 👥 Team Members

* Gannoju Akshith  (2025AIB1024)
* Akshay krishna G (2025AIB1027)
* Adhyaan Aggarwal (2025AIB1003)
* Harnoor Singh    (2025AIB1028)
* Piyush Kothiwala (2025AIB1047)

---

## 🔗 Repository

https://github.com/gannojuakshith65-prog/financial-fraud-detection-/tree/main
