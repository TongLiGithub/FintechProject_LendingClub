
# Financial Technology Project: Lending Club

In this project, I used borrowers' social and economic information to predict their loan status ("fully paid" or "charged off"). The data are downloaded and scraped from [Lending Club](https://www.lendingclub.com/info/download-data.action). The project has three parts. 

### Part I Data Preparation

** This part includes three sections:**    
* Fetch current and historical data (2014 data) from Lending Club
* Unify feature formats of current loans (to lower case) and 2014 loans (remove underline in feature name)
* Find common features of current and 2014 loans, keep only the common features, "loanstatus", and "issued" for 2014 loans and save to loan_2014.csv     

I want to use the model not only to predict the historical loan status, but also in the future. Therefore, only the common features in both historical data and current data were used to train the model. There are some unique features in 2014 data, which may also be important. But since they are not in the current data, they cannot be used to predict the loan status in the future.  

### Part II Exploratory Data Analysis

** This part includes four sections:**    
* Find out null features (in which all values are null). For other features, find out categorical and numeric features and separate them    
* Examine categorical features one by one, consider how to work on them in the next step
* Explore the relationship between categorical features and the target (loanstatus) by plots
* Explore the distribution of numeric features with histogram. For the ones which do not spread out, look into their relationship with the target (loanstatus)    

### Part III Modeling

** This part includes five sections:**    
* Select data: Get rid of null features, split train and test datasets in terms of issued time, select data with term of 36 months
* Feature engineering and cleaning
* Train a preliminary XGBoost model
* Tuning hyperparameters with Bayesian Optimization
* Find out the most important predictors based on the tuned model 

** Note: ** Historical data file is too large (more than 100 MB) and cannot be uploaded on to github
