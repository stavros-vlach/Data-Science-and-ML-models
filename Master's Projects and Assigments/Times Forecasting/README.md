This problem concentrates on training a Neural Network model for time series forecasting. The dataset
at hand corresponds to the Monthly Mean Sunspots spanning from 1749 to 2019. Thus it includes 3252
samples. The goal of this analysis is to build a Multilayer Neural Network that can forecast accurately
the number of sunspots several months into the future (multi-step ahead forecast). You are required to
do the following:

1) Open a Jupyter-notebook load the the sunspots.csv file. Print and observe the structure of the data.
Extract the appropriate column that is of interest to the analysis.

2) Check the sanity and appropriateness of the data. Search for missing values and print descriptive
statistics. Cast the data into a numpy array. Plot the data.

3) Scale all data in the interval [0,1]. Choose a window parameter of 40 timesteps. Split the resulting
reformed data into train and test parts such that 90% of the samples in retained in the training set. The
output of the Neural Network should be a vector of size equal to length of the test set (forecasting horizon).
This horizon should be constructed with one input sample (sequence-to-vector).

4) Build a Multilayer Percepton Model with the following sequence of layers:
a) Batch Normalization Layer
b) Dense layer with 50 neurons utilizing Lecun Normal initiliazation and SELU activation
c) Dense layer with 25 neurons utilizing Lecun Normal initiliazation and SELU activation
d) An output layer

The model should be compiled with MSE loss and ADAMW optimizer. Add MAE to the model’s
metrics. Train the model for 30 epochs with a batch size set to 32 and with a validation split set to 10% of
the training set. You have to utilize early stopping with patience of 2 iterations and the ability to restore
the best weights. Print the model summary and explain the number of parameters and where they come
from. Measure the training time and print.

5) Plot the training loss with respect to the epochs in a semi logarithic diagram for both training and
validation. Print the RMSE and MAE for training and test. Discuss the results.

6) Compute predictions based on test inputs. Plot the actuals corresponding to the test set along with
the predictions and discuss the results.

7) Create an additional model using two Gated Recurrent Unit (GRU) layers and the output layer of
Q4. The parameters should be the same as those on Q4. Compare the new model with the existing one
with respect to training times RMSE and MAE of the predictions on the test set. Additionaly, the early
stopping criterion should check if the minimum change in the monitored quantity is above 0.0005. Discuss
your results.
