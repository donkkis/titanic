# titanic

My entry to the Kaggle Titanic Survivorship prediction competition.

Data soure: https://www.kaggle.com/c/titanic

The prediction task is to fit a binary classification model to the data. The predictors are:

Variable | Description
---------|------------
pclass   | Ticket class 1 = 1st, 2 = 2nd, 3 = 3rd
sex      | Sex Male/Female
Age      | Age in years
sibsp    | # of siblings / spouses aboard the Titanic
parch    | # of parents / children aboard the Titanic
ticket   | Ticket number
fare     | Passenger fare
cabin    | Cabin number
embarked | Port of Embarkation C = Cherbourg, Q = Queenstown, S = Southampton

The binary variable to be predicted is:

survival: Survival 0 = No, 1 = Yes

Currently, we get a 0.82 f1 score in the training set utilising a Support Vector Machine classifier with hyperparameter optimization (grid search).

Things to try in order to improve the score:

* Do some further feature engineering, eg. the cabin number might encode some useful info, as well as the title in the person's name (Mr, Mrs, Miss etc)
* Try a different classifier. E.g. XGBoost and random forest algorithms have reportedly worked well for other people in this problem https://www.kaggle.com/ldfreeman3/a-data-science-framework-to-achieve-99-accuracy
* Do random search in the hyperparameter space near the "currently optimal" values  
