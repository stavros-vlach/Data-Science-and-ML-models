In this assignment, you will implement and train a Generative Adversarial Network (GAN) from scratch
using the Fashion-MNIST dataset. Your GAN will learn to generate synthetic fashion item images that
resemble real samples from selected categories.

1) Load the Fashion-MNIST dataset through tensorflow.keras.datasets, keep the data on the training
set, select and retain only the T-shirt/top, Trousers, and Pullover classes, and scale the pixel values to the
range [-1, 1].

2) Create a generator that takes input random noise vectors of size 30. It has two hidden layers, each
with 100 and 150 units, with an activation function ReLU and a He normal kernel initializer. It outputs
a fully connected layer of a 784-dimensional vector with activation tanh, which is reshaped to a 28 by 28
pixels image.

3) Create a Discriminator that reads a 28 by 28 pixel image and classifies it as “real” or “fake”. The
Discriminator consists of two hidden layers, each with 150 and 100 units, with an activation function ReLU
and a He normal kernel initializer. A sigmoid function activates the output layer.

4) Connect the generator and discriminator to set up a GAN pipeline. Use the Binary Cross Entropy
as the loss function and the RMSProp optimizer for both the discriminator and the GAN models. Create
batches of 32 images by slicing the training set. Train the GAN for 10 epochs, alternating between updat-
ing the Discriminator and Generator models on each batch. After each epoch of training ends, visualize
32 generated images.
   
5) After training the Generator, feed it with 32 random noise vectors and visualize the 32 generated
images. Are you satisfied with the results?

6) What is the accuracy of the discriminator in predicting that the generated images of the previous
question are fake?
