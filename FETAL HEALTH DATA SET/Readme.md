It is a study of Fetal Health and comparing and classifying various parameters in order to prevent child and maternal mortality.

In this we have 22 columns and 2126 records. The target column is Fetal_health which is classified into 3 classes.

Normal-----------1 Suspect----------2 Pathological-----3

We have done Visualization of data. No missing values are there in the dataset

We built the model using K-Nearest Neighbor Algorithm. Then tuned the model using GridSearchCV

Short introduction of Hyper parameter Tuning:

Hyper parameter tuning -- GridSeachCV To improve all scores for each ML model, we want to search the set of "hyperparameters" by using the common approach "Grid search" for four models above.

Hyper-parameters are a set of additional, model-dependent parameters that are not inferred automatically by the learning algorithm but need to be specified before the learning phase: a common example of hyper-parameter is the value of k in k-Nearest Neighbor or the number of hidden units in a Neural Network. Hence, finding sub-optimal values of the hyper-parameters is crucial to ensure proper generalization. The hyper-parameter optimization procedure, which was repeated separately for each candidate learning methodology, encompassed the following steps:

Firstly, a set of suitable hyper-parameters to optimize was identified; for each of them, a range of candidate values was specified. These choices are dependent both on our expertise and on the computational cost needed to train the models.

Secondly, a predictor was learned for all the possible combinations of hyper-parameters and its out-of-sample performance was estimated using 5-fold Cross Validation (CV), i.e. We trained the model with 70% of the total training set size and validated its performance in the remaining 30%.

GridSearch:

GridSearch exhaustively searches through all possible combinations of hyperparameters during training the phase. Before we proceed further, we shall cover another cross-validation (CV) methods since tuning hyperparameters via grid search is usually cross-validated to avoid overfitting. Hence, For accelerating the running GridSearchCV we set: n-splits=3, n_jobs=2.