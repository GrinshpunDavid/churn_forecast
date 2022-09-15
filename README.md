## Project Description
The telecom operator Interconnect would like to be able to forecast their churn of clients. 
If it's discovered that a user is planning to leave, they will be offered promotional codes and special plan options. 
Interconnect's marketing team has collected some of their clientele's personal data, 
including information about their plans and contracts.

### Data Description
The data consists of files obtained from different sources:

* contract.csv — contract information
* personal.csv — the client's personal data
* internet.csv — information about Internet services
* phone.csv — information about telephone services
* In each file, the column customerID contains a unique code assigned to each client.

**The contract information is valid as of February 1, 2020.**

### Solution Report:
a. Steps performed:
- Exploratory Data Analysis
- Feature engineering (address class imbalance)
- train/test/(validation) split
- Hyperparameter tuning
- Testing your final model on the test set

b. Difficulties encountered:
- Data leakage, removed the date and keped only the contract_duration.

c. Key steps:
- OHE the categorical data
- Turning yes/no columns to uint8 for faster calculations
- Fix class imbalance using imblearn.over_sampling and under_sampling

### Results:
- test 'roc_auc' = 0.93 using "CatBoostClassifier".
