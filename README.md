# SalesForce_LogisticRegression
Propensity Modeling / Logistical Regression Example to Forecast Client Engagement Probabilities

Salesforce allows you to add field to assist sales associates with their business development efforts. 

Formula fields can be used to compute a probability that a particular client will do something and allow a simple report to be used to direct your employees to action.

If you would like to leverage your past data to predict future events read on or watch <a href="http://www.youtube.com/watch?feature=player_embedded&v=c2WXsM-6M5k
" target="_blank">YOUTUBE Tutorial</a>: 




![alt text](https://github.com/SententiaInc/Salesforce_LogisticRegression/blob/master/SalesforceExample.PNG "Propensity Modeling")

Historical data must be structured in the following manner. 


![alt text](https://github.com/SententiaInc/Salesforce_LogisticRegression/blob/master/sampledata.PNG "Propensity Modeling")

`((EXP(
Beta +
IF( wcBeta * wasCalled__c, 1, 0) +
IF( raBeta *  receivedAd__c, 1, 0) + 
IF( pcBeta * priorCustomer__c, 1, 0) ))
/ (

1+ EXP(Beta +
IF( wcBeta * wasCalled__c, 1, 0) +
IF( raBeta *  receivedAd__c, 1, 0) + 
IF( pcBeta * priorCustomer__c, 1, 0) )))
)
* 100`


![alt text](https://github.com/SententiaInc/Salesforce_LogisticRegression/blob/master/ColumnDef.PNG "Propensity Modeling")


