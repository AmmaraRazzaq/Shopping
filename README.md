# Machine Learning Model to Predict Online Customer Behavior
Not all users who visit a shopping website end up purchasing. It can be important to predict whether a user will end up purchasing or not, maybe to place targeted ads or give discount 
if the website can predict that user will likely not purchase anything. How can a user's behavior be predicted? The answer is by using a machine learning model. 

In this project, a K Nearest Neighbor (KNN) classifier is trained to predict whether a user will purchase anything or not, hence it is a binary classification task. A KNN Classifier
is a memory based classifier where it memorizes the dataset and look at the labels of K nearest neighbors and selects the target label by a majority vote.  

### Dataset
The data set consists of 12000 user sessions from a shopping website. Each row in dataset represents a user session and consists of useful information such as, how many pages a 
user has visited, what web browser they used, is it a weekend or not, etc.

This dataset is taken from [CS50's Introduction to Artificial Intelligence with Python, Harvard University OpenCourseWare](https://cs50.harvard.edu/ai/2020/projects/4/shopping/)

### Libraries Used
* Pandas, Numpy, Scikit Learn

## 1. Data Cleaning/Encoding
Machine learning models require data in numerical form. Hence, categorical data is converted to numerical data using label encoding. For example, months that are given in string form
as ['Jan','Feb','Mar'...] are encoded into numerical form as [1,2,3 ...].

## 2. Extract Features and Split Data 
1. Features and target labels are extracted and then split into training and test data by random splitting. 
2. 75% data will be used for training and 25% data will be kept for testing.

## 3. Train and Evaluate KNN Classifier
1. The classifier is trained for different values of k ranging from 1 to 20.
2. Training score and test score of the model for different values of k are plotted.
3. The accuracy plot shows that for k=1 the model is overfitting as the accuracy on training data is maximum but on test data is very low.
4. For higher values of k, the model is underfitting as the accuracy on both training and test data is low.
5. The model generalizes well for k=8, as the accuracy on test data is maximum and accuracy on training data is optimal. 

# Result
Model is 85.4% accurate with k=8 neighbors. 
