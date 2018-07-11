# Weekly Report
### Abhijeet Gokar -11 July 2018

# Problem Statement
To completely perform SVM and Random Forest on Open Datasets Indian Pines , Pavia University and Kennedy Space Center.

# Tasks

* Implementing GridSearchCV() (and k-fold cross validation) to find the optimal hyperparameters in SVM and Random Forest Classifier.
* Observe the nature of Discriminant functions in SVM
* Perform k-fold cross validation selectively on the data
* Dump/Pickle the optimal Model and indices of the class-wise segregated dataset into binary files , so that it need not be retrained again for a different dataset.

## Code Implementation

* Using SVM and Random Forest, the first task was to see the accuracy metrics by training the classifier functions by train test splitting the data. 
'''
$ linear_p = svm.SVC(C=1 , kernel='linear',cache_size=1000)
'''
'''
$ i_RF = RandomForestClassifier(max_depth=4, random_state=42)
'''

* The main objectives here are to overcome the random splitting of data which is not suited for the hyperspectral datasets , and to see the ideal train test split ratio in order to minimize the variance in accuracy.

* The next step to fine tune the training is to use k-fold cross validation and gridsearch to search for the optimal parameters.

'''
 from sklearn.model_selection import GridSearchCV
 GridSearchCV()
 '''


# Evaluation
* The classical methods are good only when the hyperparameters are fine-tuned, and the data is trained properly. 

* This method will not be good for original remote sensing data as the boundaries or rules cannot be learned properly from the data, and neural network models have to be used to do classification.

