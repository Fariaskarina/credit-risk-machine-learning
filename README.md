![creditrisk](https://user-images.githubusercontent.com/84626126/193157220-7d96567c-892a-4afa-8bbf-7e680c3128b3.jpg)
# <h1 align="center"> Credit risk with machine learning </h1>
![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=%20Concluded&color=GREEN&style=for-the-badge)


Credit risk prediction with Machine Learning algorithm using Python.

### Introduction
This code uses users' credit history to predict whether or not they have paid the requested loans. Data on age, income, status of loans already made are related to make the prediction if the person has paid or not paid the loan, and thus define a standard for making a prediction.

Please visit my LinkedIn and learn more about my work: https://www.linkedin.com/in/karina-farias-10a15a17a/

### How to build and run the preprocessing notebook locally

1. Clone the source code
```
https://github.com/Fariaskarina/credit-risk-machine-learning.git
```

2. Install libraries

You can do this manually:
```
pip install pandas numpy seaborn matplotlib plotly sklearn
```
Or using:
```
  pip install -r requirements.txt
```

### Dataset
The Kaggle Platform user history Datasheet was used:
[Credit Risk Dataset](https://www.kaggle.com/datasets/laotse/credit-risk-dataset)

### Results and Discussions
33% of the data was used for testing and the rest for training. 
Of the 10752 data used for testing, 8830 are from customers not able to receive credit, and 1922 from eligible customers. 
Of the 21829 data for training, 18006 are from customers not able to receive credit and 3823 from eligible customers.
1= eligible for credit
0= not eligible for credit

To evaluate the model, four machine learning classifiers were used:
k-Nearest Neighbors (kNN), Support vector machine (SVM), Decision Tree and Ensemble Bagged Tree

And six metrics:
Accuracy, Precision, Recall, F1 score, macro avg and weighted avg.

The first classifier, k-NN, provided the following results:

Accuracy (hit rate):
Test
80% hit, and out of 8830 non-eligible customers, the model got 8474 right and 356 wrong, and out of 1922 eligible customers, the model got 97 right and 1825 wrong.
Training
86% hit, and out of 18,006 non-eligible customers, the model got 17,989 right and 17 wrong, and of 3,823 eligible customers, the model got 839 right and 2,984 wrong.

Precision (among those predicted as positive, what is the proportion of correct answers?)

Recall (among the real positives, what is the correct proportion?)

F1score:
is the harmonic mean between precision and recall (balance between the two metrics). The f1-score is higher when there is a “middle ground” between precision and recall.

Macrof1: average of the f1 of the classes (useful when the classes are unbalanced).

The k-NN classifier gave good results when we related the proportion of metric values between test and training. The Decision Tree and Ensemble Bagged Tree classifiers performed well in training, but were far from test data, which means that if the model is able to predict training data very well, but is poor at predicting test data , we have an overfitting problem :[ . 
So, let's consider the accuracy of the first classifier, 86%.

![image](https://user-images.githubusercontent.com/84626126/195333022-27c4ecd7-f513-4faa-8fb1-b3d29ace270b.png) ![image](https://user-images.githubusercontent.com/84626126/195332977-422a42e7-9bca-41d6-b019-76deac86d224.png)
