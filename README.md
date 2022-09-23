# Regressions

## Linear Regression

We use the data set chemistry_samples.csv to obtain a linear regression model to predict the toxicity factor LC50 as our target variable using all the other features as predictors.

We apply the model to the test (unseen) data (chemistry_test.csv) to predict the target variable, and compute the out-of-sample R2 score on this test set. We compare the out-of-sample and the in-sample R2 score.

## Ridge Regression

We use the data set chemistry_samples.csv and repeat a similar task to the Linear regression, but employing Ridge regression with 5-fold cross-validation to tune the penalty hyper-parameter of the model. Using the average mean squared errors (MSE) over all folds, we demonstrate with plots how we scan the penalty hyper-parameter to find its optimal value. We report the optimal value for the penalty parameter and the performance of the model in terms of MSE. Using some of your computations, we explain the trend of bias, variance and MSE as a function of the penalty hyper-parameter.

Then we fix the penalty hyper-parameter to the optimal value and retrain the model on the entire data set chemistry_samples.csv. We obtain the in-sample R2 score when applied to chemistry_samples.csv, and compare it to the out-of-sample R2 score on the test set chemistry_test.csv.

## Relaxation of Lasso Regression

We implement a relaxation of the Lasso optimisation that can be solved using gradient descent. We consider a smooth version of Lasso in which the penalty term of the cost function is approximated through smooth functions Lc (Huber functions) so that it is differentiable.

We use the data set chemistry_samples.csv and employ this relaxed Lasso-Huber regression with a 5-fold cross-validation (with the same folds as in 1.2.1) to conduct a grid search to find the optimal penalty hyper-parameter lambda.