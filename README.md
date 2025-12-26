# 🎓 Student Performance Prediction using Machine Learning

## 📌 Project Overview
This project aims to predict students’ **overall academic performance** using demographic and behavioral features.  
An end-to-end **machine learning pipeline** was implemented using **scikit-learn**, focusing on correct preprocessing, model training, and evaluation while explicitly avoiding data leakage.

---

## 📊 Dataset Description
- **Total records:** 25,000 students  
- **Target variable:** `overall_score`  
- **Features include:**
  - Demographic: age, gender, school type, parental education
  - Behavioral: study hours, attendance percentage, study method, extra activities
  - Infrastructure: internet access, travel time  

> ⚠️ Columns such as `student_id` and `final_grade` were removed to prevent data leakage.

---

## 🛠️ Tools & Technologies
- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## 🧠 Methodology

### 1️⃣ Data Preparation
- Separated **features (X)** and **target (y)**
- Removed identifier and leakage-prone columns
- Performed **train-test split (80/20)**

### 2️⃣ Preprocessing Pipeline
Used `ColumnTransformer` with:
- **Numerical features:** `StandardScaler`
- **Categorical features:** `OneHotEncoder (handle_unknown='ignore')`

All preprocessing steps were combined with the model using **sklearn Pipelines** to ensure consistency and prevent data leakage.

### 3️⃣ Model Used
- **Linear Regression** (baseline regression model)

### 4️⃣ Model Evaluation
- RMSE (Root Mean Squared Error)
- R² Score
- Visual evaluation using prediction and residual plots

---

## 📈 Results
- **RMSE:** ~18.39  
- **R² Score:** ~0.95  

The model demonstrates strong predictive performance with realistic error after eliminating data leakage.

---

## 📊 Visualizations
- **Actual vs Predicted Scores Plot**
- **Residuals vs Predicted Values Plot**

These plots help assess prediction accuracy and error distribution.

---

## 🔍 Key Learnings
- Importance of removing data leakage (`final_grade`, `student_id`)
- Correct use of **Pipelines and ColumnTransformer**
- Clear separation of training and testing data
- Proper evaluation of regression models
- Building a clean and reproducible ML workflow

---

## 📂 Project Structure
