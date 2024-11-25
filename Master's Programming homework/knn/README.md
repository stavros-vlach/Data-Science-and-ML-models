Let’s deep dive into the MNIST dataset, where you have to handle the next subqueries:
1) Load the data as arrays and split them into training and test sets with the next ratio: 85-15. Verify
that all the classes have the adequate number of instances.
2) Depict the first 8 images of the created training and test sets using different subplots in a 2 by 4 frame,
with their labels as titles.
3) We need to handle a classification problem of distinguishing between two classes: even and odd numbers.
First, create the training and test subsets for each class. Then, choose a binary classifier and a normal-
ization technique of your choice, before wrapping them into a scikit-learn pipeline. Fit your pipeline to
observe the created diagram.
4) Use 3-fold cross validation and evaluate your classification pipeline by calculating the next metrics: ac-
curacy, recall, and precision. Compare the predictive performance of your model against a dummy model
that always guesses that an image belongs to the even category.
5) Calculate the confusion matrix for the training set, following the same 3-fold cross validation protocol.
Record the kind and the amount of the predictions based on that.
6) Train the same pipeline over all the training set, and apply that on the test set for getting your predic-
tions. Extract again the confusion matrix, and comment any great changes in the behavior of your model.
7) Pick one random instance from those that belong to false positives and false negatives from the test
set, and depict their original images in separate figures.
