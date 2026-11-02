# 📱 Telecom Plan Recommendation | Machine Learning Classification

### Predicting the Most Suitable Mobile Plan Using Customer Behavior and Machine Learning

**Python • Pandas • Scikit-learn • Classification • Model Evaluation • Hyperparameter Tuning**

## 📌 Project Overview

Telecommunications companies need to understand customer behavior to recommend services that better match individual usage patterns.

This project develops a machine learning classification model for **Megaline**, a fictional telecommunications company, to recommend one of two mobile plans: **Smart** or **Ultra**.

Using customer behavior data, the project compares three classification algorithms and selects the model with the highest validation accuracy.

**Business Goal:** Build a predictive model capable of recommending a mobile plan based on customer usage patterns, achieving a minimum accuracy of 75%.

## 🎯 Project Objectives

- Analyze customer usage data.
- Verify data quality and completeness.
- Prepare features and the target variable.
- Split data into training, validation, and test sets.
- Train and compare different classification algorithms.
- Optimize model hyperparameters.
- Select the best-performing model.
- Evaluate its performance on unseen test data.

## 🛠️ Technologies Used

| Technology | Application |
|---|---|
| Python | Programming and data analysis |
| Pandas | Data loading and preparation |
| Scikit-learn | Machine learning and model evaluation |
| Jupyter Notebook | Experimentation and documentation |

## 📂 Dataset Description

The dataset, `users_behavior.csv`, contains **3,214 customer records** and five columns.

| Feature | Description |
|---|---|
| `calls` | Number of calls made |
| `minutes` | Total call duration in minutes |
| `messages` | Number of text messages sent |
| `mb_used` | Mobile internet usage in megabytes |
| `is_ultra` | Target variable indicating the customer's plan |

### Target Variable

- `0` — Smart plan
- `1` — Ultra plan

The dataset was already preprocessed and contained no missing values or duplicate rows.

## 🔄 Project Methodology

### 1. Data Preparation

The dataset was inspected to verify its structure, data types, missing values, and duplicate records.

The target variable `is_ultra` was separated from the four predictive features.

### 2. Train, Validation, and Test Split

The dataset was divided into:

| Dataset | Percentage |
|---|---:|
| Training | 60% |
| Validation | 20% |
| Testing | 20% |

A fixed random state (`12345`) was used to support reproducibility.

### 3. Model Training

Three classification algorithms were evaluated.

**Decision Tree Classifier**

Different maximum tree depths were tested to identify the configuration with the best validation accuracy.

**Random Forest Classifier**

Multiple combinations of tree counts and maximum depths were evaluated to improve predictive performance.

**Logistic Regression**

A logistic regression classifier was trained as an additional model for comparison.

## 📊 Model Performance

### Validation Results

| Model | Validation Accuracy |
|---|---:|
| Decision Tree | 78.54% |
| **Random Forest** | **80.87%** |
| Logistic Regression | 71.07% |

Random Forest achieved the highest validation accuracy.

### Best Hyperparameters

| Parameter | Value |
|---|---|
| Algorithm | Random Forest Classifier |
| `n_estimators` | 40 |
| `max_depth` | 8 |
| `random_state` | 12345 |

## 🧪 Final Model Evaluation

The selected Random Forest model was evaluated on the test dataset.

| Metric | Result |
|---|---:|
| Training accuracy | 87.50% |
| Validation accuracy | 80.87% |
| **Test accuracy** | **79.63%** |
| Minimum required accuracy | 75.00% |

### Interpretation

The final model achieved **79.63% test accuracy**, exceeding the project's minimum requirement of 75%.

The difference between training and test accuracy suggests some degree of overfitting may be present, although the model maintained performance above the required threshold on unseen data.

## 💡 Key Findings

- Customer behavior can be used to classify mobile plan preferences.
- Random Forest outperformed Decision Tree and Logistic Regression in the validation experiments.
- Hyperparameter tuning improved model selection.
- The final model met the required accuracy threshold.
- A separate test dataset provided an evaluation of performance on previously unseen records.

## ⚠️ Limitations and Future Improvements

The project evaluates predictive performance primarily through accuracy.

Future improvements could include:

- Evaluating precision, recall, F1-score, and confusion matrices.
- Comparing results against a simple baseline classifier.
- Using stratified data splitting and cross-validation.
- Exploring automated hyperparameter optimization.
- Analyzing feature importance.
- Investigating the business impact of incorrect recommendations.

## 🚀 How to Run the Project

1. Clone the repository.
2. Install the required Python libraries.
3. Download or place `users_behavior.csv` in the project data directory.
4. Update the CSV file path in the notebook.
5. Open the notebook in Jupyter Notebook or JupyterLab.
6. Run all cells sequentially.

### Install Dependencies

```bash
pip install pandas scikit-learn notebook
```

## 📈 Conclusion

This project demonstrates the practical application of supervised machine learning to a telecommunications business problem.

By comparing multiple classification algorithms and tuning their hyperparameters, a Random Forest model was selected and achieved **79.63% accuracy on the test set**.

The project highlights skills in data preparation, classification, model comparison, hyperparameter tuning, and predictive performance evaluation.

## 👩‍💻 Author

**Andressa Miranda**

Computer Science | Data Analytics | Python | Machine Learning

[GitHub Profile](https://github.com/Andressa202)

*Developed as part of the TripleTen Data Science program.*
