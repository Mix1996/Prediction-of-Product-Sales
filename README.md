# Data Science - Prediction of Product Sales
##  Using machine learning to make predictions about future sales based on the data provided. 

**Author**: 
Mikhail Pillay
### Business problem:

**The objective is to help the retailer by using machine learning to make predictions about future sales based on the data provided. The goal of this is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales.**


### Data:
Sales Dataset: [https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries](https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view?usp=sharing)

For this dataset, there were 8524 rows and 12 columns.
Here is the Data Dictionary for this dataset:

![image](https://github.com/Mix1996/Prediction-of-Product-Sales/assets/53317324/aaabd1c7-b8e9-46f0-b81a-e0b54154a37d)

## Methods
**To prepare this data, the data was cleaned, and the following processes were performed:**
- Drop duplicates and fix inconsistencies in categorical data.
- Identify the features (X) and target (y): Assign the "Item_Outlet_Sales" column as your target and the rest of the relevant variables as your features matrix.
- Perform a train test split
- Create a preprocessing object to prepare the dataset for Machine Learning
- Imputation of missing values occurs after the train test split using SimpleImputer.

**Maching Learning Using the Following Models:**
- Linear regression model
- Random Forest Regressor Model
- Tuned/Best Random Forest Regressor Model


## Results

#### Visual 1 - Best Forest Model VS Linear Model - Testing Data
![image](https://github.com/Mix1996/Prediction-of-Product-Sales/assets/53317324/af2b409f-673a-42d1-a363-9ade0ac15f44)


> Both models have very similar performance metrics across the board. The differences in R-squared, MAE, MSE, and RMSE are relatively small, suggesting that their predictive performance on the testing data is quite comparable.

#### Visual 2 - Best Forest Model Training and Testing results
![image](https://github.com/Mix1996/Prediction-of-Product-Sales/assets/53317324/4b1df59f-2fe3-451b-9cc7-ed7e4c85bcc5)



>The model's performance metrics are relatively consistent between the training and testing data. This suggests that the model is generalizing reasonably well to new, unseen data. While the R-squared values indicate that there is room for improvement in explaining more of the variance, the MAE, MSE, and RMSE values show that the model's predictions are consistently close to the actual values on both training and testing datasets.
## Model

Given that the goal is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales, a Linear Model might be a better choice. Its interpretability allows retailers to gain clear insights into the effects of different features on sales. This can be highly valuable for making informed decisions related to product and outlet strategies.

Report the most important metrics

**Linear Regression Model:**
Results for testing data:
  - R^2 = 0.4
  - MAE = 886.468
  - MSE = 1463444.832
  - RMSE = 1209.729

**Random Forest Model:**
Results for testing data:
  - R^2 = 0.291
  - MAE = 965.583
  - MSE = 1729902.972
  - RMSE = 1315.258

**Best Forest Model:**
Results for testing data:
  - R^2 = 0.39
  - MAE = 885.384
  - MSE = 1489129.284
  - RMSE = 1220.299

The Final Model Chosen was a Linear Regressor Model with the n_estimators tuned to 150.

For the testing set on the model, 39% of the variance in y was explained by x.

The Mean Absolute Error was off by about $885.384.

The Mean Squared Error was $1 489 129.284.

The Root Mean Squared Error had a calculation of $1 220.299.

## Recommendations:

The Linear Regression Model and the Best Forest Model both seem to be competitive choices. Both of these models have R-squared values around 0.4, indicating that they explain a similar portion of the variance in the data. Additionally, their MAE, MSE, and RMSE values are relatively close.

However, considering the slightly better performance of the Best Forest Model in terms of MAE, MSE, and RMSE, it may be the preferable choice. It also has a comparable R-squared value while achieving slightly better accuracy in terms of error metrics. Therefore, the Best Forest Model could be the recommended choice for making predictions based on the provided data.


## Limitations & Next Steps

As always, it's important to consider factors beyond just the numerical metrics, such as model complexity, interpretability, and any domain-specific considerations that may influence your decision.


### For further information


For any additional questions, please contact **mikhailpillay83@gmail.com**
