# Sales Forecasting Project

## Overview
This project focuses on developing and testing machine learning models to predict sales figures based on historical data. The project demonstrates the entire data science pipeline, including data preprocessing, exploratory data analysis, feature engineering, model training, and evaluation.

---

## Objectives
- **To forecast the number of items sold using historical sales data.**
- **To compare the performance of various regression models.**
- **To identify key features contributing to the predictions.**

---

## Methodology
The methodology follows these structured steps:
### 1. **Importing Packages**  
   Essential libraries for data manipulation, visualization, and machine learning (e.g., `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`, and `xgboost`) are imported.
   
### 2. **Exploratory Data Analysis (EDA)**  
   - Analyze the data structure, size, missing values, and unique entries.
   - Summarize the dataset and preview key patterns and anomalies.
   
### 3. **Data Visualization**  
   - Visualize distributions of key features such as `country`, `store`, and `num_sold` using bar plots and scatter plots.
   - Create insightful plots for identifying trends and relationships.

### 4. **Feature Engineering**  
   - Extract temporal features from the `date` column, such as `year`, `month`, `day`, and `day_of_week`.
   - Encode cyclic features using sine and cosine transformations.
   - Generate dummy variables for categorical features (e.g., `country`, `store`, `product`).

### 5. **Data Splitting**  
   - Split data into training and test sets (75% training, 25% testing).
   
### 6. **Model Training**  
   - Train three regression models:
     - Random Forest Regressor
     - Gradient Boosting Regressor
     - XGBoost Regressor
   - Evaluate the models using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), Mean Absolute Percentage Error (MAPE), and R². <p>
   
   <table align="center">
     <tr>
       <th>MODEL</th>
       <th>MAE</th>
       <th>MSE</th>
       <th>MAPE</th>
       <th>R²</th>
     </tr>
     <tr>
       <td>Random Forest Regressor</td>
       <td align="center">8.356004</td>
       <td align="center">254.881242</td>
       <td align="center">0.052009</td>
       <td align="center">0.992415</td>
     </tr>
     <tr>
       <td>Gradient Boosting Regressor</td>
       <td align="center">18.932657</td>
       <td align="center">1028.543518</td>
       <td align="center">3.451058</td>
       <td align="center">0.966299</td>
     </tr>
     <tr>
       <td>X Gradient Boosting Regressor</td>
       <td align="center">7.926935</td>
       <td align="center">197.354002</td>
       <td align="center">0.067435</td>
       <td align="center">0.994139</td>
     </tr>
   </table>

   - The models performed well with the best model *(Random Forest Regressor)* having a Mean Percentage Error of **~5% (5.20%)** indicating a high predictive power with very minor errors

### 7. **Model Evaluation**  
  - **Regression Plots**
     - The **near-perfect alignment** of points with the diagonal indicates **excellent predictive accuracy** for all three models.

     - **Random Forest and X Gradient Boosting** seem to **slightly outperform** **Gradient Boosting** in prediction consistency, based on the tightness of the scatter plot clusters.

   ![1 2](https://github.com/user-attachments/assets/5a3f1c16-0cf6-4fbf-b718-e0198b3cca80)

  - **Feature Importance**  
    - With regards to feature importance the most consistently influencial feature was 
      - **Kagglazon Store** and 
      - **
      Win Friends and Influence People (Product)**  
    - Other notables features were;  
      - **Argentina (Country)**  
      - **Canada (Country)**

   ![1 3](https://github.com/user-attachments/assets/48751ce5-fb4d-42f7-b4f2-992ff92bfbb0)
