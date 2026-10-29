# DSA2050-Week6-672112
# DSA2050 Week 6: Guided Regression Lab

## Student Information

- **Student Name:** [Valentine Wachira]
- **Student ID:** [672112]
- **Course:** DSA2050
- **Lab:** Week 6 - Guided Regression Lab

## 1. Lab Objective

The objective of this lab was to develop and evaluate regression models for predicting sales using the provided sales dataset. The analysis compared different machine learning models to determine which model produced the most accurate predictions of sales in Kenyan shillings (KES).

The lab also involved data preprocessing, model evaluation, cross-validation, residual analysis, and investigating overfitting.

## 2. Dataset

The dataset used was `DSA2050_Week6_Sales_Data.csv`.

It contains 320 observations and seven columns, including:

- AdvertisingSpend_KES
- StoreVisits
- DiscountPercent
- Region
- CustomerSegment
- ProductCategory
- Sales_KES

The target variable was `Sales_KES`. The remaining six variables were used as predictors.

The dataset contained no missing values and no duplicate rows.

## 3. Models Compared

The following models were evaluated:

1. Mean Baseline
2. Median Baseline
3. Linear Regression
4. Ridge Regression
5. Decision Tree Regression

The models were compared using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and the coefficient of determination (R^2). Five-fold cross-validation was also used to assess model performance.

## 4. Best Model

Ridge Regression was the best-performing model among the three trained regression models based on the test-set results.

Its evaluation results were:

- **MAE:** KES 13,714.40
- **RMSE:** KES 17,458.82
- **R^2:** 0.8705

The five-fold cross-validation results for Ridge Regression were:

- **Cross-validation MAE:** KES 15,971.37
- **Cross-validation RMSE:** KES 20,103.54
- **Cross-validation R²:** 0.8479

Ridge Regression performed slightly better than Linear Regression. However, the difference between the two models was small.

## 5. Two Key Findings

### Finding 1: Ridge Regression performed best

Ridge Regression achieved the lowest test-set MAE among the trained regression models, at KES 13,714.40. Its R² of 0.8705 indicates that the model explained approximately 87.05% of the variation in sales in the test set.

### Finding 2: The unrestricted Decision Tree showed overfitting

The unrestricted Decision Tree achieved a training MAE of 0.00 but a test MAE of KES 26,797.50. This suggests that it memorised the training data rather than generalising well to unseen observations.

The regularised tree performed better than the unrestricted tree on the test set.

## 6. Three Limitations

1. **Small dataset:** The dataset contains only 320 observations. A larger dataset could provide a more reliable assessment of model performance.

2. **Limited predictors:** The model uses only the variables provided in the dataset. Other factors, such as seasonality, competition, product availability, and changing customer demand, could also influence sales.

3. **Generalisation limitations:** The models were evaluated using a particular train-test split and cross-validation on the available dataset. Their performance may differ when applied to new data or different business conditions.

## 7. Conclusion

Ridge Regression was selected as the best-performing trained regression model because it achieved the lowest test-set MAE and performed slightly better than Linear Regression during cross-validation.

However, its advantage over Linear Regression was small. Further evaluation using additional data would help determine whether it remains the most reliable model for future sales predictions.
