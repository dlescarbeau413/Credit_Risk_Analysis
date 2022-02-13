# Credit_Risk_Analysis

Overview of analysis:

For this module, we used different techniques to train and evaluate unbalanced classes. To do this we used sklearn and imbalanced learn libraries to build and evaluate the models using resampling. We used a variety of approaches to predict credit risk that included oversampling data, undersampling data, a combination of both using the SMOTEENN algorithm. Afterwards, we compared two new machine learning models that reduced bias which were RandomForestClassifier and EasyEnsembleClassifier to predict credit risk as well. 

Results:

- The first method we used was the RandomOverSampler with this algorithm, we ended up getting an accuracy score of 64.6%. We can see in the classification report, that the precision for high risk is low around 1% and the low risks were 100% predicted true. When we look at the recall or sensitivity, we can see that 71% of high-risk applicants were likely predicted and 58% low risks were predicted. 


![](Resources/RandomOS%20acc_score.PNG)
![](Resources/RandomOS%20cm.PNG)
![](Resources/RandomOS%20cr.PNG)

- When we used the SMOTE Oversampling method we came to similar conclusions when it came to the accuracy score and the precision and sensitivity. This model provided us with an accuracy score of 65.8%. The precision for the SMOTE algorithm for high and low risk applicants were the same as the RandomeOverSample method. However, the recall for each of the categories were closer than in the previous test. We can see that high risk applicates were at 63% correctly predicted and low risk applicants were at 68% correctly predicted. The percentage was down for the high-risk applications and the low-risk percentage was higher.



![](Resources/SMOTEOS%20acc_score.PNG)
![](Resources/SMOTEOS%20cm.PNG)
![](Resources/SMOTEOS%20cr.PNG)


- The next method we used was an undersampling algorithm. We found that the accuracy score for this algorithm had the lowest accuracy score out of all the algorithms used at 54.4%. We see however that the recall for the high risk applicated is correctly predicted at a rate of 69% and 40% of low-risk applicants were predicted. 



![](Resources/undersampling%20acc_score.PNG)
![](Resources/undersampling%20cm.PNG)
![](Resources/undersampling%20cr.PNG)



- The combination of undersampling and oversampling produced an accuracy score of 63.6%. This method produced a recall of 68% for the high-risk applicant category and 59% for the low-risk category. Which with these numbers, it is similar to the previous undersampling method. Right away, I would throw out the undersampling algorithm and the combination algorithm. 



![](Resources/combo%20acc_score.PNG)
![](Resources/combo%20cm.PNG)
![](Resources/combo%20cr.PNG)


- With the BalancedRandomForestClassifier, we see that our accuracy score jumps up from a previous high of 65.8% (SMOTE Oversampling method), all the way up to 78.8 percent with the random forest. We can see that the recall for high-risk applicants don’t jump as significantly up to 70% but we do see that the low-risk applicants that are correctly predicted does go up to 87% which is a substantial jump from 68% (SMOTE Oversampling).



![](Resources/brfc%20acc_score.PNG)
![](Resources/brfc%20cm.PNG)
![](Resources/brfc%20cr.PNG)

- The algorithm with the best results came from the Easy Ensemble Adaboost Classifier algorithm. With this algorithm, the boosting is trained until the error rate is minimized. We can see how well it works right away with the accuracy score which is 93%. The recall for high-risk applicants is at 92% correctly predicted and the low risk applicated sitting at 94% correctly predicted. With these numbers you can see that this is the best algorithm used from the others by far. The highest accuracy score before we ran this algorithm was 78% with our Random Forest Classifier. However, when we ran the Adaboost Classifier, we were able to reach an accuracy score of 93%.



![](Resources/boost%20acc_score.PNG)
![](Resources/boost%20cm.PNG)
![](Resources/boost%20cr.PNG)



Summary:



When training and testing our data on high risk and low risk applicants we see that there are similarities between the Oversampling, undersampling and combination algorithms when it comes to our results. However, when we use the Random Forest Classifier and Ensemble Adaboost Classifier algorithm we see a vast improvement in our results. 


However, the most important information that we want to look at is in the classification report. Throughout all of our tests, we see a relatively low precision when it comes to predicting the high-risk applicants. The highest precision when it comes to our data is when we run the Easy Ensemble Adaboost Classifier with a precision of 9%. We also see that the sensitivity for high-risk applicants is at 92% which is pretty close to almost perfectly classifying the high-risk applicants. However, I cannot recommend using any of these models for the bank to use when determining credit risk due to the low precision rate we see throughout our analysis.
