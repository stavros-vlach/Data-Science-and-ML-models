Work with the MNIST dataset and:
1) Split and normalize the data into a training (5/7), a validation (1/7), and a test (1/7) set. [5%]
2) Convert the target values into one-hot vectors.
3) Built a convolutional neural network (CNN). For the features extractor part of the CNN, create:
a 2D convolutional layer of 8, 5x5 kernels, add padding zeros to the image and move each kernel two
pixels,
a 2x2 max polling layer,
a 2D convolutional layer of 16, 3x3 kernels that retain the size of its input image and
a 2x2 max polling layer,
a 2D convolutional layer of 32, 3x3 kernels that retain the size of its input image.
For the classification part of your model, start with a 20% dropout layer and use two fully connected layers
of 64 and 32 nodes, in addition to the output layer.
4) Compile the model using the Adam optimizer, a loss function of your choice, and add accuracy in
your metrics.
5) Fit the model on the training data (allow 100 epochs) and use early stopping with patience 5 epochs
to monitor the validation set.
6) Plot the history of the loss and accuracy of the training process for the training and the validation
set. Comment on your results.
7) Plot the confusion matrix and the accuracy of your model on the test set.
Feel free to take any extra action to solve this problem.
