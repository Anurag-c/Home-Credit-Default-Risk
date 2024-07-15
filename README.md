# Home-credit-default-risk

In the final phase, after proving our hypothesis that tuned machine learning techniques can outperform baseline models to aid Home Credit in their evaluation of loan applications, we believe expanding our framework will create a more robust environment with improved performance.

Logistic regression, XGBoost, Random Forest and LightGBM were selected to run with RFE, PCA, SelectKBest and Variance Threshold for feature selection, and SMOTE for data imbalance. The best performance for each algorithm was included in the classification ensemble using soft voting. The resulting Kaggle score was 0.72592 ROC_AUC.

Single and Multi-layer deep learning models, including linear, sigmoid, ReLu, and hidden layers were added with binary CXE, custom hinge loss using adam & sgd optimizer. The deep learning Kaggle score fell short of the ensemble model; additional experimentation will result in a better performing deep learning models. By combining and continuing to refine our extended loss function, we can further demonstrate our effectiveness.

Below has more details or the various classifiers executed in this project.

### **Logistic Regression :** <br> 
This model was chosen as the baseline model trained with imbalanced dataset and later performed feature selection using RFE, SelectKBest, PCA & Variance Threshold technique on it. The baseline training accuracy for this model was encouraging which let us to perform the prior mentioned feature selection on these models. The best model for logistic regression we had is with Variance Threshold, with training accuracy as 92.56% and test accuracy as 92.2%. A 75.22% ROC score resulted with best parameters for this model. The same model was run with other feature selection performed very closer to the best model.

### **Gradient Boosting :** <br> 
Boosting didn't help in achieving better results than the baseline model. The results were not good enough to continue in implementing & evaluating other feature selection technique. Training accuracy of 94.75% and test accuracy of 91.95% was achieved in this model. Test ROC under the curve for this model came out to 72.12%

### **XGBoost :** <br> 
By far this model resulted in the second best model with RFE hence we continued to explore other feature selection techniques on this. The best performing model for XGBoost was with Variance Threshold. The accuracy of the training and test are 93.1% and test 92.36%. Test ROC under the curve is 73.88%. The other feature selection were very closer to the best XGBoost model. We also performed XGBoost with SMOTE as the dataset had oversampled records. The ROC score has promising result with 74.23%.

### **Light BGM :** <br> 
Our expectation was this model would give us better and faster results than XGBoost, however it was slightly lower compared to XGBoost. Both RFE and variance threshold feature selection resulted in same ROC score of 72.2. The training accuracy came as 92.81% and test accuracy 92.28% was achieved.

### **Random Forest :** <br> 
On our last decision tree models, the best Random Forest was with variance threshold which produced training accuracy of 92.51% and test accuracy of 92.36%. Test ROC score came out as 72.43%. Random forest performed better compared to LightBGM but lower than XGBoost.

### **SVM :** <br> 
This was the lowest performing model in our experiment. Hence we didn't decide to continue on SVM with other feature selection techniques. The ROC score achieved for this model was way lower i.e. is 67.21%.
