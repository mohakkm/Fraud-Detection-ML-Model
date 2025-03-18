 Fraud Detection Using Random Forest

🔍 Overview

Fraud detection in financial transactions is challenging due to highly imbalanced datasets. This project implements a Random Forest Classifier with Borderline-SMOTE (to generate synthetic fraud cases) and Random Undersampling (to balance legitimate transactions). The model effectively distinguishes between fraudulent and legitimate transactions using optimized hyperparameters and resampling techniques.

📊 Dataset Details

The dataset consists of anonymized credit card transactions with:

0 (Legitimate Transactions): Majority of cases.

1 (Fraudulent Transactions): Highly underrepresented.

Features are mainly transformed via PCA, except Amount (standardized) and Time (removed).

⚙️ Data Processing & Balancing

Duplicate records are removed, and data is split (75% training, 25% testing). Since fraudulent transactions are rare, a combination of Borderline-SMOTE (generates synthetic fraud samples) and Random Undersampling (reduces majority class) ensures better balance without excessive data loss.

🏗️ Model Training & Optimization

The Random Forest Classifier is trained with class_weight='balanced' to assign higher importance to fraud cases. GridSearchCV is used for tuning hyperparameters like:

n_estimators (number of trees)

max_depth (tree depth)

min_samples_split (splitting threshold)

📈 Performance & Evaluation

The model is assessed using:

AUC-ROC Score (~0.98) – Measures fraud detection capability.

Precision-Recall Curve – Ensures minimal false positives while maximizing fraud detection.

GitHub: mohakkm

Email: mohakkmalvankar1104@gmail.com
