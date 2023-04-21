# SC1015-MiniProject
Our mini project focus on medical insurance from the United States. We performed Random Forest and Catboost on the [dataset](https://www.kaggle.com/datasets/tejashvi14/medical-insurance-premium-prediction) by TEJASHVI on kaggle.


### Members
- Eugene Ian Teo-Aldridge
- Jiang Yifei
- Huang Shu yang


### Problem Definition
- What are the factors that effects the premium pricing most?  
- How can a insurance company develop an adaptive premium pricing model?  
- How can the customers choose the best value for money medical insurance plans?  


### Files
1. SC1015.csv  
2. (For the Slides)
3. SC1015_project.ipynb
    - Data Cleaning  
    - EDA and Visualization  
    - Machine Learning: Random Forest & Catboost


### Detalis
#### Data Cleaning
   a. no missing values in the data
   b. Used box plot for visualizing
   c. Outlier removal: removed the rows that contain outliers in numeric data. 2% of the whole dataset was removed.
  
  
#### Exporatory Data Analysis
   a. Used cross-vairant dot plot for guessing the correlation between the colomns.
   b. Correlation matrix helped us to observe the strength of the relationship.
   c. Define new feature 'BMI' with weight and height, and expressed it in both numeric data and categorical data.
   d. Observe the correlation between categorical data and prices by using boxplots.


#### Machine Learning
   Random forest and Catboost are used to predict the price.   
   The results are similar and Random forest is slightly better than Catboost.
   
   
### Conclusions & Recommodation
  1.  Customers can have a better understanding of what influences the premium price -- the customer’s age, weight and any history of transplants or chronic diseases will result in a higher premium price.
  2. Insurance companies can potentially experiment dropping some of the factors to make their insurance sale more attractive.
  3. The customers can use the model to predict whether the price is worth or not.
 
 
### Reflections
  1. Learnt how to use the random forest method and the high accuracy and categorical data specialised CatBoost. 
  2. Learn about gredient boosting, which is the basis of Catboost.
  3. Learnt the method on feature engineering, creating new data based on the existing data.


