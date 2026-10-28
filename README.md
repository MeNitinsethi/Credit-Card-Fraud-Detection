# Credit Card Fraud Detection Using Machine Learning

A machine learning project to identify potentially fraudulent credit card transactions using imbalanced classification, model evaluation, and decision-threshold analysis.

## Project Overview

Credit card fraud detection is a challenging classification problem because fraudulent transactions represent only a very small proportion of all transactions. A model that predicts every transaction as legitimate could achieve high accuracy while failing to detect fraud.

This project investigates how machine learning can help identify suspicious transactions while balancing fraud detection against false alarms.

## Objectives

- Explore and validate the transaction dataset.
- Understand class imbalance and feature distributions.
- Establish a baseline classification model.
- Train and compare machine learning models.
- Evaluate precision, recall, F1-score, and precision-recall AUC.
- Analyze confusion matrices and decision thresholds.
- Document limitations and opportunities for improvement.

## Dataset

**Source:** [Credit Card Fraud Detection — Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data)

The dataset contains European cardholder transactions from September 2013 over a two-day period.

- **Transactions:** 284,807
- **Fraudulent transactions:** 492
- **Features:** 30, including anonymized principal components, transaction time, and transaction amount
- **Target:** `Class` — 1 indicates fraud; 0 indicates a legitimate transaction

The dataset is highly imbalanced. Download it from Kaggle and place `creditcard.csv` where the notebook's data-loading instructions expect it.

The raw dataset is not included in this repository.

## Methodology

1. **Data validation:** Check columns, data types, missing values, duplicates, and class distribution.
2. **Exploratory analysis:** Examine transaction amounts, feature distributions, and class imbalance.
3. **Data preparation:** Split data into training, validation, and test sets before fitting preprocessing steps.
4. **Baseline model:** Establish a reference point for comparison.
5. **Model training:** Train and compare classification models.
6. **Threshold selection:** Choose a decision threshold using validation data, not the final test set.
7. **Evaluation:** Assess precision, recall, F1-score, precision-recall AUC, and the confusion matrix.
8. **Interpretation:** Discuss false positives, missed fraud, and potential operational trade-offs.

## Evaluation Metrics

- **Precision:** What proportion of flagged transactions are actually fraudulent?
- **Recall:** What proportion of fraudulent transactions are detected?
- **F1-score:** A combined measure of precision and recall.
- **Precision-recall AUC:** How well the model distinguishes fraud across different decision thresholds.
- **Confusion matrix:** Shows correctly and incorrectly classified transactions.

Accuracy will not be used as the sole measure of success.

## Repository Structure

```text
credit-card-fraud-detection/
├── README.md
├── credit_card_fraud_detection.ipynb
├── requirements.txt
├── .gitignore
├── LICENSE
└── reports/
    └── figures/
```

## Getting Started

### Requirements

- Python 3.10 or a compatible Python environment
- Jupyter Notebook or Google Colab
- pandas, numpy, scikit-learn, matplotlib, and seaborn

### Run in Google Colab

1. Open the notebook in this repository.
2. Download the dataset from Kaggle.
3. Upload `creditcard.csv` when prompted by the notebook.
4. Run the cells in order.
5. Review the generated evaluation metrics and visualizations.

## Results

**Status:** Initial implementation.

Model performance results will be added after the complete notebook has been executed and evaluated. No performance claims are made until the results have been verified.

| Metric | Result |
|---|---|
| Precision | Pending evaluation |
| Recall | Pending evaluation |
| F1-score | Pending evaluation |
| Precision-recall AUC | Pending evaluation |

## Model Evaluation Results

The model was evaluated on a held-out test set containing 56,962 transactions, including 99 fraudulent transactions.

| Metric | Legitimate | Fraud |
|---|---:|---:|
| Precision | 1.00 | 0.89 |
| Recall | 1.00 | 0.79 |
| F1-score | 1.00 | 0.83 |
| Support | 56,863 | 99 |

**Overall accuracy:** 1.00 (rounded to two decimal places)

### Key Findings

- The model achieved a fraud precision of 0.89.
- Fraud recall was 0.79, indicating that some fraudulent transactions were missed.
- The fraud F1-score was 0.83.
- Accuracy alone is insufficient for evaluating this highly imbalanced classification problem.

### Limitations and Next Steps

- Review the confusion matrix to quantify false positives and missed fraud cases.
- Evaluate precision-recall AUC and compare against a baseline model.
- Investigate alternative decision thresholds using validation data.
- Assess whether the model's performance remains stable across different transaction samples.

These results are specific to the evaluated test set and do not establish real-world fraud detection performance.

## Limitations

- The dataset represents a short historical period and may not reflect current fraud patterns.
- Most input features are anonymized, limiting direct business interpretation.
- Model performance may change when transaction distributions change.
- The appropriate decision threshold depends on fraud losses, investigation costs, and customer impact.
- This project is an educational demonstration, not a production fraud detection system.

## Future Improvements

- Compare additional classification algorithms.
- Calibrate predicted probabilities.
- Evaluate models under different false-positive constraints.
- Add a simple interactive demonstration.
- Implement automated tests and a reproducible training pipeline.
- Explore model monitoring and data drift detection.

## Disclaimer

This project is for educational and portfolio purposes only. It should not be used to make real-world financial decisions without further validation, security controls, and appropriate operational review.

## Author

Unwrapping_AI

More projects will be added to the portfolio as they are completed and evaluated.
