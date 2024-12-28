# Predictive Health Insurance Model for Shield Insurance

## 
In this project, a predictive model was developed for Shield Insurance to estimate health insurance premiums based on factors like age, smoking habits, BMI, and medical history. The dataset was cleaned and preprocessed by handling missing values, encoding categorical variables, and scaling numerical features. Exploratory data analysis (EDA) revealed key relationships between features and the target variable. Various regression models were trained, and the XGBoost Regressor was optimized using hyperparameter tuning, achieving an impressive R² score of 0.96. 

![alt text](https://github.com/Kkishank/Predictive-Health-Insurance-Model-for-Shield-Insurance/blob/cacc07411b5e800780452d811ae75a531d8972c8/distribution%20of%20residuals.png)

Out of 48,000 records, 30% of the records had a margin of error within 10% between the actual values (y) and predicted values (y_pred), while 342 records exhibited a margin of error greater than 50%.

From the distribution plot comparing for Extreme Errors vs Overall:

The distribution is similar in all the features except for the age column 
The model appears to be most error-prone when dealing with younger individuals
Model performance is more reliable for middle-aged and older individuals
This suggests a potential bias or difficulty in predicting outcomes for younger age groups

![alt text](https://github.com/Kkishank/Predictive-Health-Insurance-Model-for-Shield-Insurance/blob/cacc07411b5e800780452d811ae75a531d8972c8/age%20moe.png)

This shows that majority of the extreme errors are coming from young age group (i.e. <25 years of age). We need to may be build a separate model for this segment

We segmented the data with dataset<=25 and dataset>25 and built separate models 

![alt text](https://github.com/Kkishank/Predictive-Health-Insurance-Model-for-Shield-Insurance/blob/cacc07411b5e800780452d811ae75a531d8972c8/model_seg.png)

When the dataset was segmented and built separately The margin of error with threshold of 10% was reduced from 30% to 2%


