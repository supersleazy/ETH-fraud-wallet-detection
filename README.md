# Ethereum (ETH) Fraud Detection using Supervised Machine Learning

Detecting fraudulent Ethereum wallets using behavioral transaction analysis and supervised machine learning.

---

## Introduction

> Cryptocurrency scams and fraudulent wallet activity have become increasingly common with the growth of blockchain-based financial systems. Fraud Ethereum wallets are often involved in phishing, scam token distribution, suspicious ERC20 transfers, and abnormal transaction behavior.

The goal of this project was to explore whether machine learning models can identify fraud Ethereum wallets using behavioral transaction features and ERC20 activity patterns.

The project focuses on:
- behavioral analysis of Ethereum wallets
- exploratory data analysis
- fraud pattern detection
- machine learning-based classification

---

## Setup & Running the Jupyter Notebook:

1. Clone the Repository

```bash
git clone https://github.com/supersleazy/ethereum-fraud-detection.git
```

2. Navigate to the Project Folder

```bash
cd ethereum-fraud-detection
```

3. Install Required Libraries

```bash
pip install -r requirements.txt
```

4. Launch Jupyter Notebook

```bash
python -m notebook
```

5. Open the Notebook

  Open:
  
  ```txt
  notebooks/ethereum_fraud_detection.ipynb
  ```
  
  and run the cells sequentially.

---

## Dataset

Dataset used:
- Ethereum Fraud Detection Dataset (Kaggle)
> The Kaggle dataset is downloaded from https://www.kaggle.com/datasets/vagifa/ethereum-frauddetection-dataset and can be found in `./data/transaction_dataset.csv`

The dataset contains approximately 9800 Ethereum wallet records with fraud and non-fraud labels.

Each row represents a wallet/account and contains aggregated blockchain statistics such as:
- transaction counts
- Ether transfer values
- ERC20 activity
- wallet interaction behavior
- transaction timing features

---

## Data Analysis

The project began with exploratory data analysis (EDA) to better understand wallet behavior and fraud-related transaction patterns.

The analysis included:
- normal vs fraud wallet distribution
- transaction count distributions
- skewed blockchain activity visualization
- feature correlation analysis
- ERC20 behavioral analysis
- violin plots and boxplots for normal vs fraud wallet comparison

---

## Machine Learning Workflow

1. Data loading and cleaning
2. Exploratory Data Analysis
3. Behavioral analysis of wallet activity
4. Correlation analysis with fraud labels
5. Data preprocessing and feature scaling
6. Train-test split
7. Model training
8. Model evaluation
9. Feature importance analysis

---

## Machine Learning Models

The following supervised machine learning models were trained and evaluated:

### Logistic Regression

Used as the baseline model for fraud classification.

### Random Forest

Used to capture nonlinear behavioral relationships between Ethereum wallet features.

### XGBoost

Used as the final boosting model.

---

## Model Evaluation

Models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

| Model | Accuracy | Precision | **Recall** | F1-Score | ROC-AUC |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Logistic Regression | 0.9334 | 0.8657 | **0.8279** | 0.8464 | 0.9405 |
| Random Forest | 0.9903 | 1.0000 | **0.9564** | 0.9777 | 0.9992 |
| XGBoost | 0.9964 | 1.0000 | **0.9839** | 0.9919 | 0.9986 |

---

# Technologies Used

Python | Pandas | NumPy | Matplotlib | Seaborn | Scikit-learn | XGBoost | Jupyter Notebook

---

# Repository Structure

```bash
Ethereum-Fraud-Detection/
│
├── data/
│   └──transaction_dataset.csv
│   └──transaction_dataset.zip
├── notebooks/
│   └── ethereum_fraud_detection.ipynb
│
├── reports/
│   └── Report_PDF.pdf
│   └── Report_HTML.html
│
├── requirements.txt
│
└── README.md
```

---

# Future Improvements

Possible future extensions for the project:
- 5-Fold Cross Validation
- Ensemble stacking and bagging
- External dataset validation
- Additional blockchain behavioral features

---

# Conclusion

This project explored Ethereum wallet fraud detection using behavioral transaction analysis and machine learning.

The project demonstrated that:
- fraudulent wallets exhibit distinct behavioral patterns
- ERC20 activity contains important fraud-related signals
- ensemble models are highly effective for blockchain fraud detection tasks

The workflow also showed the importance of combining:
- exploratory data analysis
- behavioral interpretation
- machine learning
- feature importance analysis

to better understand fraud behavior on blockchain networks.
