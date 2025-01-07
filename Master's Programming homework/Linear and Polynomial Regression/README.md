We are going to use different variants of regressors to model a sinusoidal function. Use the following code
to create a set of non-linear data:

import numpy as np
np.random.seed(42)
m = 1000
X = 5 * np.random.rand(m, 1) - 2.5
y = np.sin(X)*100 + np.random.randn(m, 1)

1) Apply standardization to the data and plot the learning curve for Linear Regression.
2) Transform the data into a polynomial of degree 50, apply standardization and plot the learning curve.
3) Repeat the process for a Regularized Linear Regression model using Ridge Regression with alpha=0.001
and comment on the differences between the three plots.
4) Apply 10-fold cross-validation for the simple Linear Regression model and calculate the mean RMSE
and its standard deviation.
5) Apply 10-fold cross-validation for the polynomial model without regularization and calculate the mean
RMSE.
6) Apply 10-fold cross-validation for the regularized model and calculate the mean RMSE.
7) Comment on your results in the queries 4, 5, and 6.
