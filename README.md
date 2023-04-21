# SC1015-MiniProject

School of Computer Science and Engineering
Nanyang Technological University
Lab group: B126
Group : 2

Our mini project focus on medical insurance from the United States. We performed Random Forest and Catboost on the [dataset](https://www.kaggle.com/datasets/tejashvi14/medical-insurance-premium-prediction) by TEJASHVI on kaggle.



### Members
- Eugene Ian Teo-Aldridge
- Jiang Yifei
- Huang Shu yang

### Files
1. SC1015.csv  
2. (For the Slides)
3. SC1015_project.ipynb
    - Data Cleaning  
    - EDA and Visualization  
    - Machine Learning: Random Forest & Catboost

### Description
This repository contains the ipynb file of our project, slides, video presentation and the references for any claims and methods we use in our SC1015 project. 

This README contains descriptions of the various sections of our jupyternotebook. If you want to see a full detailed rundown of our process, do refer to the jupyternotebook itself, which contains detailed descriptions and comments on the steps and our thought processes. 



### Problem Definition
There are a lot of insurance companies in America which results in a price sensitive and competetive market. A slight difference in Premium Prices can lose the companies a large number of customers. Our goal is to investigate and find out which health factors are the most important when it comes to deciding on a premium price. This can help companies make better judements on which health factors warrents an increase in premium prices, and which factors they can ignore, widening their customer base and improving profits. This can also help customers what are the determining factors that affect their premium prices, allowing them to make a more informed decision when choosing their insurance plans.

### Details
#### Data Cleaning
In this section, we worked on cleaning and preparing our data set for analysis in the next part. Since our data does not contain NULL values, there is no need for us to utilise imputation techniques to fill up the NULL values. Our categorical values are also one hot encoded, which removes the need to do so ourselves. 

We also split our numerical data into its own dataframe for ease of analysis in the EDA section. Outliers were also identified and removed. We define outliers as data that are outside of the whiskers of the box plot.
  

#### Exporatory Data Analysis
In this section, we explored the cleaned dataset to try and find if there are any relationships between the various health factors and premium pricing. We also employed feature engineering to explore if the BMI of a person will have any significant influence on the premium pricing. Futhermore, we explored the relationships between the categorical data and numerical data before deciding on which data we will use in training our model.

Here is how we did it:
  1. Used cross-vairant dot plot for guessing the correlation between the colomns.
  2. Correlation matrix helped us to observe the strength of the relationship.
  3. Define new feature 'BMI' with weight and height, and expressed it in both numeric data and categorical data. 
  4. Observe the correlation between categorical data and prices by using boxplots.  




#### Machine Learning
For our machine learning, we have decided to employ 2 different models:

Model 1: Random forest

A random forest is a very accurate model which can utilise both categorical and numerical data to make predictions. We decide to use it because it is more accurate and resistant to noise than a standard decision tree. It also has access to 'Feature Importance', allowing us to properly visualise the importance of each feature relative to one another.

Model 2: CatBoost

We decided to experiment with CatBoost as it is a model that specialises in dealing with categorical data. Since the majority of our data is categorical, we decided to utilise it. Catboost also has it's own 'feature importance', allowing us to get visualise the importance of each feature with more emphasis on our categorical data, which provides us with a different perspective.
   
   
### Conclusions & Recommodation
Over here, we compared the importance of the different health factors and explored the features that both models agreed were important. We found that there were some health factors that simply did not have much of an influence on the pricing, while others such as age had a significant influence. 

  1.  Customers can have a better understanding of what influences the premium price -- the customer’s age, weight and any history of transplants or chronic diseases will result in a higher premium price.
  2. Insurance companies can potentially experiment dropping some of the factors to make their insurance sale more attractive to those with such ailments.
  3. Insurance companies can better understand which health factors are truly important, allowing for more informed pricing

 
 
 
### Reflections
  1. Learnt how to use the random forest method 
  2. Learn about gradient boosting, which is the basis of Catboost.
  3. Learnt the method on feature engineering, creating new data based on the existing data.

### References:
  1. https://research.aimultiple.com/insurance-pricing/
  2. https://catboost.ai/en/docs/concepts/fstr
  3. https://catboost.ai/en/docs/concepts/tutorials
  4. https://scikit-learn.org/stable/auto_examples/ensemble/plot_forest_importances.html
  5. https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html
