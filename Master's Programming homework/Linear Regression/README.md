A very frequent problem in machine learning is predicting the value of a feature of an unknown set of samples, based on the remaining features with respect to a given dataset. This is performed by proper analysis of the predictors, i.e. the features that will be used as inputs to the model, and the labels which are the outputs of the model. An interesting use case, in these lines, is the estimation of the wine quality based on its characteristics. This assignment requires the design and implementation of an end-to-end machine learning solution that ad- heres to the following:

1. Open a Jupyter-notebook. Download the wines dataset and load the data of the “red” wines.
2. What are the features describing the quality of the wines?
3. Compute the descriptive statics of the dataset features and discuss about their types, ranges and completeness.
4. Form the histograms of the features and discuss their distribution. Can the distribution of some features be improved (tending more towards the Gaussian) and how?
5. Which are the features that mostly affect quality and which are those that affect it less? Provide evidence through correlation and discuss accordingly.
6. Split the dataset into a training and a testing set retaining 80% and 20% of the total number of samples, respectively, using splitting that retains the statistical properties of the input data (stratified) with respect to quality.
7. Scale the data with a Standard scaler and train a linear regression model. Evaluate the performance of the model, using the test set, with respect to metrics such as R2-score, Mean Absolute Error, Mean Absolute Percentage Error, Mean Squared Error and Accuracy. Comment on the accuracy of predictions by plotting Actuals vs Predicted diagram. 
8. Perform 10-fold cross validation and compute the mean and standard deviation of the scores over the folds. Is the model’s R2-score within the limits defined by the 10-fold cross validation?
