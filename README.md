# telco-churn-prediction
Predicting customer churn using machine learning with Python.
Telco Customer Churn Prediction
Project Overview
This project focuses on analyzing the Telco Customer Churn dataset to identify key factors that lead to customer churn. The primary goal is to build and evaluate machine learning models that can predict whether a customer will churn or not. The project involves two main stages: a comprehensive Exploratory Data Analysis (EDA) and the development of predictive models.

Dataset
The dataset used is the Telco Customer Churn dataset, which contains information about a fictional telco company's customers. It includes customer demographics, account information, and services they have signed up for.

Source: Kaggle - Telco Customer Churn

Project Structure
telco-churn-prediction/
│
├── WA_Fn-UseC_-Telco-Customer-Churn.csv    # The raw dataset
├── Telco_Churn_Analysis.ipynb              # Jupyter Notebook with all the code and analysis
├── churn_by_contract.png                   # Visualization of churn vs. contract type
├── tenure_distribution.png                 # Visualization of churn vs. customer tenure
└── README.md                               # This file
Installation and Setup
To run this project, you need Python 3 and the following libraries. You can install them using pip.

Clone the repository:

Bash

git clone https://github.com/Saima786/telco-churn-prediction.git
cd telco-churn-prediction
Install the required libraries:

Bash

pip install pandas numpy matplotlib seaborn scikit-learn jupyterlab
Methodology
The project follows a standard data science workflow:

1. Data Cleaning & Exploratory Data Analysis (EDA)
Data Loading: The dataset was loaded into a pandas DataFrame.

Initial Inspection: Checked for shape, data types, and missing values.

Data Cleaning: The TotalCharges column was converted from an object to a numeric type. The 11 missing values created during this conversion were filled with the median value.

Visualization & Insights: Key relationships were visualized to understand the drivers of churn.

Customers with month-to-month contracts are significantly more likely to churn.

Newer customers (with low tenure) have a higher churn rate.

Customers using Fiber optic internet service show a higher churn rate.

2. Model Building & Evaluation
Feature Engineering: The customerID was dropped. Categorical features were one-hot encoded, and numerical features were scaled using StandardScaler.

Data Splitting: The dataset was split into training (80%) and testing (20%) sets.

Model Training: Two different classification models were trained:

Logistic Regression

Random Forest Classifier

Evaluation: The models were evaluated using Accuracy, Precision, Recall, and F1-Score.

Results
The performance of the two models on the test set is summarized below.

Model Performance
Model	Accuracy	Precision (Churn)	Recall (Churn)	F1-Score (Churn)
Logistic Regression	81.6%	0.68	0.58	0.62
Random Forest	79.1%	0.63	0.49	0.55

Export to Sheets
Key Visualizations
Churn Rate by Contract Type

Distribution of Customer Tenure

Conclusion
Both models performed well, but the Logistic Regression model is recommended for this business problem. While its accuracy is only slightly higher, it achieved a significantly better Recall score (0.58) for the churn class. In a churn prediction scenario, correctly identifying customers who are likely to churn (high recall) is often more important than being precise, as it allows the company to take proactive retention measures.

How to Run the Code
Ensure all the required libraries are installed.

Launch Jupyter Notebook or JupyterLab:

Bash

jupyter lab
Open the Telco_Churn_Analysis.ipynb file and run the cells sequentially.
