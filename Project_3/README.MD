# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3:  Web APIs & Classification

## Classifying Android & Iphone Reddit Posts

### Problem Statement

As a data scientist in Android Inc, we are looking at how to better design and develop android phones. There are many variants of Android and we want to look at reddit forums to see what users prefer in a mobile phone. At the same time, Android has a close competitor, Iphone. <br><br>We would also want to look at their users comments on Iphone as well. However as there are still differences in the phones' users and usage, we would want to classify the two types of reddit posts to enhance our research.

### Analysis Method

- Web scraping Android and Iphone Posts from Reddit
- Exploratory Data Analysis
- Modeling
- Model Evaluation
- Conclusion and Recommendations

### Web Scraping Android and Iphone Posts From Reddit

The 2 reddit topics used are:
https://www.reddit.com/r/Android/

https://www.reddit.com/r/iphone/new

Each of these topics will extract around 800 posts without duplicates.

### Exploratory Data Analysis

These are the steps taken to prepare our data for our model.

- **Selftext** and **title** are chosen to be used for our classification as these are the 2 main columns with text content.
- **Subreddit** will be our target as it indicates the post category.
- Combine Android and Iphone dataframes.
- Null values of are filled with blank.
- Concat selftext and title into one column **content**.
- **Subreddit** is map to 1 and 0.
- We do a train test split on our data.
- We create a function to remove HTML, remove characters, remove stop words and lemmatize our content.

### Modeling

We first get a baseline score from our current data frame. Baseline is 0.52. Our models should perform better than baseline.

The 2 models we will look at are Logistic Regression and Naive Bayes Multinomial. Before implementing our models, we need to use feature text extraction using CountVectorizer and TFIDVectorizer. 

Our models are implemented using Pipelines. 

### Model Selection

We will evaluate our model using statistics from confusion matrix, accuracy score and Receiver Operating Characteristic curve.

To ease our comparison, compareStats function is created to put the 2 model statistics side by side.

```
Stats     | Logistic Regression | Multinomial |
================================================
Recall    |           0.92      |   0.9       |
Precision |           0.8       |   0.81      |
Score     |           0.84      |   0.84      |
TP        |           181       |   178       |
TN        |           134       |   136       |
FP        |           45        |   43        |
FN        |           16        |   19        |
```

##### Observations

We can see from the stats that both models performed similarly. In our case, precision score is important as we want to accurately identify Android posts. we want to know what Android users comment about their android phones and implement the right features. If If we wrongly implement a feature that was commented by an Iphone user on their Iphone, it may cause design and sales issues. However in this case, our both models have only slight differences in our most scores. 

**Recommendations** <br/>From the model stats and ROC AUC curve, both models perform similarly and with acceptable accuracy. 

- We can look at other models to see if they can do better than our current models.
- To further build on this project, we can look at sentiment analysis on the 2 topics. We can also look at specific mobile phone features that has more positive sentiment.