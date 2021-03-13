# Cross-Validation-Methods

**Cross Validation :**
- Cross Validation is a evaluation technique of the model
- It is used to assess the generalization performance of a ML model.
- It helps us to measure how well a model generalizes on a training data set

**Types Cross Validation:** There are two main categories of cross-validation in machine learning.
- Exhaustive: This method learns and tests on all possible ways to divide the original sample into a training and a validation set.
- Non-Exhaustive: This method don’t compute for all possible combinations of the original data.

**Types of Exhaustive method:**
- **Leave-P-Out Cross-Validation**: In this strategy, p observations are used for validation, and the remaining is used for training. For a data set with n observations, n-p observations will be used for training, and p will be used for validation. Since this method is exhaustive, it trains and tests on all possible combinations, and it can become computationally expensive for large values of p.
- **Leave-one-out Cross-Validation**: This is a variant of LPO. When p = 1 in Leave-P-Out cross-validation then it is Leave-One-Out cross-validation. In LOO, one observation is taken out of the training set as a validation set. We will train the model without this validation set and later test whether it correctly classify the observation.

**Types of Non-Exhaustive method:**
- **Hold-Out**: This is the simplest method of all. In Holdout validation, the data is randomly partitioned into train and test set. Most of the times it is 70/30 or 80/20 split. We train our model in the training set, and it’ll be tested in the test set to see how well the model is performing for unknown events.
- **K-Fold**: This is the frequently used cross-validation method. In k-fold cross-validation, we split the training data set randomly into k equal subsets or folds. Out of these k subsets, we’ll treat k-1 subsets as the training set and the remaining as our test set. This process is repeated for k iterations. For each iteration, a different fold is held-out for testing, and the remaining k-1 is used for training.
- **Stratified K-Fold**: We use stratified K-fold to cope with class imbalances in the data set. Stratified K-fold maintains the class proportions by splitting the data set in such a way that they contain approximately the same proportions of labels as in the original data set. This strategy guarantees that when the data set is unbalanced, one class of the data is not over-represented.
- **Repeated random subsampling validation**: Monte Carlo validation splits the data randomly into train and test set, and this process is repeated multiple times. The results are averaged over all splits. The disadvantage of this method is that some observations may never be chosen, whereas some might be selected multiple times.

**Why Cross Validation is used ?**
- We used because whether the model is peforming generally or not.
- We can identify whether our model is underfit or overfit.
