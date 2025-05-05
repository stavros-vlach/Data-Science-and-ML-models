In this task, you will explore strategies to help neural network architectures mitigate issues such as over-
fitting. Your goal is to analyze the impact of each strategy when applied to a deep network architecture.
Apply the following models to the data that retain only the top half (upper portion) of each image of
the Fashion MNIST database.
Train each model using an Adam optimizer, for 15 epochs with a batch size of 32, sparse categorical
cross entropy as the loss function, and add accuracy as a metric. Ensure the output layer is appropriately
configured for a multiclass problem.
1) Create and train a base model using Tensorflow/Keras library with three hidden layers of 128, 64,
and 32 nodes, respectively, and add ReLU as their activation function.
2) Rebuilt and train the base model after adding an early stopping mechanism, with a patience argu-
ment of 3, and track the validation loss.
3) Rebuilt and train the base model after incorporating a batch normalization layer after each dense
layer (do not use early stopping, and ensure the use bias argument of dense layers is set to False).
4) Rebuilt and train the base model after adding a dropout layer with a rate of 0.50 after each dense
layer (do not use early stopping or batch normalization).
For each of the four questions in this problem, print the model summary of each created model and
generate a classification report using the scikit-learn library. Moreover, plot the training and the validation
loss along with the training and the validation accuracy. In the same figure pinpoint the best epoch.
Finally, comment on the obtained results. Did you notice any significant differences in performance?
