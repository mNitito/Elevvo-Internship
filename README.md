# 🎯 Task 1 — Student Exam Score Prediction

## 📌 Overview
This project is part of my **Elevvo Internship**, focusing on predicting students' exam scores based on various academic, personal, and support-related factors.  
The goal was to experiment with **different feature sets** and **machine learning models** to find the most accurate prediction approach.

---

## 📊 Dataset
The dataset contains features such as:

- `Hours_Studied`
- `Attendance`
- `Sleep_Hours`
- `Parental_Involvement`
- `Tutoring_Sessions`
- `Teacher_Quality`
- `Previous_Scores`
- `Motivation_Level`
- Encoded categorical variables: `High`, `Medium`, `Low`

**Target:** `Exam_Score`

---

## 🧪 Phases & Experiments

### **Phase 1 — Simple Model**
- **Features:** `Hours_Studied`
- **Model:** Linear Regression
- **Results:**
  - MSE: `~15.74`
  - R²: `~0.23`
- **Observation:** One feature alone cannot explain the score variation.

---

### **Phase 2 — Adding Original Features**
- **Features:** `Hours_Studied`, `Attendance`, `Sleep_Hours`
- **Model:** Linear Regression
- **Results:**
  - MSE: `~9.58`
  - R²: `~0.52`
- **Observation:** Performance improved by adding related features.

---

### **Phase 3 — All Available Features**
- **Preprocessing:** Encoded categorical variables
- **Features:** All dataset columns
- **Models Tested:**
  - **Linear Regression**
    - MSE: `4.05`
    - R²: `0.71`
  - **Polynomial Regression (degree 2)**
    - MSE: `4.23`
    - R²: `0.70`
- **Observation:** Linear Regression with all features gave the best results.

---

### **Phase 4 — Feature Engineering**
Created new features:
1. **Study_Efficiency** = `Hours_Studied / Sleep_Hours`
2. **Total_Support** = `Parental_Involvement + Tutoring_Sessions + Teacher_Quality`
3. **Academic_Preparedness** = Average of `Previous_Scores` + `Motivation_Level`

- **Results:**
  - MSE: `~4.40`
  - R²: `~0.69`
- **Observation:** Did not outperform all-features approach.

---

### **✅ Final Choice**
- **Best Model:** Linear Regression (all features)
- **Final Performance:**
  - MSE: `4.05`
  - R²: `0.71`
- **Reasoning:** Best balance of accuracy and simplicity.

---

## 📈 Conclusion
- All features gave the best accuracy.
- Polynomial regression and custom features did not improve results.
- Shows the importance of **systematic experimentation** in ML.

---

## 📂 Repository Structure
