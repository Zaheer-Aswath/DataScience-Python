The project is to predict the insurance charges based on various factors like age, sex, bmi and so on.

The dataset used in this project is downloaded from - https://www.kaggle.com/datasets/teertha/ushealthinsurancedataset/

After importing required libraries and the dataset, I have done the following:
1. Data Preprocessing - to check null values and remove the same
2. Exploraatory Data Analysis on continuous and categorical variables to check the distribution, outliers and count categorical values
3. Label encoding of categorical values
4. Find correlation between all columns to check their impact on Insurance charges prediction
5. Find coefficient of columns with charges columns using OLS model
6. Removed region column as it has very low or negligible amount of correlation and coefiicient with charges column
7. Built Linear, Ridge and Lasso models, fitted the train data and predicted the test data
8. Evaluated the models using R-square and Mean Absolute Error (MAE) metrics
9. Based on above metrics although there was not much difference among the three models, I have concluded that Linear regression is the best fit for our problem with 78% of accuracy
10. Finally, used sample test data to predict insurance charges using Linear Regression Model.
