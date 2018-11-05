# SalesForce_LogisticRegression
Propensity Modeling / Logistical Regression Example to Forecast Client Engagement Probabilities

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
