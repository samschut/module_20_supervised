# module_20_supervised
Overview
In this module a credit dataset is used to plug into different machine learning tools to determine the probability of getting a loan defaulted on or not. The data showed some basic information about a client including loan size, interest rate, borrower income, debt to income, num of accounts, derogatory marks, and total debt. Based on these there was also a column that had the loan status marked as 0 or 1. 0 meaning they were currently healthy within the loan and 1 being they defaulted. We can look at the other columns and use them as variables within machine learning tools in order to predict if that number is going to be a 0 or 1 based on this dataset. 
One issue with this dataset is it is very unbalanced. This means there are far more instances of a 0 being present than a 1. This can create some overlery optimistic models. I did scale the data in order create a balanced 'weight' for each variable in order to create better models. I used a LogisticalRegression and Adaboost to compare and contrast. The logistical model is good in this case because it is a binary outcome and they generally do well with fitting with the data, however, there is a high chance of overfitting. Adaboost is good about minimizing overfitting while historically having great models. 

Logistical regression
-Accuracy: is at 99% which is nearly perfect. the ROC is also at 1.00 which is impossible in the real world, suggesting an overfit model.
-Precision: 87% shows a higher chance of false positives, meaning that it thinks more people will default when they would not.
-Recall: 95% shows it is good at not falsely predicting that someone will not default when they actually will. 
-F1-score: 91% this is a pretty good overall score because life is not perfect, however, getting in the 90s is generally good from a financial standpoint because usually there are things set up in place for some room for error. A life is not necessarily on the line here so to me it is acceptable.

AdaBoost
-Accuracy: 100% indicates this is actually overfit ironically
-Precision: 87% shows the same score as the logistical regression
-Recall: 99% also almost perfect, outperforming the logistical regression model
-F1-score: 93%   this is not much better, only 2% better than the logistical regression

I don't think I would choose either of these to stake my career on. I really think a larger dataset should be used and try to get a better balanced dataset while we are at it. This may be why the precision was not better in either of the models because there was not a lot of data to set this up better. I would think false positives could be poor business to a lending company because a loss of revenue stems from this. Generally, when someone defaults on a loan, there is still a posibility of money to be made from that because bill collection agencies will purchase these and make the calls to get some money from those who have defaulted. There are also insurances to be purchased for higher risk individuals that prevent the lending company from any kind of risk. 
