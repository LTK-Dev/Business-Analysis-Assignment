# Bank Customer Churn Prediction

This repository contains the implementation of a customer churn prediction model for banking services. The project includes exploratory data analysis (EDA), standard pipeline implementation, and competitive approaches that achieved top rankings in multiple Kaggle competitions.

## Dataset Description

The dataset contains the following attributes:

- **RowNumber**: Record sequence number
- **CustomerId**: Unique customer identifier
- **Surname**: Customer's last name
- **CreditScore**: Customer's credit score
- **Geography**: Customer's country of residence
- **Gender**: Customer's gender
- **Age**: Customer's age
- **Tenure**: Duration of customer's relationship with the bank
- **Balance**: Customer's account balance
- **NumOfProducts**: Number of bank products used by the customer
- **HasCrCard**: Whether the customer has a credit card (1 = Yes, 0 = No)
- **IsActiveMember**: Whether the customer is an active member (1 = Yes, 0 = No)
- **EstimatedSalary**: Estimated salary of the customer
- **Exited**: Target variable indicating if the customer left the bank (1 = Yes, 0 = No)

## Project Structure

The repository contains three main Jupyter notebooks:

1. **EDA.ipynb**: Exploratory Data Analysis

   - Data visualization
   - Feature distribution analysis
   - Correlation analysis
   - Customer behavior patterns

2. **Standard_Pipeline.ipynb**: Basic Implementation

   - Standard feature engineering
   - Model training with CatBoost
   - Basic evaluation metrics
   - Simple ensemble approach

3. **Top1_Competition_Pipeline.ipynb**: Advanced Implementation

   - Advanced feature engineering techniques
   - Sophisticated ensemble methods
   - Competition-specific optimizations
   - State-of-the-art model performance

4. **LLM_predict.ipynb**: Large Language Model Prediction Pipeline
   - Uses a large language model (LLM) via Together AI API to predict customer churn
   - Preprocesses and handles missing values in telecom customer data
   - Formats customer data as prompts for the LLM
   - Sends requests to the LLM and parses predictions (Exited: 0 or 1)
   - Supports batch prediction and result export for submission

## Submission Files

The `/Submission` folder contains the following prediction files:

1. **Standard_top1.csv** (2.8MB)

   - First place submission for Data Vision 2025 competition
   - Contains predictions for 100,000 test samples
   - Format: id, Exited (probability of churn)
   - Generated using standard pipeline with basic feature engineering

2. **Competitive_Top1.csv** (2.8MB)

   - First place submission for Playground Series S4E1 competition
   - Contains predictions for 100,000 test samples
   - Format: id, Exited (probability of churn)
   - Generated using advanced pipeline with competition-specific optimizations

3. **BankChurnNew_top1.csv** (255KB, 10,002 lines)
   - First place submission for Public Telecom Customer Churn Analysis and Prediction
   - Contains predictions for 10,000 test samples
   - Format: id, Exited (probability of churn)
   - Generated using specialized pipeline for telecom customer churn prediction

Each submission file represents the best performing model for its respective competition, showcasing different approaches to the churn prediction problem.

## Competition Results

The implementation achieved top rankings in multiple Kaggle competitions:

1. **Data Vision 2025**

   - Submission: Standard_top1.csv
   - Result: 1st Place

2. **Playground Series S4E1**

   - Submission: Competitive_top1.csv
   - Result: 1st Place

3. **Public Telecom Customer Churn Analysis and Prediction**
   - Submission: BankChurnNew_top1.csv
   - Result: 1st Place

## Key Features

- Comprehensive data preprocessing
- Advanced feature engineering
- Multiple model ensemble approach
- Competition-specific optimizations
- Detailed performance analysis

## Requirements

The project requires the following Python packages:

- autogluon==1.1.0
- xgboost==1.7.6
- scikit-learn==1.3.2
- lightgbm==4.3.0
- catboost
- pandas
- numpy
- matplotlib
- seaborn

## Usage

1. Clone the repository
2. Install required packages
3. Run the notebooks in sequence:
   - Start with EDA.ipynb for data understanding
   - Use Standard_Pipeline.ipynb for basic implementation
   - Explore Top1_Competition_Pipeline.ipynb for advanced techniques

## Model Performance

The final ensemble model combines:

- CatBoost predictions (70% weight)
- AutoGluon predictions (30% weight)

This combination achieved optimal performance across multiple competitions.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
