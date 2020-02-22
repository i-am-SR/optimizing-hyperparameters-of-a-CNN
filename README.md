# optimizing-hyperparameters-of-a-CNN
Optimizing the hyper-parameters of a Convolutional Neural Network using gaussian processes

In this project you will apply Gaussian Processes to efficiently select best hyper-parameters for a
model. You will implement a convolutional neural network (CNN) to classify the cropped color
digits from the SVHN dataset [12]. Using the training set, create your training dataset of 10, 000
samples (1000 samples per digit). Create a separate validation dataset of 500 samples (50 samples
per digit). From the test dataset, select 2000 samples (200 samples per digit). This is the data for
the experiment. The CNN architecture consists of 3 convolution layers followed by 3 fully connected
layers including the classification layer. The first convolution layer has 32 filters of size 5 × 5 with
zero padding and stride 1. The second convolution layer has 64 filters of size 3×3 with zero padding
and stride 1. The third convolution layer has 128 filters of size 3 × 3 with zero padding and stride
1. The first and second fully connected layers are of dimensions 1024, the third fully connected
layer (softmax-cross-entropy) is of size 10. Apply ReLU activations for all layers except the last
layer, which has softmax activation. Apply dropout to the first and second fully connected layers.
we have 5 hyper parameters for this network. 
(1) Starting Learning Rate: η0, 
(2) Learning Rate 4 Decay: δ, where learning-rate η = η0(1+δ∗t) , where t is the epoch number, 
(3) Mini-Batch size: B,
(4) Dropout parameter p1 for the first fully connected layer, 
(5) Dropout parameter p2 for the second fully connected layer. 
The goal is to estimate the optimal values of the hyper parameters
using the validation set. Apply the principles outlined in this work [13] and [14] (Bayesian Global
Optimization) to demonstrate that Gaussian Processes arrive at the optimal hyper parameters much
more quickly compared to grid search.
