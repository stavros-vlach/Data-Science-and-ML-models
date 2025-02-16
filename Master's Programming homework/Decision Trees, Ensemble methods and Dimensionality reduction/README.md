This problem concentrates on training models for the MNIST dataset using Decision Trees, Ensemble
Models and Dimensionality reduction: Please fix the random state to 42 where required.

1) Open a Jupyter-notebook load the MNIST dataset and split it into 80% training and 20% test parts
using stratisfied splitting with a fixed random state. Retain only the 10000 first entries of the training
set and the first 2000 from the test set. Convert the labels from an array of strings to an array of 64-bit
integers.

2) Perform a Grid Search with 5-fold cross validation, with the maximum number of features taking
the values [100, 150, 200], and the maximum depth the values [2, 4, 5], for a Decision Tree Classifier, using
the Entropy criterion and fixed random state. Print the accuracy score, the F1 - score (set the average
parameter to “macro”), with respect to the test data, and the values of the best parameters for the best
estimator. Print the scores for all the combinations of the grid search parameters and discuss the results.
  
3) Create a pipeline performing PCA with fixed random state, retaining 90% of the variance of the
initial features included in the training dataset, and train a Decision Tree with the depth parameter dis-
covered in the previous question. Compute the accuracy and the F1 - score with respect to test data and
compare them with the previous results. Please discuss the advantages or disadvantages of using PCA.

4) Perform PCA with the number of components dictated in the previous question, compress the train-
ing data and train a Gradient Boosting Classifier (GBC). The model should have a maximum depth of 2, 6
estimators and a learning rate equal to 1.0. The random state should be fixed where required. Discuss the
results with respect to the previously used Tree Classifier. How is it possible for the GBC, with shallow
trees, to outperform a deeper Tree Classifier?

5) Reconstruct the first five images (digits) by using the output of the PCA, of the previous question,
and plot them along with their corresponding originals in the same figure and discuss. [15%]
Perform KMeans Clustering, with 20 clusters, using the PCA transformed training data and plot the most
representative digits in a Figure with 2 rows and 10 columns. The most representative digit of each cluster
is its corresponding centroid.

6) An important part of unsupervised learning is labelling. Manually label the printed images (cen-
troirs) of the 20 clusters in Question #5 and store them in a vector. Then, label each sample of the test
data based on the label of its nearest cluster (label propagation). By treating these assignments as pre-
dictions, compute the accuracy and F1 score, with respect to test set labels, and compare to the previous
approaches with respect also to the execution times of the trainig process.
