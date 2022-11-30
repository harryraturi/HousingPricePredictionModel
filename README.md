# HOUSE PRICE PREDICTION
> A US based housing company named Surprise Housing wants to enter into Austrailian market. Their first task is to understand the market with the help of data analytics so that they can use this to purchase house properties at very low price which should be less than its actual price and sell the property at higher price.

> So company wants to understand what are the factors affecting the prices and how exactly are those factors influencing the prices.The company then would manipulate their strategy and concentrate on areas that will yield high return.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
- A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. The company has collected a data set from the sale of houses in Australia.

- **Problem Statement** : 
The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

The company wants to know:

  1. Which variables are significant in predicting the price of a house, and

  2. How well those variables describe the price of a house. 

Also, determine the optimal value of lambda for ridge and lasso regression.

- **Business Goal** : 
You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.


## Conclusions
- As when doing RFE for features selection for model building then we got R2 score better for train data but not for test data, So we have decided to check with Ridge and Lasso Regression for Regularization.

- After doing Ridge and Lasso Regression we got below summary:

    - **R2_score and Mean Squared Error for Ridge and Lasso** :
      - **Ridge Regression** 
          - R2 score [Train Data] :   0.931156
          - R2 score [Test Data]  :   0.917088
          - Mean Squared Error [Test Data]: 0.111843
      - **Lasso Regression**
          - R2 score [Train Data] :  0.921097
          - R2 score [Test Data]  :  0.916931
          - Mean Squared Error [Test Data]: 0.111949
      - **Though model performance by Ridge Regression is better than Lasso in terms of R2 Score and MSE, but better to use Lasso Regression as it also helps us in Feature Selection by shrinking most of the insignificant features to 0.**
      - **As it is always advisable to use simple yet robust model.**
   
   - **Optimal value of Alpha/Lambda for Ridge and Lasso** :
      - Ridge (**Alpha = 10.0**)
      - Lasso (**Alpha = 0.001**)
      
- Some higher valued **positive coefficients** are ['GrLivArea', 'Neighborhood(Crawfor)', 'SaleType(New)', 'OverallQual', 'SaleCondition(Normal)']
- Some higher valued **negative coefficients** are ['PropAge', 'Neighborhood (MeadowV)', 'BsmtQual (TA)', 'SaleType (WD)', 'HeatingQC (TA)']
- Higher value of Positive Coefficient, helps for high Sale Price and Higher value of Negative Coefficient, suggests dip in Sale Price.


## Technologies Used
- Python - version 3.9.12
- numpy library - version 1.21.5
- pandas library - version 1.4.2
- seaborn library - version 0.11.2
- matplotlib.pyplot library - version 3.5.1
- sklearn.model_selection - train_test_split
- sklearn.model_selection - GridSearchCV
- sklearn.preprocessing - StandardScaler
- sklearn.linear_model - LinearRegression,Ridge,Lasso
- sklearn.feature_selection - RFE
- sklearn - metrics
- sklearn.metrics - r2_score,mean_squared_error


## Acknowledgements
- This project was inspired by Upgrad.
- Referenced from Google, Case Study, Live session and Stack-Overflow


## Contact
Created by Harish Rathuri : [@harryraturi](https://github.com/harryraturi)  - feel free to contact me!
