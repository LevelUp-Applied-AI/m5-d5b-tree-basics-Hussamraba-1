# Core Skills Drill 5B — Tree-Based Model Basics

Module 5 Week B drill for AI.SPIRE Applied AI & ML Systems.



##  Overview

In this drill, I worked on implementing basic tree-based models using scikit-learn. The goal was to practice training a Decision Tree, understanding feature importance, and using a Random Forest model with class imbalance handling.

---

 Setup

```bash
pip install -r requirements.txt
```

---

## Tasks

The main work was done in `drill.py`, where I completed the following functions:

### 1. `train_decision_tree`

Trained a `DecisionTreeClassifier`
Used `max_depth=5` to control overfitting
Fit the model on training data and returned the trained model

---

### 2. `get_feature_importances`

 Extracted feature importance values using `feature_importances_`
 Mapped each feature name to its importance
 Sorted the results in descending order to identify the most influential features

---

### 3. `train_balanced_forest`

 Trained a `RandomForestClassifier` with:

   `n_estimators=100`
   `class_weight='balanced'` to handle class imbalance
 Generated predictions on test data
 Evaluated the model using:

  Precision
  Recall
  F1 Score

---

##  Results

 The Decision Tree model was successfully trained with controlled depth.
 Feature importance showed that variables like `total_charges`, `tenure`, and `contract_months` had the highest impact on churn prediction.
 The Random Forest model achieved:

   Moderate recall (better detection of churn cases)
   Lower precision (more false positives)
 This trade-off is expected when handling imbalanced data.

---

##  What I Learned

 How Decision Trees work and how to prevent overfitting using `max_depth`
 How to interpret model behavior using feature importance
 The difference between a single tree and ensemble methods like Random Forest
 How class imbalance affects model predictions
 How `class_weight='balanced'` improves recall for minority classes
 Why precision, recall, and F1 score are more useful than accuracy in imbalanced datasets

---

##  How to Run

```bash
python drill.py
```

Expected output includes:

 Decision tree depth
 Top important features
 Random Forest evaluation metrics

---

##  Submission

1. Created a branch: `drill-5b-tree-basics`
2. Completed all required functions in `drill.py`
3. Opened a PR to `main`
4. Submitted PR link on TalentLMS

---

##  License

This repository is provided for educational use only. See [LICENSE](LICENSE) for terms.
