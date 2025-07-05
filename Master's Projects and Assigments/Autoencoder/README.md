In this assignment, you will work with a filtered version of the Fashion MNIST dataset to explore the
ability of autoencoders to compress and reconstruct image data. You will build and evaluate two autoen-
coder variants and compare their performance based on various experimental setups. Make sure to print
any output you consider important to support your observations.

1) Load the Fashion MNIST dataset from the tensorflow.keras.datasets module. Keep only the in-
stances that belong to the following three classes: ‘Sandal’, ‘Sneaker’, and ‘Ankle boot’. Split the filtered
dataset into a training set (5/7), a validation set (1/7), and a test set (1/7). Make sure the split uses
stratified sampling to preserve class balance. Scale all subsets so pixel values are in the range [0, 1]. Print
the class distribution of each subset with clear, labeled messages.

2) Build a stacked autoencoder with the following architecture: an encoder and a decoder part of two
fully-connected (Dense) layers each. Use ReLU activation for all hidden layers, and sigmoid activation for
the output layer. Flatten the input before feeding it to the encoder, and reshape the output to match the
original image shape (28×28). Set the latent space (codings) size to 50, and all other hidden layers to 256
units. Compile the model using: Nadam optimizer with learning rate 10−4 , adding binary cross-entropy
as the loss function. Print the model summary of this autoencoder.

3) Now, build a second autoencoder that is identical in architecture to the one in Question 2, add l1
regularization to the latent space (the bottleneck layer), and use an activity regularizer with weight 10−6 .
Print the model summary for this sparse autoencoder. 

4) Train both autoencoders (from Q2 and Q3) for up to 50 epochs. Use early stopping with patience=5,
and min_delta equal to 10−2 , monitoring the validation loss. Train each model with two different batch
sizes: 32 and 256. This gives you four experiments in total (2 models × 2 batch sizes). After running
your experiments, plot the training and validation loss curves for all of them. Add your comments on the
differences observed between the models and batch sizes.

5) Write a function that compares original images with their reconstructions from an autoencoder.
The function should:

• Accept a model, a set of images, and the number of images to display as input.

• Display a grid where the top row shows the original images, and the bottom row shows the recon-
structed images.

• Ensure the pixel values are clipped to the range [0, 1] for proper visualization.

Then use this function to display the first 15 test images and their reconstructions from the regular au-
toencoder trained with a batch size of 256, and the sparse autoencoder trained with a batch size 256. [10%]
