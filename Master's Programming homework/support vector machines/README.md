Apply linear and RBF SVMs on the Breast Cancer dataset.
1) Download the Breast Cancer dataset from the sklearn.datasets package.
2) Out of the 30 available features, select only ”Worst area” and ”Mean Concave Points”.
3) Visualize the data from the Positive and Negative class with the ”Mean Concave Points” on the x-axis
and ”Worst Area” on the y-axis. 4) Train two linear SVM classifiers with the regularization hyperparam-
eter C equal to 0.1 and 1000, respectively. Don’t forget data standardization.
5) Plot the data points, the decision boundaries and the margins for the two classifiers.
6) Display the number of Support Vectors and the training set F1-score for each of the two classifiers.
7) Run a Grid Search for an RBF SVM, with the following hyperparameter options:
C: [0.1, 1, 10, 100] , gamma: [0.1, 1, 10, 100]
8) Display the best hyperparameter values, the number of support vectors, and the training set F1-score
for the best model.
9) Plot the data points and the decision boundary for the best RBF model.
