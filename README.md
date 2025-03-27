# Telco Data Churn Predictor & Dashboard 

A predictive data analytics project built using Python and Google Colab to analyze and predict customer churn behavior in the telecommunications industry. The project utilizes an Ensemble Tree Method to achieve a prediction accuracy of 80%. Additionally, a Power BI dashboard is developed to visualize key factors influencing churn, providing insights into customer behavior and retention strategies.

### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiZTM5OGE1OTMtYjRhYS00MjE5LTgxYmUtZTRmOGJmNTMyNTQ5IiwidCI6IjZmNDQzMmRjLTIwZDItNDQxZC1iMWRiLWFjMzM4MGJhNjMzZCIsImMiOjEwfQ%3D%3D
<p align="center">
  <img src="https://github.com/user-attachments/assets/7fe3384d-fe8a-41e3-b742-7a83f9a7a64b" alt="Dashboard" />
</p>

---

## Introduction 

This project consists of two key components designed to analyze and predict customer churn in the telecommunications industry, using a dataset that includes customer information and whether they have churned or not. This project will have divided into 2 sections

1. **Churn Predictor ML Model**: A machine learning model that predicts the likelihood of a customer leaving the service. By analyzing historical data, the model helps identify high-risk customers, using Ensemble tree method from Scikit learn

2. **Interactive Dashboard**: A visualization tool that allows users to explore key metrics and trends in the telco data. It includes various interactive charts and filters to analyze churn rates, customer demographics, service usage , and more.

Together, these tools offer a comprehensive solution for understanding and mitigating customer churn in the telecom industry.

---

## Tools & Technologies

- **Python**
- **Google Colab**
- **Machine Learning (Scikit-Learn)** (Ensemble Tree Method)
- **Power BI**

---

## Dataset   

This dataset contains information on telecommunications customers and whether they have churned (i.e., stopped using the service). The data includes demographic details, service usage patterns, and billing information, making it useful for customer retention analysis and predictive modeling.

---

## Setup & Usage for ML

1. Clone the repository.
   ```bash
   git clone https://github.com/Stellar-Cretaceus/Telco-Churn-Predictor
   cd telco-data-churn-predictor
   ```
2. Open the project in Google Colab.
3. Follow the steps in the Jupyter Notebook to:
    - Import and preprocess the dataset.
    - Train the model using the Ensemble Tree Method.
    - Evaluate the model's performance.
      
---

## Data Cleaning Approached

For data cleaning, we will use different approaches depending on the tool:   
1. For machine learning (ML): After handling null values, we will transform categorical (non-numeric) data by unpivoting them into separate boolean columns. This will help in building an ensemble tree based on multiple decision trees.
2. For Power BI: We will unpivot data formatted as True/False or True/False/No into multiple rows. This transformation will improve data connectivity and enhance visualization.


---

## Insights from ML and Dashboard
- Based on the tree.feature_importances_ of this model, we can see that the most important features in the ensemble tree are tenure, whether the customer uses fiber optic as their internet service, and the total charges. These are the top three features influencing the model. We can explore this dashboard further to verify that using fiber optic increases the likelihood of churn compared to other options, and that churned customers tend to have fewer tenure years than non-churned customers.
<p align="center">
  <img src="https://github.com/user-attachments/assets/c9ddd232-90a8-49c0-b42e-28b4a823e6f5" alt="Feature Importance" />
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/90f09374-8ec6-4ce5-9d18-12ab2c7235ca" alt="Churn Highlighted Dashboard" />
</p>

- Customers with low tenure are more likely to churn. However, among long-tenured customers, those with high total charges have a higher tendency to churn. To address this, we could implement discount strategies for high-paying, long-tenured customers to bring their total charges closer to the average trend line, reducing the risk of churn.
- The churned group is mostly internet service users, particularly those using fiber optic and on month-to-month contracts. To improve retention, we could focus on encouraging longer contract commitments and offering Online Security services, as these may help reduce churn.
- Many churned customers have low total charges and short tenure, suggesting they tried the service but quickly changed their minds. To retain this group, we could introduce special contract offers or incentives that encourage them to stay longer.

