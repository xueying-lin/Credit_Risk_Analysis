# Credit_Risk_Analysis
LendingClub is a peer-to-peer lending services company and interested in how to assess the credit risk of the borrowers. As a data analyst, I need to use Machine learning techniques to figure out this question for them. Using different sampling techniques, such as Oversampling, undersampling, and combination of two to prepare the data and using two machine learning models to predict the credit risk.
## Overview
- Purpose: Testing and Comparing the sampling and machine learning models to choose **the most suitable models for predicting the credit risk.**

## Results
- **Naive Random Oversampling**
  - Accuracy score is around *62.90%*
  - ![naive random oversampling accuracy score](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/naive%20random%20oversampling-accuracy%20score.PNG)
  - Precision score for predicting high-risk loaners is low, *1%*, and the sensitivity rate is medium high, *70%*
  - ![native random oversampling report](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/naive%20random%20oversampling-report.PNG)

- **SMOTE Oversampling**
  - Accuracy score is around *65.44%*, higher than naive random oversampling
  - ![SMOTE oversampling accuracy score](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/SMOTE%20oversampling-accuracy%20score.PNG)
  - Precision score for predicting high-risk loaners is low, *1%*, and the sensitivity rate is medium, *61%*, which performs worse than naive random oversampling
  - ![SMOTE oversampling report](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/SMOTE%20oversampling-REPORT.PNG)

- **Undersampling**
  - Accuracy score is around *54.47%*, performs worse than oversampling
  - ![undersampling accuracy score](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/undersampling-accuracy%20score.PNG)
  - Precision score for predicting high-risk loaners is low, *1%*, and the sensitivity rate is medium high, *69%*, which performs better than SMOTE oversampling but worse than naive random oversampling
  - ![undersampling report](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/undersampling-report.PNG)

- **Combination sampling**
  - Accuracy score is around *64.43%*, performs better than undersampling, but worse than SMOTE oversampling
  - ![Combination sampling accuracy score](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/combination%20sampling-accuracy%20score.PNG)
  - Precision score for predicting high-risk loaners is low, *1%*, and the sensitivity rate is medium high, *72%*, which performs better than oversampling and undersampling
  - ![Combination sampling report](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/combination%20sampling-report.PNG)
 
 - **Random Forest Classifier**
   - Accuracy score is around *76.34%*, performs better than above four models
   - ![Random forest classifier accuracy score](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/random%20forest%20classifier-accuracy%20score.PNG)
   - Precision score for predicting high-risk loaners is low, *3%*, and the sensitivity rate is medium, *63%*. The precision performs better than above four models, but the sensitivity rate only performs better than SMOTE oversampling.
   - ![Random forest classifier report](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/random%20forest%20classifier-report.PNG)

 - **Easy Ensemble Adaboost Classifier**
   - Accuracy score is around *93.29%*, high performance and is the best among six models
   - ![Adaboost classifier accuracy score](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/ada%20booster%20classifier-accuracy%20score.PNG)
   - Precision score for predicting high-risk loaners is still low, *9%*, and the sensitivity rate is high, *92%*. The precision and sensitivity rate performs best among six models.
   - ![Adaboost classifier report](https://github.com/xueying-lin/Credit_Risk_Analysis/blob/4c92eec81d70ecffc8022387cd0acf44e17ca5ef/Challenge/code/Resources/ada%20booster%20classifier-report.PNG)
  
## Summary
All of the naive random oversampling, SMOTE oversampling, and undersampling model performs bad on precision and sensitivity. Although the combination sampling model improves the recall rate, the precision rate is really low and the accuracy rate did not improve a lot. Although the weight of this machine learning model will be on sensitivity, the low precision rate is still terrible for decision making on lending the money. The low lending rate will cut off the customer size. Therefore, those four models are not recommanded.

Easy Ensemble Adaboost classifier model is the best recommendation for this company. Because it has the high sensitivity rate (92%), which means among 100 borrowers who indeed are high-risk customers, the system can detect 92 of them as high-risk borrowers, which improves the saftey of the company. Meanwhile, the adaboost classifier imporves the accuracy rate and the precision rate, which is helpful for the decision making process. **Therefore, I recommand the easy ensemble adaboost classifier model.**
