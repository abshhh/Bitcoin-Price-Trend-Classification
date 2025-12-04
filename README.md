# Bitcoin-Price-Prediction
**Abstract - This report contains the details about my work on the bitcoin price prediction problem. We have a csv dataset which has features like, “Date”, “Open”,”High”,”Low”, “Close”, “Volume”, “Market Cap”. I have used various classification algorithms and compared their results in this report.**

# Introduction:
In this new digital era, where every enthusiast invests his money in stocks and among which Bitcoin is the most widespread and one of the most valuable digital currencies. So In this scenario it is very important to understand the way bitcoin fluctuates and changes over time. With this we can safeguard our digital investment.

# Dataset:
- Date column- contains dates from April, 2013 to August, 2017.
- Few features like, “Open”, “High”, “Low”, “Volume”, “Market Cap”.
- “Close”, the closing value for the day.
# Methodology:

Preprocessing:
- Added New column “close_pred”. Which is to be used for classification. Here I took a number in the range of separation of 80 to be of one class. This converts the given continuous data to categorical data. With this we are left with 36 different classes.
- I’ve shifted “Close” by 1. This brings the relationship of bitcoin values for two consecutive days. And hence a close value to be predicted depends on close values
of its previous day.
- Converted “Volume” & “Market Cap” from “Object” type to “float” type.
- Converted “Open”, “High”, “Low”, “Volume”, “Market Value” into categorical data using bins. (N_bins = 600).

Classifiers Used:
- Decision Tree Classifier
- XGBoost
- LightGBM
- Random Forest Classifier

Implementation: 
- DTC: 
Decision Tree Classifier is the most widely used Classification Model due to its ability to break complex data of high complexity into smaller branches thus reducing complexity. 
**Due to this ease in the interpretation, we have chosen Decision Tree Classifier as our next model.**

classification report is as follows:

![image](https://user-images.githubusercontent.com/76608418/178116468-56287d7f-2617-4d06-8160-9b6868ca6a38.png)

Y_pred & Y_test graphs: 

![image](https://user-images.githubusercontent.com/76608418/178116512-9e9123d6-2e60-47e3-9d16-f11d097c11c5.png)

- XGB 
XGBoost (Extreme Gradient Boosting), is a gradient boosted decision tree, it provides parallel tree boosting. It is a supervised machine learning algorithm used for relatively large datasets.

classification report is as follows:

![image](https://user-images.githubusercontent.com/76608418/178116542-5044c63a-91d5-4891-9a3a-b371fb9a8c17.png)

Y_pred & Y_test graphs: 

![image](https://user-images.githubusercontent.com/76608418/178116564-33ae98a0-75b7-444b-a471-f36dfa083cea.png)

- LightGBM 
LightGBM is a gradient boosting framework based on decision trees to increase the efficiency of the model and reduce memory usage. 

classification report is as follows:

![image](https://user-images.githubusercontent.com/76608418/178116580-51f04f42-cf2c-4c70-8d72-0f02e4ab2757.png)

Y_pred & Y_test graphs: 

![image](https://user-images.githubusercontent.com/76608418/178116593-eb4fbec0-8923-4eaf-a614-6d0b1d634f27.png)


- Random Forest 
Random Forest Classifier Model creates a set of multiple decision trees from randomly selected subsets of the training set. It then takes the average of all the votes of different trees to finally select the class. The advantage in this method is that the error of one tree will be overshadowed by the other trees. 

classification report is as follows:

![image](https://user-images.githubusercontent.com/76608418/178116636-ab00d421-4575-45b5-a76d-d5d958ef18f5.png)

Y_pred & Y_test graphs: 

![image](https://user-images.githubusercontent.com/76608418/178116647-24c2f88e-e1d9-4e9b-9fbc-d89355c03188.png)

# Classification Accuracy
- DTC              - 62.740
- XGB              - 61.884
- LightGBM         - 62.740
- Random Forest    - 61.456
# Report

