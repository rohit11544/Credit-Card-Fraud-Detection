# credit-card-Fraud-Detection
### LIBRARIES
* numpy
* pandas
* seaborn
* matplotlib
* sklearn

### DATA SET
* This dataset contains around 290,000 credit card transaction details.
* There are 32 features in total for the dataset including the time when the transaction happened and the amount.
* According to the organization restrictions the name of the features are kept confidential.

### CLEANING DATA
there are not null value in the data set to fill

### FEATURE ANALYSIS
There are too many features so to prevent from overfitting unnecessary features are dropped. By plotting the heatmap and FacetGrid plots , the features that are less correlated to the class are dropped.

-> The features V1, V3, V5, V6, V7, V9, V10, V12, V13, V14, V15, V16, V17, V18, V23, V24 and Time are not correlated to the Class.

#### SPLITTING DATA
As they are around 290,000 the data set was splitted into 90% train 10% test sets.

### TRANING
This data is trained on several models :  
* XGBoost
* SVM
* RandomForest
* k nearest neighbour 
* Logistic regression

### EVALUATION METRIC
=> As this data set contains very few exaples of class 1 (around 500) it is not a good idea to use accuracy as evaluation metric.

=> It is very important to detect the fraud transaction so the there are 2 evaluation matrics used 
1) model with recall for class 1 should be minimum 80%
2) model with highest accuracy

### MODEL COMPARISON

| MODEL        | Class 1 RECALL | ACCURACY |
| -------------|:--------------:| --------:|
| XGBoost      | 0.69           |  99.95%  |
| SVM          | 0.64           |  99.94%  |
| RandomForest | 0.82           | 98.45%   |
| k nearest neighbour |  0.69   | 99.95%   |
| Logistic regression |  0.85   |  97.31%  |

### BEST MODEL

# RandomForest WITH 82% RECALL AND 98.45% ACCURACY
