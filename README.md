# Churn Prediction

## Project Overview

This project aims to predict employee churn (attrition) using various features, such as satisfaction level, average monthly hours, work accident status, promotion in the last 5 years, and more. The goal is to build a machine learning model to identify employees at high risk of leaving the company, enabling HR departments to take proactive measures.

## Features

- **satisfaction_level**: Employee satisfaction on a scale from 0 to 1.
- **last_evaluation**: Performance evaluation score of the employee.
- **number_project**: Number of projects the employee is involved in.
- **average_montly_hours**: Average number of working hours per month.
- **time_spend_company**: Number of years the employee has spent with the company.
- **work_accident**: Indicates whether the employee had a work accident (binary).
- **promotion_last_5years**: Indicates whether the employee was promoted in the last 5 years (binary).
- **department**: Department where the employee works.
- **salary**: Employee's salary level (Low, Medium, High).

## Methodology

- **Data Preprocessing**:
  - Cleaning duplicate entries.
  - Scaling numerical features using `StandardScaler`.
  - Label encoding for categorical features (`department` and `salary`).

- **Model**: 
  - Logistic Regression with **L2 regularization** was applied to predict employee churn.
  - Hyperparameter tuning was performed using GridSearchCV to select the best model.

- **Performance**: 
  - The model achieved an accuracy of 83.4% on the test set.

## Key Points from the EDA (Exploratory Data Analysis)

- **Promotion and Tenure**: People who have not been promoted in the last 5 years are more likely to leave the company. Additionally, employees with a tenure of up to 6 years are also more likely to leave.
  
- **Work Hours and Projects**: Employees who work longer hours on average and handle more projects are more likely to leave.
  
- **Satisfaction Levels**: A lower satisfaction level significantly increases the likelihood of leaving the company.
  
- **Work Accidents**: Work accidents do not appear to have much importance in predicting employee churn, as they do not strongly correlate with the target variable.

## Tools and Libraries Used

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn

## Conclusion

This project successfully built a machine learning model to predict employee churn, helping HR departments take necessary actions to retain talent.
