# Project 2 - Ames Housing Data and Kaggle Challenge
In this project, we were provided with the Ames Housing Dataset and our job is to create a model using the regression technique that can best predict the sale price of houses in the vicinity.
The objective is to improve on the model to achieve the best prediction results as possible.
The Data Description is provided in this [link](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)

# Problem Statement
From the Ames Housing Dataset, create a model to predict the housing prices and determine which features are the best to maximize the value of your house.

# Summary of Process
The Dataset consist of 81 features and 2051 observations. 1 of the features is the Sale Price and the others are different properties of the house.

3 Models were created and tested.

## Process

The data was cleaned. Features with too many null values were dropped and the rest were replaced with their respective values.
The main data set was split into 3 datasets.(Ordinal, Nominal, Continuous). Exploratory data analysis was performed on each of the datasets

The first model was built by finding the features with the highest correlations from each dataset with respect to sales price.
From there, we combined the features into 1 dataset and checked for multicollinearity between features and removed those features. The model was predicted with Ridge Regression and predicted sales price was submitted to Kaggle.
Kaggle Score for Model 1: RMSE = 31730.63840 (Public) , 33019.52792 (Private)

The second model was first run through the Lasso Regression to eliminate any features that does not have any significance to the Sale Price. Once these features were eliminated, the top 26 features with the highest absolute coefficient was selected and checked for multicollinearity.
After that, the model was predicted with Ridge Regression and predicted sales price was submitted to Kaggle.
Kaggle Score for Model 2: RMSE = 28669.97609 (Public) , 31707.44886 (Private)

The third model was created by combining certain features that seemed to relate to each other. Then the highest few features with correlation to Sales price was choosen and checked for multicollinearity.
After that, the model was predicted with Lasso Regression and predicted sales price was submitted to Kaggle.
Kaggle Score for Model 3: RMSE = 33611.97639 (Public) , 33342.21643 (Private)

# Conclusion
The best model created would be the second model as the public and private RMSE are the lowest.
The best features are General Living Area, Overall Quality and Year house was built.
The worst features are the number of bedrooms in your house and if the type of house you have is the end units of a twinhouse.
