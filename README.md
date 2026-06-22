# 🏥 Healthcare Insurance Cost Prediction using Linear Regression and Logistic Regression

## 📌 Project Overview

Healthcare insurance costs vary significantly based on several factors such as age, BMI, smoking habits, number of children, gender, and geographical region. Understanding these factors can help insurance companies estimate costs more accurately and identify high-risk individuals.

This project applies both **Linear Regression** and **Logistic Regression** on a healthcare insurance dataset to solve two different machine learning problems:

1. **Linear Regression** – Predict the exact insurance charges of an individual.
2. **Logistic Regression** – Classify individuals into Low-Risk or High-Risk categories.

The project demonstrates the complete Machine Learning workflow, including data preprocessing, exploratory data analysis (EDA), feature engineering, model training, evaluation, and result interpretation.

---

# 🎯 Objectives

* Analyze healthcare insurance data.
* Identify factors influencing insurance charges.
* Build a Linear Regression model to predict insurance costs.
* Build a Logistic Regression model to classify customer risk.
* Compare regression and classification approaches.
* Visualize relationships among features and target variables.

---

# 📂 Dataset Description

The dataset contains information about insurance beneficiaries.

| Feature  | Description            |
| -------- | ---------------------- |
| age      | Age of the individual  |
| sex      | Gender (Male/Female)   |
| bmi      | Body Mass Index        |
| children | Number of dependents   |
| smoker   | Smoking status         |
| region   | Residential region     |
| charges  | Medical insurance cost |

### Dataset Size

* Records: 1338
* Features: 7

---

# 🛠 Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn

---

# 🔄 Project Workflow

## Step 1: Data Collection

The healthcare insurance dataset was imported into Pandas DataFrame for analysis.

---

## Step 2: Data Understanding

Basic information was examined using:

* Shape of dataset
* Data types
* Statistical summary
* Missing value check

### Observation

* No missing values were found.
* Dataset was clean and ready for analysis.

---

## Step 3: Exploratory Data Analysis (EDA)

Several visualizations were created to understand the data.

### Age Distribution

Analyzed age patterns among insurance beneficiaries.

### BMI Distribution

Studied body mass index distribution.

### Charges Distribution

Examined insurance cost variations.

### Smoker vs Charges

Compared insurance charges between smokers and non-smokers.

### Gender vs Charges

Compared charges between males and females.

### Region Analysis

Investigated regional differences in insurance costs.

### Correlation Heatmap

Measured relationships among variables.

### Key Findings

* Smoking status has the strongest impact on insurance charges.
* Age shows a moderate positive relationship with charges.
* BMI contributes to increased insurance costs.
* Gender has relatively little effect on charges.

---

# 🔧 Data Preprocessing

### Categorical Encoding

The following categorical features were converted into numerical format:

* Sex
* Smoker
* Region

Using:

```python
pd.get_dummies()
```

This enabled machine learning models to process the data.

---

# 📈 Linear Regression Model

## Purpose

Predict the exact insurance charge amount.

### Input Features

* Age
* BMI
* Children
* Sex
* Smoker
* Region

### Target Variable

* Charges

### Train-Test Split

* Training Data: 80%
* Testing Data: 20%

### Model Used

```python
LinearRegression()
```

---

## Evaluation Metrics

The model was evaluated using:

* MAE (Mean Absolute Error)
* MSE (Mean Squared Error)
* RMSE (Root Mean Squared Error)
* R² Score

### Results

* MAE ≈ 4177
* RMSE ≈ 5956
* R² Score ≈ 0.81

### Interpretation

An R² score of approximately 0.81 indicates that the model explains around 81% of the variation in insurance charges.

The scatter plot of Actual vs Predicted values demonstrates a strong positive relationship, indicating good predictive performance.

---

# 📊 Logistic Regression Model

## Purpose

Classify customers into:

* Low Risk (0)
* High Risk (1)

### Risk Category Creation

The median insurance charge was used as a threshold:

```python
risk_category = charges > median_charge
```

### Model Used

```python
LogisticRegression()
```

---

## Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score
* Classification Report
* Confusion Matrix

### Results

* Accuracy ≈ 91%
* Precision ≈ 89%
* Recall ≈ 93%
* F1 Score ≈ 91%

### Interpretation

The Logistic Regression model successfully classified insurance customers into risk categories with high accuracy.

The confusion matrix shows a low number of misclassifications, indicating strong classification performance.

---

# ⚖️ Linear Regression vs Logistic Regression

| Feature         | Linear Regression | Logistic Regression             |
| --------------- | ----------------- | ------------------------------- |
| Problem Type    | Regression        | Classification                  |
| Output          | Continuous Value  | Class Label                     |
| Target Variable | Charges           | Risk Category                   |
| Prediction      | Exact Cost        | Low Risk / High Risk            |
| Evaluation      | MAE, RMSE, R²     | Accuracy, Precision, Recall, F1 |
| Use Case        | Cost Estimation   | Risk Prediction                 |

### Comparison Summary

Linear Regression is useful when the objective is to estimate the exact insurance charge amount.

Logistic Regression is useful when the objective is to classify customers into predefined risk categories.

Both models provide valuable insights for healthcare insurance companies and can be used together for better decision-making.

---

# 📌 Results Summary

### Linear Regression

✅ Successfully predicted insurance charges.

✅ Achieved approximately 81% explanatory power (R² Score).

### Logistic Regression

✅ Successfully classified customers into risk categories.

✅ Achieved approximately 91% classification accuracy.

---

# 🚀 Future Enhancements

* Implement Random Forest Regressor.
* Implement XGBoost Regressor.
* Perform Hyperparameter Tuning.
* Build a Web Application using Flask or Streamlit.
* Deploy the model on cloud platforms.
* Use larger real-world healthcare datasets.

---

# ✅ Conclusion

This project demonstrates the practical application of Machine Learning in the healthcare insurance domain.

Linear Regression was used to estimate insurance charges, while Logistic Regression was used to classify customer risk levels.

The results indicate that smoking status, age, and BMI significantly influence healthcare costs. Both models achieved strong performance and provide meaningful insights that can assist insurance providers in pricing strategies and risk assessment.

