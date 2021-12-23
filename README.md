
<img src=Images\credit_risk.jpg>

## Overview of the loan prediction risk analysis: 
The purpose of this analysis is to evaluate the performance of 6 machine learning models and make a written recommendation on whether they should be used to predict credit risk.

---
---

## Results: 

For each of the 6 models, these steps were followed: 
- resample the dataset 
- view the count of the target classes 
- train a logistic regression classifier
- calculate the balanced accuracy score 
- generate a confusion matrix
- generate a classification report
---

1. ### Naive Random Oversampling
This method is to generate new samples by randomly sampling with replacement the current available samples.

<img src=Images\Naive_Random_Oversampling.jpg>

Naive Random Sampling produced:
- Balanced Accuracy Score 65%
- "High Risk" sensitivity 68%
- "Low Risk" sensitivity 63%
---

2. ### SMOTE Oversampling
 The Synthetic Minority Oversampling Technique (SMOTE) generates new samples in by interpolation. That is, for an instance from the minority class, a number of its closest neighbors is chosen. Based on the values of these neighbors, new values are created.

<img src=Images\SMOTE_Oversampling.jpg>

 SMOTE Oversampling produced:
- Balanced Accuracy Score 64%
- "High Risk" sensitivity 60%
- "Low Risk" sensitivity 68%
---

3. ### Undersampling
Cluster centroid undersampling is an algorithm that identifies clusters of the majority class, then generates synthetic data points, called centroids, that are representative of the clusters. The majority class is then undersampled down to the size of the minority class.

<img src=Images\Undersampling.jpg>

 Undersampling produced:
- Balanced Accuracy Score 49%
- "High Risk" sensitivity 54%
- "Low Risk" sensitivity 43%
---

4. ### Combination (Over and Under) Sampling
SMOTEENN combines the SMOTE and Edited Nearest Neighbors (ENN) algorithms. It first oversamples the minority class with SMOTE, then cleans the resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong to two different classes, that data point is dropped.

<img src=Images\Combination_Sampling.jpg>

 Combination/SMOTEENN Sampling produced:
- Balanced Accuracy Score 66%
- "High Risk" sensitivity 73%
- "Low Risk" sensitivity 59%
---

5. ### Balanced Random Forest Classifier
A balanced random forest randomly under-samples each boostrap sample to balance it.

<img src=Images\BRF.jpg>

 Balanced Random Forest Classifier produced:
- Balanced Accuracy Score 79%
- "High Risk" sensitivity 70%
- "Low Risk" sensitivity 87%
---

6. ### Easy Ensemble Classifier
The classifier is an ensemble of AdaBoost learners trained on different balanced boostrap samples. The balancing is achieved by random under-sampling.

<img src=Images\EEC.jpg>

 Easy Ensemble Classifier produced:
- Balanced Accuracy Score 93%
- "High Risk" sensitivity 92%
- "Low Risk" sensitivity 94%
---
---

## Summary: 
The algorithm that performed best on this dataset was clearly the Easy Ensemble Classifier, as no other had an accuracy score or recalls over 80%. With Ballanced accuracy of 93% and the high and low risk within 1% of that, it does predict well. With some room for improvement, futher research into additional machine learning models is suggested to see if we can get better results.