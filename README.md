# Sales Forecasting Notebook

## Overview
This notebook focuses on developing and testing machine learning models to predict sales figures based on historical data. The project demonstrates the entire data science pipeline, including data preprocessing, exploratory data analysis, feature engineering, model training, and evaluation.

---

## Objectives
- **To forecast the number of items sold using historical sales data.**
- **To compare the performance of various regression models.**
- **To identify key features contributing to the predictions.**

---

## Methodology
The methodology follows these structured steps:
1. **Importing Packages**  
   Essential libraries for data manipulation, visualization, and machine learning (e.g., `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`, and `xgboost`) are imported.
   
2. **Exploratory Data Analysis (EDA)**  
   - Analyze the data structure, size, missing values, and unique entries.
   - Summarize the dataset and preview key patterns and anomalies.
   
3. **Data Visualization**  
   - Visualize distributions of key features such as `country`, `store`, and `num_sold` using bar plots and scatter plots.
   - Create insightful plots for identifying trends and relationships.

4. **Feature Engineering**  
   - Extract temporal features from the `date` column, such as `year`, `month`, `day`, and `day_of_week`.
   - Encode cyclic features using sine and cosine transformations.
   - Generate dummy variables for categorical features (e.g., `country`, `store`, `product`).

5. **Data Splitting**  
   - Split data into training and test sets (75% training, 25% testing).
   
6. **Model Training**  
   - Train three regression models:
     - Random Forest Regressor
     - Gradient Boosting Regressor
     - XGBoost Regressor
   - Evaluate the models using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), Mean Absolute Percentage Error (MAPE), and R².

7. **Model Evaluation**  
   - Visualize regression plots for predicted vs. actual values.
   - Analyze feature importance for each model.

---

## Key Code Features
- **Custom Functionality:**  
  A utility function `resultify` is designed to process and store evaluation results across multiple models.
  
- **Data Visualization:**  
  Comprehensive visualization of relationships and model performance to support data-driven insights.

- **Feature Engineering:**  
  Leveraging temporal and categorical features to enhance model performance.

---

## Outputs
- **Visuals:**  
  Regression plots for model predictions and feature importance visualizations.
- **Metrics:**  
  Performance scores for models to facilitate comparison and selection.
