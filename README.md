# House Price Prediction Model

![house_predict](https://github.com/user-attachments/assets/4c1dc837-dbed-454a-82f4-594aa816453f)


## Project Overview

This project focuses on developing a machine learning model capable of accurately predicting house prices based on a diverse set of features, including property characteristics, location data, and socioeconomic indicators. The goal was to identify the most effective regression technique for this task and gain insights into the factors that significantly influence housing prices.

## Methodology

The project involved the following key steps:

1.  **Data Exploration and Preprocessing:** Not much analysis was performed on the dataset as the sole aim of the project was to build the models.
   Outliers were removed from the dataset and the features were also scaled using StandardScaler.
2.  **Model Selection:** Several regression models were explored and evaluated:
    * Linear Regression
    * Ridge Regression
    * Lasso Regression
    * Decision Tree
    * Random Forest
    * Gradient Boosting
    * Support Vector Regression (SVR)
3.  **Model Training and Evaluation:** Each model was trained on the prepared dataset and evaluated using the following metrics:
    * **R² Score (Coefficient of Determination):** Measures the proportion of variance in the target variable explained by the model (higher is better).
    * **RMSE (Root Mean Squared Error):** Represents the average magnitude of the prediction errors in the same units as the target variable (lower is better).
    * **MAE (Mean Absolute Error):** Measures the average absolute difference between predicted and actual values (lower is better).
    * **MAPE (Mean Absolute Percentage Error):** Indicates the average percentage error of the predictions (lower is better).
4.  **Feature Importance Analysis:** For the best-performing model, feature importance scores were analyzed to understand the relative influence of each input feature on the predicted house prices.

## Model Performance

The performance of the evaluated models is summarized below:
| Model             | R² Score | RMSE          | MAE           | MAPE (%) |
| ----------------- | -------- | ------------- | ------------- | -------- |
| Linear Regression | 0.49     | \$185,850.00  | \$121,234.87  | 48.01    |
| Ridge Regression  | 0.49     | \$185,844.16  | \$121,233.35  | 48.01    |
| Lasso Regression  | 0.49     | \$185,849.42  | \$121,234.59  | 48.01    |
| Decision Tree     | 0.63     | \$158,369.72  | \$103,013.78  | 40.91    |
| **Random Forest** | **0.81** | **\$114,326.31** | **\$76,009.57** | **31.63** |
| Gradient Boosting | 0.76     | \$126,921.35  | \$89,634.11   | 36.79    |
| SVR               | -0.05    | \$266,186.10  | \$196,248.62  | 73.30    |

The **Random Forest** model ended up having the best overall performance, exhibiting a significantly high R² score and the lowest error metrics (RMSE, MAE, MAPE). This reinforces its strong ability to predict house prices accurately based on the provided features. The linear models showed moderate performance, while the Decision Tree and Gradient Boosting models also performed well, though not as effectively as the Random Forest. The Support Vector Regression (SVR) model again showed poor performance on this dataset.

## Feature Importance

Analysis of the feature importance scores from the Random Forest model revealed the following top contributing features:

| Feature                  | Importance |
| ------------------------ | ---------- |
| Median Household Income  | 0.275957   |
| Living Space             | 0.245242   |
| Zip Code                 | 0.089029   |
| Longitude                | 0.081173   |
| Zip Code Density         | 0.068746   |
| State\_encoded           | 0.045105   |
| Address\_encoded         | 0.044889   |
| Baths                    | 0.038187   |
| Latitude                 | 0.036058   |
| Zip Code Population      | 0.023577   |
| City\_encoded            | 0.018248   |
| County\_encoded          | 0.017879   |
| Beds                     | 0.015911   |

**Key Insights:**

* **Median Household Income** and **Living Space** are the most influential factors in predicting house prices.
* **Location-based features** (Zip Code, Longitude, Latitude, Zip Code Density) are also significant predictors.
* Encoded categorical features contribute to the model's predictive power.

## Conclusion

This project successfully developed a house price prediction model, with the Random Forest algorithm demonstrating the highest accuracy. The feature importance analysis provides valuable insights into the key determinants of housing prices within the dataset.

## Future Work

Potential areas for future development include:

* **Hyperparameter Optimization:** Fine-tuning the parameters of the best-performing models to potentially improve their accuracy further.
* **Feature Engineering:** Creating new relevant features from the existing data.

___
# Thanks for reading through
