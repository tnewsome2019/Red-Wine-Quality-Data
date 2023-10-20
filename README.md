# INST414 Final

## Introduction

In this analysis, I delve into the world of red wine, exploring its physiochemical properties such as pH levels and acidity to gain insights into its overall quality. Additionally, I investigate the interplay between these properties and whether they collectively influence a wine's quality rating. The intricacies of what defines a "good" or high-quality wine are multifaceted, with numerous factors that can enhance or detract from its rating.

I will be utilizing the Red Wine Quality dataset sourced from the UCI machine learning repository [here](https://archive.ics.uci.edu/ml/datasets/wine+quality).

The choice of this dataset stems from my curiosity about the level of specificity involved in defining a good red wine. The world of wine is renowned for its meticulous attention to seemingly imperceptible details during evaluation.

## Data

- **Quality**: The dependent variable for this analysis is the wine's quality rating, which falls on a scale of 1 to 10.
- **Alcohol**: Denotes the alcohol content percentage of the wine.
- **pH**: Quantifies the acidity or basicity of the wine on a scale ranging from 0 (very acidic) to 14 (very basic). Most wines typically have pH levels between 3 and 4.
- **Chlorides**: Reflects the salt content in the wine.
- **Residual Sugar**: Represents the remaining sugar content after the fermentation process.
- **Citric Acid**: Present in small quantities, citric acid can contribute to freshness and flavor in wines.
- **Volatile Acidity**: Indicates the presence of acetic acid in wine, which, at excessive levels, can lead to an unpleasant vinegar-like taste.
- **Fixed Acidity**: Refers to the nonvolatile acids in wine that do not readily evaporate.

## Method

The dataset was collected from the UCI machine learning repository, with a specific focus on red wine. Fortunately, the dataset didn't contain any missing or null values, simplifying the analysis process. "Total sulfur dioxide" was omitted due to its low correlation with the "quality" column.

## Analysis

Variables were meticulously defined, with "quality" as the target variable and other physicochemical properties as the independent variables. The quality variable was transformed into a binary classification, and the data was partitioned into training (70%) and test (30%) sets. A SciKit Learn Logistic Regression model and a Random Forest Classifier were then applied to predict the quality rating of red wine.

## Results

The model displayed an impressive accuracy score of 98%, suggesting high precision in predictions. The Random Forest Classifier, too, achieved a matching accuracy score of 98%, reinforcing the strong connection between the quality rating and the physiochemical composition of red wine.

## Conclusion

The analysis aimed to shed light on several key questions about the relationships between these variables.

**To what extent do citric acid, pH, and chlorides influence a red wine's overall quality rating?**

Citric acid exhibits a positive effect on wine quality, with the highest ratings occurring in wines with citric acid levels between 0 and 0.5, gradually declining as levels increase.

pH levels between 2 and 5 show a marginal negative influence on wine quality. The correlation between average pH levels and quality ratings suggests that pH levels at the lower or higher extremes have minimal impact on quality.

Chloride levels exhibit a negative relationship with quality, indicating higher quality when chlorides are lower.

**Do the acidity levels (fixed, volatile, citric) compromise alcohol content percentage?**

The pair plot analysis reveals that acidity levels do not significantly affect alcohol content. Intriguingly, a positive relationship exists between citric acid and fixed acidity, while a negative relationship exists between citric acid and volatile acidity.

**For wines with high volatile acidity, can high sugar levels contribute to a high quality rating?**

Wines with elevated volatile acidity tend to have low residual sugar content, typically below 5. These wines receive higher quality ratings when volatile acidity falls between 0.2 and 1. Additionally, wines with average residual sugar levels tend to have higher quality ratings. However, higher residual sugar amounts do not result in higher quality ratings. Consequently, introducing high sugar levels to wines with high volatile acid content does not lead to a higher quality rating.
