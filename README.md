# Comparing Classifiers on Banking Data

[V1.0 Jupyter Notebook Link][https://github.com/sjt80/comparing-classifiers/blob/main/comparing_classifiers.ipynb]

### Executive Summary

In this practical application, our goal is to compare the performance of the following classifiers: namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines. We will utilize a dataset related to marketing bank products over the telephone.

### Dataset Overview

In this practical application, our goal is to compare the performance of the following classifiers: namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines. We will utilize a dataset related to marketing bank products over the telephone.

To gain a better understanding of the data, read the information provided in the UCI link above, and examine the Materials and Methods section of the paper.

As explained in the accompanying paper: The dataset collected is related to 17 campaigns that occurred between May 2008 and November 2010, corresponding to a total of 79354 contacts. During these phone campaigns, an attractive long-term deposit application, with good interest rates, was offered. For each contact, a large number of attributes was stored and if there was a success (the target variable). For the whole database considered, there were 6499 successes (8% success rate).


### Findings

1. Influential Factors 

    Using Logistic Regression we were able to extract the coefficients and order them in terms of importance.  Houses without a loan came out as the primary feature when looking for depositors.
    It would also appear that being contacted in the month of October had a negative correlation on outcome.  This would need to be further verified.
    

2. Models and Performance

    Unlike Linear Regression or other non classification models we cannot just go for the model that has the best score.  In our case we have unbalanced data so Logistic Regression is a great model as not only can it handle imbalanced data well but it can also provide results that are very interpretable; we get coefficients that define the importance of the input features and the output is a continuous probability of the class.  SVM is also another good model however calculation time was a limiting factor.  The other two models; KNN and Decision Trees do not handle unblanced data as well however did perform to a satisfactory level for our puprose.


### Conclusion

For our case there is no catastrophic outcome if we wrongly predict a small amount of false positives (aka we predict a person will open a saving account but they don't). A low precision and high recall model is recomended or in other words we can have an optimistic classifier. On the other hand if we have limited sales personel and or a very costly sales follow up process we would want the inverse and have high precision and low recall. In our case we are using this data to trigger sales call activities; in this case the better tradeoff is to capture all potential customers reducing the amount of False negatives, and maybe have a few more False positives. Thus we can further optimize our model by selecting a threshold on the lower end say 0.4 to acheive the above.
