# Mortgage Optimization with Machine Learning

## Project Overview

This project aims to optimize the mortgage lending process using machine learning to maximize profits while managing risk. The company in this scenario deals with mortgage loans and has a total of 25 billion rubles to lend within a year. By leveraging data on real estate and clients, the company seeks to prioritize loan issuance based on factors such as predicted real estate price and the likelihood of client debt.

## Problem Statement

The objective is to create a strategy that optimizes the company's profits by:

1. Prioritizing mortgage issuance based on client profiles using a machine learning model that predicts loan success and real estate prices.
2. Managing the risk of client defaults by incorporating the probability of a client going into debt in decision-making.

The company seeks to maximize profits by issuing loans to clients with the highest priority while staying within budget and mitigating default risks.

## Key Features

- **Mortgage Prioritization:** Loans are issued based on a priority column (`__priority`), which is generated using machine learning predictions. Clients with the highest priority values receive mortgages first until funds are depleted.
- **Price Prediction:** The model predicts the real estate value (`__price_predict`), and loans are issued only if the predicted price falls within 10% of the real estate's actual value.
- **Churn Prediction:** The model predicts the likelihood of a client defaulting on their mortgage (`__churn_prob`), helping the company avoid risky clients and minimize losses.
- **Profit Calculation:** Profits are based on the loan amount and default status of the client. Defaulted loans result in a loss, while successful loans generate a percentage profit of the mortgage amount.

## Workflow

1. **Data Collection:** The dataset consists of 59 features that capture key characteristics of the clients and the real estate.
2. **Model Training:** Two machine learning models were trained:
   - **Price Prediction Model:** Predicts the real cost of the property (`__price_predict`).
   - **Churn Prediction Model:** Predicts the probability that a client will go into debt (`__churn_prob`).
3. **Loan Prioritization:** Based on the model outputs, a new column (`__priority`) is generated, ranking clients by the priority for loan issuance.
4. **Decision-Making Algorithm:** Mortgages are issued to clients with the highest priority first, ensuring the predicted property price is within the allowable range and sufficient funds remain.

## Key Variables

- **__price_doc:** Actual price of the property (million rubles).
- **__churn:** Indicator of client default (1 = default, 0 = no default).
- **__price_predict:** Predicted price of the property (million rubles).
- **__churn_prob:** Probability of client default (0 to 1).
- **__priority:** Loan issuance priority (higher values get higher priority).

## Results

- Mortgages are only issued if the predicted price falls within ±10% of the actual property value.
- Profits are calculated as a percentage of the mortgage value, with losses occurring when clients default.
- The model ensures that only the most profitable and least risky loans are issued, maximizing the company's profit potential.

## Technologies Used

- Python
- Machine Learning (sklearn, XGBoost)
- Pandas, NumPy
- Matplotlib, Seaborn

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/alb1nut/Mortgage-Optimization-Using-Machine-Learning.git

 
