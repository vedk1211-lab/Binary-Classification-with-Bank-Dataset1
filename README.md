🏦 Binary Classification with a Bank Dataset

Kaggle Playground Series 2025

This repository contains my solution to the Kaggle Playground Series 2025 – Binary Classification with a Bank Dataset competition.

The objective is to predict whether a client will subscribe to a bank term deposit using machine learning models.
---
📌 Competition Overview

Host: Kaggle

Competition: Binary Classification with a Bank Dataset – Clone

Start Date: October 13, 2025

Final Submission Deadline: October 12, 2026

Evaluation Metric: ROC-AUC

Type: Binary Classification

The dataset is synthetically generated based on real-world banking marketing data. The goal is to build models that can accurately predict customer subscription behavior.
---
🎯 Problem Statement

Given customer-related features such as demographic, financial, and campaign information, predict the probability that a client will subscribe to a bank term deposit.

Target variable:

y → Binary (0 = No, 1 = Yes)

Submissions must contain predicted probabilities for each test id.
---
📂 Dataset Structure

train.csv → Training dataset (features + target y)

test.csv → Test dataset (features only)

sample_submission.csv → Submission format

Submission format:

id,y
750000,0.5
750001,0.5
750002,0.5
---
⚙️ Approach
1️⃣ Data Preprocessing

Handled missing values (if any)

Encoded categorical variables

Stratified K-Fold cross-validation

Feature engineering (if applied)

2️⃣ Model Used

LightGBM Classifier

Early stopping to prevent overfitting

Stratified 5-Fold Cross Validation

3️⃣ Evaluation

Metric: ROC-AUC

Cross-validation AUC used to estimate leaderboard performance
---
🧠 Why ROC-AUC?

ROC-AUC measures the model’s ability to distinguish between the two classes across different classification thresholds. Since the competition requires probability predictions, ROC-AUC is the most appropriate metric.
---
🚀 How to Run
On Kaggle Notebook
train = pd.read_csv("/kaggle/input/binary-classification-with-a-bank-dataset-clone/train.csv")
test = pd.read_csv("/kaggle/input/binary-classification-with-a-bank-dataset-clone/test.csv")


Train the model and generate:

submission.to_csv("submission.csv", index=False)


Then download from the Output section and submit to Kaggle.
---
📊 Model Improvements (Future Work)

Hyperparameter tuning (Optuna / GridSearch)

Feature interaction engineering

CatBoost implementation

Model ensembling / stacking

SHAP explainability analysis
---
🏁 Results

Cross-validation ROC-AUC: [Add your score here]

Kaggle Public Leaderboard Score: [Add score]
---
📚 References

F.A. Nina. Binary Classification with a Bank Dataset – Clone.
Kaggle, 2025.
https://kaggle.com/competitions/binary-classification-with-a-bank-dataset-clone
---
Link 

https://www.kaggle.com/code/vedantkulka12/notebooka5b00cf664
