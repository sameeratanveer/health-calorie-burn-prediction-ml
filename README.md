# 🏃‍♂️ Calorie Burnt Prediction

![Project Status](https://img.shields.io/badge/Status-Completed-brightgreen)  
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)  
![Machine Learning](https://img.shields.io/badge/Technique-Machine%20Learning-orange)  

## Overview
This project focuses on building a machine learning model that predicts the number of **calories burnt** based on a person's physical attributes and exercise session details.  
It is especially useful for healthcare applications like **fitness apps** or **personalized workout plans**.

---

## 📅 Dataset Information

The project uses **two datasets** that were **merged** on the `User_ID` column to form the final working dataset.

| Feature        | Description                      |
| -------------- | -------------------------------- |
| User_ID        | Unique Identifier for each user  |
| Gender         | Male / Female                    |
| Age            | Age of the user                  |
| Height         | Height in centimeters            |
| Weight         | Weight in kilograms              |
| Duration       | Exercise Duration (minutes)      |
| Heart_Rate     | Average Heart Rate during exercise |
| Body_Temp      | Body Temperature in Celsius      |
| Calories       | Target Variable - Calories burnt |

### Dataset Shape
- **Rows:** 15000
- **Columns:** 9

### Data Cleaning
- No missing values ✅
- No duplicate entries ✅

---

## 🔍 Exploratory Data Analysis (EDA)

- **Encoding:** Gender column encoded into numerical format (`Gender_male`).
- **Feature Engineering:**
  - **Age Groups** were created:
    - 0-18 ➔ 0 (Child/Teen)
    - 19-30 ➔ 1 (Young Adult)
    - 31-50 ➔ 2 (Adult)
    - 51-100 ➔ 3 (Senior)
  - **BMI** (Body Mass Index) was calculated from `Height` and `Weight`.

- **Correlation Analysis:**
  - High correlation observed between:
    - Height and Weight
    - Age and Age Group

---

## 🧠 Model Building

Three models were trained and evaluated:

| Model                    | MAE (Mean Absolute Error) | MSE (Mean Squared Error) | R² Score |
| ------------------------- | ------------------------- | ------------------------ | -------- |
| Linear Regression         | 8.66                      | 143.57                   | 0.964    |
| Decision Tree Regressor   | 4.92                      | 59.44                    | 0.985    |
| Random Forest Regressor   | 4.86                      | 57.75                    | 0.9857   |

### Best Model
- **Random Forest Regressor** performed the best with:
  - **Lowest MAE and MSE**
  - **Highest R² Score (0.9857)**

---

## Technologies Used

- Python 🐍
- Pandas
- Numpy
- Scikit-Learn
- Matplotlib / Seaborn (for EDA)

---

