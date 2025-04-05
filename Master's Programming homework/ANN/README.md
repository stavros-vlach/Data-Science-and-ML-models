In this task, you will experiment with a standard neural network architecture by utilizing different fea-
ture subsets from the Fashion MNIST dataset. You are required to use only Keras components through
Tensorflow for building the neural network models, while any necessary analysis should utilize standard
libraries (like pandas, numpy, or sklearn).
1) Load the Fashion MNIST dataset using Keras’ dataset module, adhering to the default training and
test split specified in the official documentation, https://keras.io/api/datasets/fashion mnist/. Then, use
the last 10,000 instances of the training subset as the validation subset.
2) Record the class distribution of the 3 distinct subsets (training/validation/test) in a Pandas Dataframe,
sorting them by the column name, which should coincide with the actual name of the existing labels.
3) Print the range (minimum and maximum) of pixels in each part of the dataset. Scale the data by
normalizing the pixel values.
4) Create two data variants:
 The first will retain only the top half (upper portion) of each image.
 The second will retain the bottom half (lower portion) of each image.
Crop each image along the height axis to create these two distinct representations.
5) Visualize the first 20 instances from the training set for both variants. Use subplots with 4 rows and
5 columns to display them, verifying the correctness of your slicing process against a plot of the original
images.
6) Build a neural network using Tensorflow/Keras for a multiclass classification task. The network
should have two hidden dense layers with 128 and 64 nodes, and use ReLU as the activation function of
each layer. The output layer should be compatible with multiclass classification. Compile the model using
the SGD optimizer with a learning rate of 10−4 , sparse categorical cross-entropy as the loss function, and
add classification accuracy to the metrics. Print a summary of the model.
7) Train one model for each data variant, ensuring consistent weight initialization across both experi-
ments. Hint: Store the initial random weights of the model in a variable. Train the model on the first data
variant, and then reset the weights of the model to the stored weights. Train each model for 10 epochs with
batches of 32 samples. Apply each trained model to the corresponding test set and export the classification
report for each model using the scikit-learn library. Comment on the most important differences in the
models’ performance per class.
8) Identify test instances where one model correctly predicts the correct class, but the other model
makes an incorrect prediction. For each case, display the first 5 instances along with the actual labels and
the incorrect predictions from the competitor model.
