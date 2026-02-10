# 🚢 Titanic Survival Prediction – Data Preprocessing & Feature Scaling

## 📌 Project Overview
This project focuses on **data preprocessing and feature scaling** using the famous **Titanic dataset**.  
The goal is to prepare raw passenger data into a clean, machine-learning–ready format by handling missing values, encoding categorical features, detecting outliers, and applying feature scaling techniques.

This notebook is especially useful for **beginners in Machine Learning** to understand how real-world data is cleaned before model training.

---

## 📊 Dataset Description
The Titanic dataset contains passenger information such as:

- **Survived** – Survival status (Target variable)
- **Pclass** – Passenger class
- **Sex** – Gender of passenger
- **Age** – Age of passenger
- **SibSp** – Number of siblings/spouses aboard
- **Parch** – Number of parents/children aboard
- **Fare** – Ticket fare
- **Embarked** – Port of embarkation
- **Ticket, Cabin, Name** – Passenger identifiers

---

## 🧹 Data Cleaning Steps

### 1️⃣ Dropping Irrelevant Columns
Columns such as **Name, Ticket, and Cabin** are removed because:
- They do not contribute significantly to prediction
- They contain many missing values
- They are mostly identifiers rather than features

---

### 2️⃣ Handling Missing Values
- Rows with missing **Embarked** values are dropped
- Missing **Age** values are filled using the **mean age**
- This ensures no missing data remains in numerical features

---

## 📈 Outlier Detection
- A **Box Plot** is used to visually detect outliers in the **Age** feature
- Outliers are analyzed instead of blindly removed, as they may carry real-world meaning (e.g., infants or elderly passengers)

---

## 🔢 Feature Scaling

### 🔹 Why Feature Scaling?
Many Machine Learning algorithms are sensitive to the scale of data.  
Feature scaling ensures all numerical features contribute equally.

---

### 🔹 Standardization (Z-score Scaling)
Standardization transforms features so that:
- Mean = 0
- Standard Deviation = 1

**Formula:**
Z = (X - mean) / standard deviation



This method is especially useful for:
- Logistic Regression
- Support Vector Machines (SVM)
- K-Nearest Neighbors (KNN)
- Neural Networks

---

### 🔹 Numerical Features Scaled
- Age
- Fare
- SibSp
- Parch

Categorical features are excluded from scaling.

---
