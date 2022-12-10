# INST414 Final
## Introduction 

The topic that I have chosen for data analysis is red wine, and how it’s physiochemical contents, like pH levels and acidity, can inform its overall quality. Additionally, I will examine how some contents affect other content areas, and if all of those elements interacting with each other has a significant effect on the wine. There is a lot that goes into what makes a wine “good” or of high quality, and with that, there are many areas that could fall short and also affect the overall rating or the wine for better or worse.

I will be using the Red Wine Quality dataset from the UCI machine learning repository (https://archive.ics.uci.edu/ml/datasets/wine+quality).
 
I chose to work with this dataset because I am curious to see how much particularity there is around a good red wine, since I know that the world of wine itself is very particular as far as the seemingly-unnoticeable details that are considered during the assessment. 

## Data
The dependent variable for the analysis is the wine’s quality rating, which is the overall rating of each red wine sample on a scale of 1-10. The independent variables are the volatile acidity, fixed acidity, citric acid, pH level, residual sugar, and alcohol content. 

**Quality**
Output variable (based on sensory data, score between 0 and 10)

**Alcohol**
The percent alcohol content of the wine

**pH**
Describes how acidic or basic a wine is on a scale from 0 (very acidic) to 14 (very basic); most wines are between 3-4 on the pH scale

**Chlorides**
The amount of salt in the wine

**Residual Sugar**
The amount of sugar remaining after fermentation stops

**Citric Acid**
Found in small quantities, citric acid can add 'freshness' and flavor to wines

**Volatile Acidity**
The amount of acetic acid in wine, which at too high of levels can lead to an unpleasant, vinegar taste

**Fixed Acidity**
Most acids involved with wine or fixed or nonvolatile (do not evaporate readily)


## Method
The data was collected through the UCI machine learning repository. The repository contained datasets for both red and white wine, but I went with red. Luckily there were no missing or null values in the dataset, which made my analysis much simpler. I dropped "total sulfur dioxide" due to its low correlation with the "quality" column. 

## Analysis
The variables were defined, with "quality" as the target variable, and the other physicochemical properties as the x-value. The quality variable was coded from being a range of 0 - 10, to binary for classicfiction. The data was also split into a training and test set, where 30% of the data was for testing and the other 70% was for training. The SciKit Learn Logistic Regression model and Random Forest Classifier algorithm was then fit to the dataset and used to predict red wine quality rating. 

## Results
The model had an accuracy score of 98%, which means that it is highly accurate in its prediction. The model also had an accuracy score of 98% with the use of the Random Forest Classifier, which means it is still equally as accurate in predicition the quality. This verifies the relationship between the quality rating and the physiochemical makeup of the red wine. 

## Conclusion

The purpose of this analysis was to answer some questions about the relationship between all of the variables.
**How much of an effect does a red wine’s citric acid, ph, and chlorides have on its overall quality rating?**

A red wine’s citric acid shows to have a postive effect on the quality of the wine. It seems as citric acid between 0 and 0.5 have an increse in quality, but it drops the further it goes along.   

The wine’s pH levels, between 2-5, also appear as having slight negative influence on the wine’s quality. The graphs shows concentration and correlation between an average pH level and an average quality rating, with pH levels on the lower or higher end not significantly changing the quality. 

The wine’s chloride levels on the graph have a negative relationship with the quality rating. Quality is higher when the chlorides are low.  

**Does a red wines acidity levels (fixed, volatile, citrus) compromise the alcohol content percentage?**

The pair plot told us that the acidity levels had no effect on the alcohol content of the wine. Interestingly enough, there was a positive relationship between the citric acid and fixed acidity, and a negative relationship between citric acid and volatile acidity. 

**For wines with high amounts of volatile acid, can the introduction of high levels of sugar still contribute to a high quality rating?**

For wines with high amounts of volatile acid, the residual sugar content levels were low, or less than 5. Likewise, the quality rating showed to be higher in wines with a volatile acidity between 0.2 and 1. Additionally, wines with average amounts of residual sugar made for higher quality ratings, as well. When volatile acidity levels are too high, it can create an unpleasant vinegar taste that might contribute to a lower rating. Volatile acidity between 0.5 and 1 make for higher quality ratings (average to high), and those same volatile acidity levels are related to low-average amounts of residual sugar. Higher amounts of residual sugars do not cause higher quality ratings, so we can conclude that the introduction of high levels of sugar in wines with high levels of volatile acid do not contribute to a high quality rating. 

 
