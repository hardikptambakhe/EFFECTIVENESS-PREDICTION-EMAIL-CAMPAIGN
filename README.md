# EFFECTIVENESS-PREDICTION-EMAIL-CAMPAIGN

Introduction
As Mentioned in the Resume, I have Worked on the EMAIL CAMPAIGN EFFECTIVENESS PREDICTION, as the Name Suggested this Project belongs to retail Domain.
Our Client approached us to make a Model, to predict Most of the small to medium business owners are making effective use of Gmail-based Email marketing Strategies for offline targeting of converting their prospective customers into leads so that they stay with them in Business.
The main objective is to create a machine learning model to characterize the mail and track
the mail that is ignored; read; acknowledged by the reader. 
In addition to the ML Model prediction, we also analyzed what all features can help us in getting the Email status to be not ignored by the customers.
Import Libraries
After gathering the data the next step is to import the required libraries. Python has a wide number of libraries which makes the work easier. Here pandas, numpy, matlplotlib, seaborn, math, sklearn etc.
Data Gathering
The First and the Most prominent think is to collect the data. As we know Data is necessary for the correct operation of the machine learning system, just like Oxygen is for Living Organisms.
In our case, Basically Clint Provided as the Data through the SQL Server, and we have a team of Data Engineers who fetch the data to our server, and we use some connectors of SQL to gather the data.



EDA
Once we got the data,    we start performing the basic Operations of machine Learning in order to analyze the State of Data. We started  the data preparation steps, which includes: EDA, Feature Engineering, Feature Selection & Extracting methods.
Now, What EDA is? EDA Stands for Exploratory Data Analysis which is a Data Analytics process to understand the data in depth and learn the different data characteristics often with Visualization Techniques. This allows you to get a better feel of your data and find useful pattern from it.
In our case initially when we gather the data we had around 6-7 lacks of rows, and nearly 70 features with us, but when we done with feature selection and feature engineering we had only left with around 30-35 feature, in order to send it to the machine to train the Model.
We were having some Categorical features like Time_Email_sent_Category, Email_type , Email_source_Type, Email_Campaign_type and some Continuous features like Subject_Hotness_Score, Word_Count, Total_Past_Communications and we perform different EDA Techniques like correlation Matrix, Scatterplot, and Visualization Libraries like Matplotlib, Seaborn etc.
From the analysis, we got to know which columns contain the missing values, and the outliers. To detect the missing values, we used Pandas Function, and to identify the outliers we used methods like Boxplot, Z-Score and IQR. And we noted down the features that were having more outliers and missing values. 
Feature Engineering
So, based on the information that we gather in EDA part we perform some operation on the data in Feature Engineering part.
Now, the question arrives what feature engineering is? Basically feature engineering is based on the data that we gather, we do some operation on the data in order to make it model friendly.
Different action we took in order to clean the data, like Imputation techniques, in which we use mean, median, mode in order to fill missing values, we use transformation and scaling approaches to convert the data in equal Scale, and whatever irrelevant features we had in the data we simply drop them after consulting with Higher Authorities.
Missing values differ from categorical as well as continuous values. So the features which are having continuous values we have replace them by using various imputation techniques, But After replacing them with the imputation technique we come to know that our data is getting bias to some particular values and it were impacting badly to the accuracy of the model, so in order to deal with this we use KNN imputer techniques, it use to fill the data by unique values as per the feature similarity unlike imputation technique.
And the features which are having categorical values, we simply replace it with mode value.
While Analysis the data we use boxplot technique to detect the outliers in the data, and then we come to know that we have lots of features which are impacted by outliers, for that we use IQR method.
After done with outliers and missing values, we come to the encoding part, where we perform Label Encoding on features having Ordinal Data, and One Hot Encoding on the features having Nominal Data.
We had Age columns which was quite important feature, but the thing is that it contains lots of missing values and noise, so we had DOB feature from which we derived the new feature Senior Citizen considering the threshold age 60yrs.




Feature Selection
Now we came to the Feature Selection Part, we use different Feature Selection Techniques like Annova Test, chi-square, Test Information Gain etc. in order to find the importance of features and visualized which features are contributing more in order to predict the output. 
We Use Principle Component Analysis to fetch the 25 best Principle Components which were contributing the most to predict the outcome.
Model Building
In Model Building at first we started with Logistic Regression. we got some results but after that we got to know that the Logistic regression was not giving the kind of results that the Client were looking for, so we switched to the next algorithm that is KNN Algorithm, as it has certain advantages over Logistic Regression, as we know KNN is a Non Parametric Algorithm, and It also work on the principle of feature similarity.
But Again, that Algorithm make us disappoint and we unable to get the good accuracy. As it is Distance Based Algorithm it does not perform well on Large Dataset.
Next we move toward Decision Tree, Firstly it gets Overfitted, even after performing the Hyperparameter Tunning we did not get expected result.
Then we switch to our final algorithm which is random forest this act as a project saving algorithm for us this algorithm give accuracy on which our client and we both were Comfortable with.
Benefits your client get from your project?
Benefits are not in terms of Numbers, we have to say like
We reduce the Human Efforts
We Reduces the decision time, before required 10min now they able to take decision in 1 min or 2 min



Achievement:
We Successfully achieve 6-7% cost reduction
Benefits your client get from your project
We Reduces the decision time



DROP FEATURE
Mode of Contact
Aadhar No.
Pan no.
Customer ID
Phone No.
Address 
Name
Customer Type



CONCLUSION

● In EDA, we observed that Email_Campaign_Type was the most important
feature. If your Email_Campaign_Type was 1, there is a 90% likelihood of your Email to be read/acknowledged.

● It was observed that both Time_Email_Sent and Customer_Location were
insignificant in determining the Email_status. The ratio of the Email_Status
was the same irrespective of the demographic location or the time frame the
emails were sent on.

● As the word_count increases beyond the 600 mark we see that there is a high possibility of that email being ignored. The ideal mark is 400–600. No one is interested in reading long emails !

● For modelling, it was observed that for imbalance handling Oversampling i.e. SMOTE worked way better than undersampling as the latter resulted in a lot of loss of information.

● Based on the metrics, XGBoost Classifier worked the best, giving a train score of 89% and test score of 81% for F1 score.



CHALLENGES

● Choosing the appropriate technique to handle the imbalance in data was
quite challenging as it was a tradeoff b/w information loss vs risk of overfitting.
● Overfitting was another major challenge during the modelling process.
● Understanding what features are most important and what features to avoid
was a difficult task.
● Decision making on missing value imputations and outlier treatment was
quite challenging as well.
