This problem focuses on supervised learning concepts using Ensemble Models, utilizing popular learning
frameworks. Additionally, the final question benchmarks the performance of a semi-supervised learning
approach using the scikit-learn library.
Please fix the random state to 42 where required.

1) Load the provided dataset, pima.csv, print its shape and display the distribution of the target vari-
able.
A description of the dataset can be found in this link:
https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database/data.

2) Display the main statistical characteristics of each column in the data in a tabular format. Identify
columns where the minimum value takes an unreasonable value equal to zero. Replace these zero values
with the median of the corresponding column, as they represent missing values based on the dataset’s
creation protocol. Print the updated dataset’s characteristics in a tabular format and list the columns
affected by this step.

3) Perform a stratified split of the dataset, allocating 700 instances to the training set and the remain-
ing samples to the test set. Ensure that the target variable is the Outcome column, while the rest of the
columns constitute the feature space for the classification task.

4) Train the following models:
- A simple Decision Tree classifier using the default values of its parameters.
- A Random Forest classifier using the default values of its parameters.
- A Bagging classifier with an SVM classifier (linear kernel) and 10 estimators.
- An AdaBoost classifier with a decision tree classifier, using 100 estimators and a learning rate of 0.25.
For each model, display a classification report presenting the standard classification metrics, precision,
recall, and F1-score and the confusion matrix as they were calculated on the test set.

5) Compare the performance of the previous four models. Comment on the observed performance
differences.

6) Select the best-performing classifier from Question #4 as the base model. Wrap it in an instance of
the SelfTrainingClassifier class with the arguments criterion=‘threshold’ and threshold=0.99. Randomly
select 200 instances from the initial training set as labeled data, marking the rest as unlabeled. Train the
semi-supervised model on the combined labeled and unlabeled data and train the supervised model on
only the labeled data. Evaluate both models on the same test set, display the classification reports, and
add your comments.
