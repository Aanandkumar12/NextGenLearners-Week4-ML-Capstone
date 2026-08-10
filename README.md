# NextGenLearners-Week4-ML-Capstone
NextGenLearners Week 4 ML Capstone — Data preprocessing, feature engineering, Logistic Regression, and model evaluation.
## 📌 Project Overview

This project is the Week 4 Machine Learning Capstone for the NextGenLearners Data Science Internship.

The project explores whether applicant information can be used to predict internship selection outcomes using a Logistic Regression classification model.

The workflow includes data preparation, feature engineering, categorical encoding, model training, evaluation, and interpretation.

## 🎯 Objectives

- Prepare applicant data for machine learning
- Create simulated applicant features
- Create a binary selection target
- Encode categorical features
- Split the data into training and testing sets
- Train a Logistic Regression model
- Evaluate model performance
- Interpret model coefficients
- Discuss model limitations and responsible use

## 📊 Dataset

The original dataset contains **250 applicant records** and **7 columns**:

- Student Name
- Email
- Phone
- Program Applied
- College
- Application Date
- Admission Status

Only applicants with confirmed admission outcomes were used for model training.

### Target Definition

| Admission Status | Target |
|---|---:|
| Accepted | 1 |
| Rejected | 0 |
| Pending | Excluded |

Pending applications were excluded because their final outcome was not confirmed.

## 🧩 Simulated Features

Four additional features were created for this machine learning exercise:

- `num_skills_listed`
- `has_portfolio`
- `prior_hackathon_participation`
- `statement_quality_score`

These features were simulated because they were not available in the original dataset.

A random seed of `42` was used to make the generated data reproducible.

## ⚙️ Feature Preparation

The following preprocessing steps were performed:

- Normalized admission status values
- Converted Yes/No features into 1/0
- Applied one-hot encoding to `Program Applied`
- Excluded personal identifier fields such as Name, Email, and Phone from model features

## 🤖 Machine Learning Model

### Model Used

**Logistic Regression**

### Train/Test Split

The confirmed applicant data was divided into:

- **80% Training Data**
- **20% Testing Data**

`random_state=42` was used for reproducibility.

## 📈 Model Performance

The Logistic Regression model achieved the following results on the test dataset:

| Metric | Result |
|---|---:|
| Accuracy | 50.00% |
| Precision | 58.33% |
| Recall | 38.89% |

A confusion matrix was also generated to evaluate correct and incorrect predictions.

## 🔍 Feature Coefficients

The Logistic Regression coefficients were analyzed to understand the features associated with the model's predictions.

Positive coefficients indicate a positive association with the predicted selection outcome, while negative coefficients indicate a negative association.

Because some features were simulated and the dataset is relatively small, these coefficients should be interpreted cautiously.

## ⚠️ Model Limitations

Several limitations should be considered:

- The dataset is relatively small.
- Four features were simulated rather than collected from real applicant records.
- Simulated features may not accurately represent real applicant behavior.
- Program names contain inconsistent capitalization.
- The model does not include many potentially important real-world applicant characteristics.
- The test dataset is small, so performance metrics may vary with different samples.
- Model associations should not be interpreted as proof of causation.

Therefore, this model should be considered an **educational and exploratory analysis**, not a production-ready applicant selection system.

## 💡 Executive Summary

This project explored whether applicant information could be used to estimate internship selection outcomes.

The analysis used applicant program information together with skills, portfolio availability, previous hackathon participation, and statement quality. Some of these additional characteristics were simulated because they were not available in the original dataset.

A Logistic Regression model was trained using applicants with confirmed outcomes. The model achieved **50.00% accuracy, 58.33% precision, and 38.89% recall** on the test data.

The results indicate that the current model is not reliable enough to automatically make internship selection decisions.

A larger dataset containing genuine applicant information and historical selection outcomes would be required for a more reliable model.

Machine learning should therefore be used as a **decision-support tool**, while final internship selection decisions remain under appropriate human review.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook / Google Colab
- GitHub

## 📁 Project Structure
NextGenLearners-Week4-ML-Capstone/
│
├── Week4_Capstone_Aanand_Kumar.ipynb
├── applicants.csv
└── README.md
