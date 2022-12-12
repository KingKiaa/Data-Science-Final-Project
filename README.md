# Data-Science-Final-Project
DATA 6150 Final Project and Description

Name = 'Kia Aalaei'
Project = 'Binary Rice Classification'
Dataset = 'https://www.kaggle.com/datasets/seymasa/rice-dataset-gonenjasmine'


import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
from sklearn.svm import LinearSVC
from sklearn.model_selection import cross_val_score
from sklearn.metrics import confusion_matrix
from sklearn.metrics import classification_report


import seaborn as sns
rice = sns.load_dataset('RiceGonenandJasmine')

rice.tail()

rice.info()

#Features is x and lables are y
X = rice.drop(['id','Class'], axis = 1)
X.head()

y = rice['Class']
y.head()



sns.pairplot(rice)


from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split( X, y, test_size = 0.33)
#67% of dataset to training and 33% to testing
#Splitting dataset into training and testing



#Linear SVC model
lsvc = LinearSVC(dual=False)
print(lsvc)


#fitting the model on training data
#training score can be checked
lsvc.fit(X_train,y_train)
score = lsvc.score(X_train,y_train)
print("Score: ", score)



#can also use cross validation methode to check training score
cv_score = cross_val_score(lsvc, X_train, y_train, cv=10)
print("CV average score: ", cv_score.mean())



#now I can predict my test data by using model
ypred = lsvc.predict(X_test)
confusionmatrix = confusion_matrix(y_test, ypred)
sns.heatmap(confusionmatrix, square=True, annot=True, cbar=False, cmap='YlGnBu') #flag, YlGnBu, jet
plt.xlabel('predicted value')
plt.ylabel('true value');
print(confusionmatrix)



cr = classification_report(y_test, ypred)
print(cr)


#SGD Classifier with a success rate of:
#PRECISION 0.9828219057407136 
#RECALL 1.0 
#F1_SCORE 0.9913365420214736






