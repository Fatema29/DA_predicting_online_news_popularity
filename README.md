# Online News Article Popularity Prediction
## Introduction:
Because of the easy access of the internet, the online news has become very popular among the people of recent days. It is now a very common trend to share online news if anyone finds it interesting or valuable. Based on this sharing number we can judge which news is now trending or popular among people. This number of sharing depends on several features. Using a huge dataset, provided by UCI Machine Learning Repository, with about 39,797 articles and total 61 attributes, an analysis was done to find the best model and features to predict the popularity of any news article even before being published. Random Forest Regression Model gave promising performance for this dataset and for the classification model, Adaboost showed a significant performance of 67% accuracy.

## Development Plan:
Step 1: The first step will be to read and load the dataset

Step 2: For further processing it is important to preprocess the raw data and turn them into an understandable format. So after loading the dataset, the next step will be the data preprocessing.

Step 3: The I will implement different learning techniques such as Logistic Regression, Random Forest Regression, Linear Regression. For classification I will implement KNN, Neural Network, Random Forest, AdaBoost

Step 4: The I will make a comparison among those techniques to find the best model and features to predict the popularity of certain articles which can be used for different online news companies to estimate the value of their articles before publishing.

## Data Acquisition:
The dataset that I have chosen is mainly provided by UCI Machine Learning Repository. This dataset has total 61 attributes, among those 58 predictive attributes, 2 non-predictive, 1 goal field. This dataset is composed of 39797 instances which means it has 39797 articles which were taken from Mashable (www.mashable.com). 

## Data Preprocessing:
In this step I have done these things to preprocess the data,

Data Cleaning: This dataset contains two non-predictive features, so at first these two non-predictive features were removed. Then it was checked if there were any null values, fortunately the dataset was clean.

Removing Recent Articles: The recent articles where time delta is less than 1 month were discarded since the convergence for those articles was not reached yet. 

Excluding Outliers: Outliers were being excluded from target column using Z-score method. In this approach,  it removes the  outlier  points  by  eliminating  any  points  that were greater than (µ+ kσ) and less than  (µ-kσ), for this project k=2 was chosen. 

Normalizing Features:The numerical features were then normalized using Minmax normalization technique. In this technique, the data is scaled in between 0 and 1.Data normalization is done to make the data more understandable and to reduce the redundancy throughout the dataset.

Dimensionality Reduction: This technique is used for reducing the number of features in a dataset while dealing with lot of features. PCA (Principal Component Analysis) is one of the dimension reduction technique which is used to down-sample high-dimensional datasets. It reduces the dimensionality and find a new set of features called component. These components are composed of original features but uncorrelated with each other. First component has the highest possible variability in the dataset, 2nd component has second high variability and so on. For this project, the number of component is set to 5.

Feature Selection: Implementing ‘feature_importances’ technique reduces the features. This technique allows to build a list by the importance of  all the features in a form of probability. So from that list we can discard the less important features and observe how it affects on the performance. 

## Model Implementation:
In this project we employed the Scikit Learn Library to implement the models.

For the regression analysis I have implemented three models, named Random Forest, Linear Regression, Logistic Regression. 

For the classification analysis I have explored Random Forest, AdaBoost, KNN, NN these 4 models.

The dataset was split into two separate parts, training and testing. 80% of the data used as training set and 20% of data used as testing set. This separation was made for each of four datasets. Then the model was implemented onto these to observe the difference of performance.

## Conclusion:
Using a dataset of 39,000 instances with 61 features I implemented different models to predict the popularity of online news articles before being published. After implementing several data mining techniques I came to a conclusion that if the outliers can be removed from the dataset it shows a significant performance improvement. And implementing dimensionality reduction and the feature selection technique, it does not improve the accuracy rate but it does reduces the computational time noteworthy. Among several models, the AdaBoost was the one who showed the best performance.
