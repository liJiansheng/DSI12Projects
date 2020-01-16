# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2:  Regression Challenge

## Predict the price of homes at sale for the Aimes Iowa Housing dataset

### Problem Statement

As a data scientist in Property Inc, our company is looking to develop residential homes in Aimes. It is important to forecast where and what kind of details to put into our development. The company is not just looking to build quality hoems, they also want to find out the variablss that make the house profitable. In order to do that, we have the housing data of Aimes Iowa.

### Data Observation

From a first look, there are many string object which suggeat a high number of category values. We will look to map them into numerical values if possible. We will split the data into number values and object for further analysis.

There are 81 columns with 2051 rows of data.

### Data Cleaning

Columns with 1000 more more null values will be dropped. There re only 2000 rows. Many of the categorical data are ordinal so we will map them to a number sequence. MS Class is category data though its type is a number. For Lot Frontage, we will fill NA values with mean of the column.

### Feature Engineering

We will handle numbers and category data separately. For numbers, we will use a heatmap to view correlation. From there we will pick how features with more than 50% or .5 correlation.

For category data, we will use bar plots to see the significance of each feature. We will see the occurence of values. Afterwhich we will do one hot encoding. For number values, scaling them caused a major drop in predictions. So we will not do it.

### Modelling

Once we merge the number and category data, we can start modellig. I used regression on all the features first. The R^2 and and mean square area was high. Iadded on RFE (Recursive Feature Elimination to cut down a number of variables.

From there, I used the variables for Ridge and Lasso. 

### Summary Analysis

This data set has many data points and cutting them down to significant features for analysis was challenging. Many methods were adopted along the way.

Initially I added did not map many of the categorical data and this resulted in many columns for categorical data. This made it hard for further analysis.
Another problem faced was after scaling the training data, the predictions were very bad in my case. Not scaling yielded a better prediction and R^2 score.

Finally, many of the categorical data are not significant in our model. The key feature was neighbourhood as we can see from our coefficents plot.

Ridge regression yielded a better result than lasso in this case.

Ridge mean prediction was **36182** as compared to Lasso **39070**

**Recommendations** <br/>After analysis, we can see that location or neighbourhood makes a significant increase in Sale Price. Not only does it affect price positively, some neighbourhood affects negatively. After location, quality of the house and other qualities like exterior and basement quality also affects the price. Garage also is a factor.

To do well, finding the right neighbourhood is crucial with a strong focus on the quality of the house will be a key factor. Another thing to consider is also the kitchen quality.

