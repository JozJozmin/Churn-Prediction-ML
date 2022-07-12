# Churn-Prediction in ML
Understanding Problem Statement : Decreasing the Customer Churn is a key goal for any business. Predicting Customer Churn (also known as Customer Attrition)
represents an additional potential revenue source for any business. Customer Churn impacts the cost to the business. Higher
Customer Churn leads to loss in revenue and the additional marketing costs involved with replacing those customers with new ones.
In this challenge, as a data scientist of a bank, you are asked to analyze the past data and predict whether the customer will churn or
not in the next 6 months. This would help the bank to have the right engagement with customers at the right time.

Objective : Our objective is to build a machine learning model to predict whether the customer will churn or not in the next six months

Data analysis and interpretation : 
<li>The provided data set includes both the train and test data set.
<li>The train data set consists of 6650 rows and 11 attributes without null values. The column includes age, gender, income, balance, vintage etc. in which 6 are numeric columns including the target column and 5 are object columns. Apart from this one attribute called ID which is specific to a customer and not required for this prediction. 
<li>The target column contains 1537 ones which indicate a customer is likely to churn and 5113 zeros indicate a customer not likely to churn. This unbalanced    unique count of values in target class indicates this is an unbalanced dataset.
<li>For this problem the input needs to be assigned to specific classes. Hence it is a classification problem.
<li>In order to understand and explore the relationships between different variables in the dataset I have performed exploratory data analysis and visualization see how they are related to the Is_Churn attribute (target column).<br/>Some of my findings are:<br/>
	1. </li> Through carefully analyzing the visualizations I found that except gender remaining all columns have a certain impact on the target columns.<br/>
	2. </li> In the credit category, the poor category has the highest impact on target data compared to the other two good and average categories.<br/>
	3. </li> In the income category 5L-10L and 10L-15L have more customers who are likely to leave.<br/>
	4. </li> The people who are between 30-60 are more likely to leave compared to other age categories.<br/>
	5. </li> And the customers who are earning below 1.5million are more likely to leave the company compared to those who earn more than 1.5 million.<br/>
	6. </li>Through analyzing the boxplot for balance and age category I found the presence of outliers in the balance and age data.<br/>
					
<br/>Some of the methods that I done to make the data clean and more perfect includes:<br/>
	<li> Oversampling <br/>
	<li>Scaling of numeric columns <br/>
	<li>Removal of outliers in Balance and Age attributes through binning. But it didn’t work well as I expected in my data due to decreasing the overall accuracy <br/>
	<li> One hot encoding of categorical variables<br/>
Since it is a categorical problem I have approached various models. And I got more accuracy in logistic regression. In order to improve the model I done hyper 			parameter tuning and feature selection <br/>
<li>In feature selection I used all the attributes which have regression coefficients greater than 0.011 in which I got higher overall accuracy.<br/>
<li> In hyper parameter tuning by RandomizedSearchCV, I got the best parameter for logistic regression  {'penalty': 'l2', 'max_iter': 400, 'C': 170}<br/>
<li>The overall accuracy I got from logistic regression model is 58.65%<br/>
<br/> The top score for this competition is 0.6249118684 <br/>
	
	
<br/> link for leader board of the competition is : https://datahack.analyticsvidhya.com/contest/job-a-thon-march-2022/#LeaderBoard <br/>
	
# Result:	
Private Leaderboard : 90
Public Leaderboard  : 105	

