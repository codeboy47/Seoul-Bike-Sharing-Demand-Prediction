# Seoul Bike Sharing Demand Prediction

The goal is to analyze and predict the demand of rented bikes. The dataset has 8,760 observations with 14 columns containing both categorical and numeric/non-categorical data.

## Problem statement
Rental bikes are presented in numerous metropolitan cities to improve portability. It is essential to make rental bikes accessible and open to people as it reduces the waiting time. Thus, fulfilling the demand of the city with a stable stock of rental bikes becomes the main issue. So it becomes crucial to predict the bike count expected every hour for the stable supply of rented bikes.

## Approach
- Understanding Business problem
- Data collection & Preprocessing
  - Data cleaning
  - Missing Data Handling
- Exploratory Data Analysis
  - Understanding categorical and numerical features
  - EDA conclusion
- Data manipulation
  - Feature Engineering
  - Outlier Detection & Treatment
  - Feature scaling
  - Categorical Data encoding
- Modelling
  - Train Test split
  - Fitting models to a Data
  - Hyperparameter Tuning
- Model Performance & Evaluation
  - Visualizing Model Performance
  - Base models v/s Tuned models
- Conclusion and Recommendations

## Data insights
1. People prefer rented bikes when temperature is high and humidity is low.
2. During holidays the demand for rented bikes is less compared to when there are no holidays.
3. People like to take rented bikes when rainfall and snowfall are low.
4. The demand is high in the morning and even higher in the evening which shows employees mostly prefer rented bikes before and after their working hours.
5. The demand is high in the month of June followed by July and May whereas the demand is lowest in the month of December, January and February.

## Models applied and their comparison
Regression algorithms used for predictions:
| S.No | Algorithm | RMSE | MAE | R2 | Adjusted R2 |
| --- | --- | --- | --- | --- | --- |
| 1. | Linear regression | 304.39021 | 208.32013 | 0.76824 | 0.76236 |
| 2. | Polynomial regression(2nd degree) | 186.33570 | 117.37459 | 0.91315 | 0.91094 |
| 3. | Lasso regression | 304.78331 | 208.25760 | 0.76764 | 0.76174 |
| 4. | Ridge regression | 304.79281 | 208.28786 | 0.76762 | 0.76173 |
| 5. | ElasticNet | 304.79324 | 208.27995 | 0.76762 | 0.76173 |
| 6. | Decision tree regressor | 250.74488 | 151.93542 | 0.84273 | 0.83874 |

There is not much difference between R2 and adjusted R2 which means the features that we added are significant to the model.

## Conclusion
- The R2 score for linear regression and all the regularization techniques like lasso, ridge and elasticnet is almost the same.
- For decision tree, the R2 score comes out to be 0.84. Also, the RMSE and MAE are comparatively low from other regression algorithms.
- 2nd-degree polynomial regression has the highest value of R2 score which means there is a non-linear relationship between the dependent and independent variables.

Hence we can rely on polynomial regression for predicting the bike count required at each hour in order to maintain the stable inventory of rental bikes.
