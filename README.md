# Diabetes Risk Factors Analysis & Prediction

**Project by: Group 15** **Course:** Statistical Data Processing  
**Date:** December 18, 2024

## 1. Project Overview
This project focuses on analyzing health survey data to identify key risk factors associated with diabetes and building a predictive model to assess an individual's probability of developing the disease based on their health metrics and lifestyle choices.

**Key Objectives:**
1.  **Exploratory Data Analysis (EDA):** Investigate relationships between diabetes and variables such as Blood Pressure, Cholesterol, BMI, Age, and Income.
2.  **Statistical Testing:** Utilize Chi-square tests and ANOVA to validate the statistical significance of these relationships.
3.  **Predictive Modeling:** Develop a Logistic Regression model to predict diabetes risk.

## 2. Dataset Description
The analysis uses the **Diabetes Health Indicators Dataset** (sourced from BRFSS 2015), containing key features:

| Variable | Description |
| :--- | :--- |
| **Diabetes_012** | **Target Variable**: 0 (No Diabetes), 1 (Pre-diabetes), 2 (Diabetes). |
| **HighBP** | High Blood Pressure (0: No, 1: Yes). |
| **HighChol** | High Cholesterol (0: No, 1: Yes). |
| **BMI** | Body Mass Index. |
| **Smoker** | Have you smoked at least 100 cigarettes in your entire life? |
| **Stroke** | History of stroke. |
| **HeartDiseaseorAttack** | History of coronary heart disease or myocardial infarction. |
| **PhysActivity** | Physical activity in past 30 days. |
| **Fruits / Veggies** | Consumption of fruits and vegetables. |
| **HvyAlcoholConsump** | Heavy alcohol consumption. |
| **GenHlth** | General health rating (1: Excellent - 5: Poor). |
| **Age** | Age category (13 levels, higher value indicates older age). |
| **Income** | Income level. |

## 3. Methodology
The project was implemented using **R Language** with the following statistical techniques:

1.  **Data Cleaning:** Preprocessing data and converting variables to appropriate factor types.
2.  **Hypothesis Testing:**
    * **Chi-square Test:** Examined the association between categorical variables (e.g., Age, HighBP, Sex) and Diabetes. Results indicated significant dependencies ($p < 0.05$).
    * **ANOVA:** Analyzed the difference in mean *BMI* across diabetes groups. Results showed that diabetic individuals have a significantly higher mean BMI (~31.9) compared to non-diabetic individuals (~28.0).
3.  **Modeling:**
    * **Logistic Regression:** Built to predict the probability of diabetes.
    * **Data Balancing:** Applied **SMOTE** to handle class imbalance.
    * **Feature Selection:** Utilized Stepwise or Lasso methods to select the most relevant predictors.

## 4. Key Findings & Insights
Based on the statistical analysis and model results:

* **Blood Pressure & Cholesterol:** These are the top risk factors. Individuals with high blood pressure are approximately **1.93 times** more likely to have diabetes.
* **BMI:** A higher BMI is strongly positively correlated with diabetes risk.
* **Age:** The risk increases progressively with age, especially in the 50+ age groups (categories 10-13).
* **Socioeconomic Status (Income/Education):** There is an inverse relationship; higher income and education levels are associated with a lower risk of diabetes (likely due to better access to healthcare and nutrition).
* **Unexpected Finding:** *Heavy Alcohol Consumption* showed a negative coefficient in this dataset. However, the team noted this might be due to sample bias or confounding factors and does not imply a health benefit.

## 5. Model Performance
* **AUC (Area Under the Curve):** Achieved approximately **0.8058**.
* The model demonstrates good capability in distinguishing between individuals at risk and those not at risk.
