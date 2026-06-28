# 🩺 Diabetes Prediction using Logistic Regression

## 📌 Project Overview

This project aims to predict whether a patient is diabetic based on various health-related attributes using **Logistic Regression**. The complete machine learning workflow was followed, starting from data exploration to model evaluation and prediction on unseen data.

The project emphasizes not only model performance but also **business-oriented decision making**, where the final model was selected based on minimizing **False Negatives (Type II Errors)** rather than simply achieving the highest accuracy.

---

## 🎯 Problem Statement

Early detection of diabetes is important for timely medical intervention. The objective of this project is to build a machine learning classification model that can predict whether a patient is diabetic based on clinical features.

---

## 📂 Dataset

**Source:** Kaggle - Diabetes Dataset

The dataset contains the following features:

- Pregnancies
- Glucose
- Blood Pressure
- Skin Thickness
- Insulin
- BMI
- Diabetes Pedigree Function
- Age

**Target Variable**

- Outcome
  - 0 → Non-Diabetic
  - 1 → Diabetic

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## 📊 Exploratory Data Analysis (EDA)

The following analyses were performed:

- Data inspection (`head()`, `tail()`, `info()`, `describe()`)
- Missing value analysis
- Duplicate value check
- Target class distribution
- Histogram analysis
- Box plot analysis for outlier detection
- Correlation heatmap
- Multicollinearity assessment

### Key Findings

- No duplicate records were found.
- Some numerical features showed right-skewed distributions.
- Outliers were observed mainly in the **Age** and **Diabetes Pedigree Function** features and were retained as they appeared to be genuine observations.
- No strong multicollinearity was observed among the independent variables.

---

## ⚙️ Data Preprocessing

The following preprocessing steps were performed:

- Feature and target separation
- Train-Test Split
- Feature Scaling using StandardScaler

---

## 🤖 Model Building

Three Logistic Regression models were developed and compared:

1. Baseline Logistic Regression
2. Logistic Regression with `class_weight='balanced'`
3. Hyperparameter-Tuned Logistic Regression using GridSearchCV

---

## 📈 Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- ROC Curve
- ROC-AUC Score
- Stratified K-Fold Cross Validation

---

## 🎯 Business-Oriented Model Selection

Instead of selecting the model based only on accuracy, the final model was selected based on the business objective.

For diabetes prediction, **False Negatives (Type II Errors)** are more critical because failing to identify a diabetic patient may delay diagnosis and treatment, potentially leading to serious health complications.

Therefore, **Recall** was considered the primary evaluation metric.

The Hyperparameter-Tuned Logistic Regression model achieved the highest Recall while maintaining good overall performance and was selected as the final model.

---

## 🔮 Prediction on Unseen Data

The selected model was tested on new unseen patient records.

The model successfully predicted the diabetes status and also estimated the probability of diabetes for each patient, demonstrating its ability to generalize to new data.

---

## 📁 Project Structure

```
Diabetes-Prediction-Logistic-Regression/
│
├── Diabetes_Prediction.ipynb
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
└── images/
```

---

## 🚀 Future Improvements

- Compare Logistic Regression with Decision Tree and Random Forest.
- Perform Feature Engineering.
- Build a Machine Learning Pipeline.
- Deploy the model using Streamlit or Flask.
- Evaluate additional classification algorithms.

---

## 👨‍💻 Author

**Dharani Kaligi**

- Data Engineer at DXC Technology
- Aspiring Data Scientist
- Skilled in Python, SQL, Machine Learning, ETL, and Power BI

---

## ⭐ If you found this project useful, feel free to star the repository.
