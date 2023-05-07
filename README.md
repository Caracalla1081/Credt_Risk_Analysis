# Credt_Risk_Analysis
## Overview of the Analysis
Evaluating who is and is not a good cancidate to loan money to has historically been one of the toughest aspects of operating a lending company. As an employee at the credit lending company Fast Lending they are of the belief that one way to imporve their identification of credit worthy applicants is by utilizing machine learning.

I am to assist the lead data scientist, Jill, in creating several machine learning models that will predict an applicant's credit risk, and then evaluate each algorithim's performance to determine which one; if any, can be used by the company moving forward.

## Results
### RandomOverSampler Algorithm
![RandomOverSampler](https://github.com/Caracalla1081/Credt_Risk_Analysis/blob/8a6f5b3bbe609473b9b339935ce48205112d02f4/Images/RandomOverSampler%20Algorithm.png)
- Balanced Accuracy Score: The balanced accuracry score of .67 can be considered marginal at prediciting who is and who is not at a worthy candidate for credit lending, meaning the "low-risk" classifications are unreliable.
- Precision Score: The precision score of .01 to classify "high-risk" and score of 1 for classifying "low-risk" indicates that there are a large amount of false positives for "high-risk", meaning the classification of "low-risk" is unreliable.
- Recall Score: The recall score of .75 for "high-risk" prediction indicates a good ability for the model to classify the "high-risk" samples, but is "bad" at classifying the "low-risk" samples.

### SMOTE Algorithm
![SMOTE](https://github.com/Caracalla1081/Credt_Risk_Analysis/blob/8a6f5b3bbe609473b9b339935ce48205112d02f4/Images/SMOTE%20Algorithm.png)
- Balanced Accuracy Score: The balanced accuracry score of .66 can be considered marginal at classifying who is and who is not at a worthy candidate for credit lending, meaning the "low-risk" classifications are unreliable.
- Precision Score: The precision score of .01 to classify "high-risk" and score of 1 for classifying "low-risk" indicates that there are a large amount of false positives for "high-risk", meaning the classification of "low-risk" us unreliable.
- Recall Score: The recall score of .66 for "high-risk" and "low-risk" classification illustrates the models barely acceptable ability to classify either risk categories accurately.
 
 
### ClusterCentroids Algorithm
![ClusterCentroids](https://github.com/Caracalla1081/Credt_Risk_Analysis/blob/8a6f5b3bbe609473b9b339935ce48205112d02f4/Images/ClusterCentroids%20Algorithm.png)
- Balanced Accuracy Score: The balanced accuracry score of .66 can be considered marginal at classifying who is and who is not at a worthy candidate for credit lending, meaning the "low-risk" classifications are unreliable.
- Precision Score: The precision score of .01 to classify "high-risk" and score of 1 for classifying "low-risk" indicates that there are a large amount of false positives for "high-risk", meaning the classification of "low-risk" us unreliable.
- Recall Score: The recall score of .67 for "high-risk" and .40 for "low-risk" classification illustrates the model is okay at classifying "high-risk" candidates, but terrible at classifying "low-risk" candidates accurately.
 
### SMOTEEN Algorithm
![SMOTEEN](https://github.com/Caracalla1081/Credt_Risk_Analysis/blob/8a6f5b3bbe609473b9b339935ce48205112d02f4/Images/SMOTEEN%20Algorithm.png)
- Balanced Accuracy Score: The balanced accuracry score of .53 can be considered bad at classifying who is and who is not at a worthy candidate for credit lending, it is essentially a toss-up on whether or not candidates are classifed as "low-risk" or "high-risk".
- Precision Score: The precision score of .01 to classify "high-risk" and score of 1 for classifying "low-risk" indicates that there are a large amount of false positives for "high-risk", meaning the classification of "low-risk" us unreliable.
- Recall Score: The recall score of .67 for "high-risk" and .40 for "low-risk" classification illustrates the model is okay at classifying "high-risk" candidates, but terrible at classifying "low-risk" candidates accurately.
 

### BalancedRandomForestClassifier
![BalancedRandomForestClassifier](https://github.com/Caracalla1081/Credt_Risk_Analysis/blob/8a6f5b3bbe609473b9b339935ce48205112d02f4/Images/BalancedRandomForestClassifier%20Algorithm.png)
- Balanced Accuracy Score: The balanced accuracry score of .73 can be considered good at prediciting who is and who is not at a worthy candidate for credit lending.
- Precision Score: The precision score of .02 to classify "high-risk" and score of 1 for classifying "low-risk" indicates that there are a large amount of false positives for "high-risk", meaning the classification of "low-risk" us unreliable.
- Recall Score: The recall score of .70 for "high-risk" and .76 for "low-risk" classification illustrates the model is relatively okay at classifying "high-risk" candidates, equally.

### EasyEnsembleClassifier
![EasyEnsembleClassifier](https://github.com/Caracalla1081/Credt_Risk_Analysis/blob/8a6f5b3bbe609473b9b339935ce48205112d02f4/Images/EasyEnsembleClassifier%20Algorithm.png)
- Balanced Accuracy Score: The balanced accuracry score of .73 can be considered good at prediciting who is and who is not at a worthy candidate for credit lending.
- Precision Score: The precision score of .02 to classify "high-risk" and score of 1 for classifying "low-risk" indicates that there are a large amount of false positives for "high-risk", meaning the classification of "low-risk" us unreliable.
- Recall Score: The recall score of .70 for "high-risk" and .76 for "low-risk" classification illustrates the model is relatively okay at classifying "high-risk" candidates, equally.

## Summary
After running and evaluating all the algorithms, it is safe to say that if the company was adamant about choosing a model to use, it would be one of the two ensemble classifiers; the Balanced Random or the Easy Ensemble. Since the impact of false negatives relating to potential losses in lending to high-risk candidates is not as risky as if we were testing for cancer, the company may find the results of these algorithms acceptable. The cmpany may find that these results fit into their other analysis on how many "losses" they can accept and still reach their yearly financial goals.

In my overall opinion, I would not recommend that any of these algorithms are great at the companies goal of accurately classifying "low" and "high" risk candidates. All models tested are bad to marginally good at properly classifying "low-risk" candidates, meaning that too many applicants are being classified as "low-risk" when they could in fact be "high-risk". When recall scores are factored in, the results illustrate teh same; the models are all either bad or marginally good at classifying candidates accurately.

Again, in summary, if the company is accepting of a certain level of loss, then the Balanced Random Forest or Easy Ensemble classifiers are the prefered models to use in classifying "low" and "high" risk candidates accurately.
