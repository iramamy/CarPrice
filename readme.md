# Car Price Prediction

## Table of Contents

- [Introduction](#introduction)
- [Data Collection](#data-collection)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Feature Engineering and Selection](#feature-engineering-and-selection)
- [Model Description and Training](#model-description-and-training)
- [Model Performance and Evaluation](#model-performance-and-evaluation)
- [Key Factors Influencing Car Prices](#key-factors-influencing-car-prices)
- [Industry Insights and Applications](#industry-insights-and-applications)
- [Future Enhancements and Model Monitoring](#future-enhancements-and-model-monitoring)
- [Conclusion](#conclusion)
- [Tags](#tags)

## Introduction

The Car Price Prediction project aims to create a predictive model that can estimate the price of cars based on their features. The model is built using the **RandomForestRegressor**, known for its robustness in handling both numerical and categorical data. The final model achieves an **R² score of 96.87%**, significantly outperforming the baseline Linear Regression model.

## Data Collection

The dataset used in this project contains **8,128 rows** and **13 columns** of car features, including variables such as mileage, engine size, max power, torque, and seats. The target variable is the car price. The dataset is publicly available and can be easily integrated into any machine learning pipeline.

## Data Cleaning and Preparation

In the data cleaning process:

- Missing values were found in key columns like mileage, engine size, max power, torque, and seats (around **221 rows**).
- Given the minimal impact, rows with missing values were removed rather than imputed to ensure data consistency and accuracy.

By eliminating these incomplete rows, the dataset remained robust enough for reliable model training.

## Exploratory Data Analysis (EDA)

To understand the relationships between car features, a detailed exploratory data analysis was conducted:

- Correlations between variables were explored using a **heat map**.
- No significant multicollinearity was detected, allowing for the retention of most features.
- Visualizations like **histograms** and **scatter plots** were used to further understand distributions and relationships between car attributes.

## Feature Engineering and Selection

Feature engineering and selection included:

- Categorical features like **car brands** and **fuel type** were encoded to be used by the model, ensuring compatibility with the RandomForestRegressor.
- A **feature importance analysis** was conducted after training, revealing that key features like **transmission type**, **max power (BHP)**, **age**, and **engine size** were the most influential in determining car prices.

All features were retained in the final model as even less significant ones were found to add valuable information to the overall prediction.

## Model Description and Training

For the prediction task, **RandomForestRegressor** was chosen due to its ability to capture complex, non-linear relationships between variables and handle both categorical and numerical data types effectively.

- **RandomForestRegressor**: An ensemble method that builds multiple decision trees and averages their predictions to reduce overfitting and improve model accuracy.
- The model was trained using **300 estimators** for robust performance.
- The dataset was split into **70% training** and **30% testing**, ensuring the model was evaluated effectively on unseen data.

### Why RandomForest?

The RandomForestRegressor was chosen over other models (e.g., Linear Regression) because:

- It handles both categorical and numerical data without heavy preprocessing.
- It can manage outliers and missing data more effectively.
- The ensemble approach reduces the risk of overfitting.

## Model Performance and Evaluation

The performance of the model was assessed using the following metrics:

| Metric                | RandomForestRegressor  | Linear Regression     |
|-----------------------|------------------------|-----------------------|
| **MSE**               | 21,057,978,610.40       | 218,848,783,799.94    |
| **MAE**               | 72,712.00               | 278,266.34            |
| **R² Score**          | 96.87%                  | 67.48%                |

The RandomForestRegressor significantly outperformed the Linear Regression model across all metrics, showcasing its ability to handle complex relationships in the data.

- **R² score of 96.87%** indicates the model explains nearly all variance in the target variable.
- Low **MSE** and **MAE** values confirm that the model's predictions are accurate.

## Key Factors Influencing Car Prices

The most significant features influencing car prices were:

- **Transmission Type**: Automatic transmissions generally command higher prices than manual ones.
- **Max Power (BHP)**: Higher power correlates with higher prices, as more powerful engines tend to be in premium cars.
- **Age of the Vehicle**: Newer cars are generally priced higher due to modern features and lower wear and tear.
- **Engine Size**: Larger engine capacities contribute to higher car prices.

Secondary factors include **mileage**, **fuel type**, and **brand**.

## Industry Insights and Applications

### For Car Dealerships:

- **Engine Power & Capacity**: Emphasize engine specs in marketing to attract performance-oriented buyers.
- **Dynamic Pricing**: Implement a pricing strategy based on high-value features such as engine power and size.
- **Mileage and Age**: Although less influential, consider these factors when pricing older cars with higher mileage.

### For Customers:

- **Engine and Performance**: Consider max power (BHP) and engine capacity as key indicators of a car's value.
- **Age and Condition**: Newer, well-maintained cars typically hold higher resale value.

## Future Enhancements and Model Monitoring

### Enhancing the Model:

- **Additional Data Features**: Include more granular features such as accident history, service records, and safety ratings.
- **Advanced Modeling**: Experiment with models like Gradient Boosting or XGBoost for improved performance.
- **Data Imbalances**: Ensure a balanced dataset for training, representing a wide range of car brands and price ranges.

### Model Monitoring:

- **Retraining**: Periodically retrain the model with new data to reflect changing market trends.
- **Live Monitoring**: Use dashboards to track model performance and detect anomalies.
- **User Feedback**: Continuously collect feedback from dealerships and customers for model refinement.

## Conclusion

The Car Price Prediction project demonstrates the power of ensemble learning through **RandomForestRegressor** in accurately predicting car prices. By leveraging key features like transmission type, engine power, and age, this model offers valuable insights for both car dealerships and customers.

## Tags

- Car Price Prediction
- RandomForestRegressor
- Exploratory Data Analysis
- Feature Engineering
- Machine Learning
- Python
- Data Science
