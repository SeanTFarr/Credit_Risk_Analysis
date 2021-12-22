
<img src=Images\credit_risk.jpg>

## Overview of the loan prediction risk analysis: 
The purpose of this analysis is to evaluate the performance of 6 machine learning models and make a written recommendation on whether they should be used to predict credit risk.

## Results: 
Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

1. ### Naive Random Oversampling
This method is to generate new samples by randomly sampling with replacement the current available samples.

<img src=Images\Naive_Random_Oversampling.jpg>


2. ### SMOTE Oversampling
 The Synthetic Minority Oversampling Technique (SMOTE) generates new samples in by interpolation. That is, for an instance from the minority class, a number of its closest neighbors is chosen. Based on the values of these neighbors, new values are created.

<img src=Images\SMOTE_Oversampling.jpg>

3. ### Undersampling
Cluster centroid undersampling is an algorithm that identifies clusters of the majority class, then generates synthetic data points, called centroids, that are representative of the clusters. The majority class is then undersampled down to the size of the minority class.

<img src=Images\Undersampling.jpg>

4. ### Combination (Over and Under) Sampling
SMOTEENN combines the SMOTE and Edited Nearest Neighbors (ENN) algorithms. It first oversamples the minority class with SMOTE, then cleans the resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong to two different classes, that data point is dropped.

<img src=Images\Combination_Sampling.jpg>

5. ### Balanced Random Forest Classifier
A balanced random forest randomly under-samples each boostrap sample to balance it.

<img src=Images\BRF.jpg>

6. ### Easy Ensemble Adaboost Classifier
The classifier is an ensemble of AdaBoost learners trained on different balanced boostrap samples. The balancing is achieved by random under-sampling.

<img src=Images\EEC.jpg>

## Summary: 
Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.