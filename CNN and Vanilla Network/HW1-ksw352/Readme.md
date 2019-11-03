2 Methods Used:<br>
2.1 **Fully connected neural network** [vanilla code in python ] <br>
• Implement the following operations: forward propagation, cost function, backward propagation, parameter updates, train, predict, affine-forward, affine-backward, activation forward and activation
backward.in python using just the matrix operation library (numpy). Do not use any other python
libraries/modules. (only need Pytorch to load the data)<br>
• The network should consist of a minimum of two hidden layers (other than the input and the output
layer).<br>
• The last layer in the neural network should be softmax (dimensions being the number of classes).<br>
• You are expected to formulate the back propogation algorithm for the network being defined.<br>
• The network should have flexibility to the number of hidden layers and hidden neurons.<br>
• Your network needs to have a validation accuracy of 50%.<br>
• After training the network, make predictions on the test set. Use the save predictions() function to
save y pred to file “ans1-uni.npy”. The numpy array should contain the un-normalized scores from
the network, so the shape should be (num classes, test size).<br>
2.2 **Convolutional Neural Network using PyTorch**<br>
• Implement a convolutional neural network(CNN) using PyTorch on the same CIFAR10 dataset. Here
as well split the train data into train and validation sets (10% of data) for hyperparameter tuning.<br>
• The network should contain convolutional, pooling, and fully connected layers. You can experiment
with the number and dimensions of each layer but we expect a minimum of two convolutional layers.
You may also experiment with the activation functions of the neurons, although ReLU being the most
popular one. (Hint - these are the different hyperparameters).<br>
• The convolutional layers would do the feature extraction, but the classification is still being aided by
the fully connected layers, so please don’t forget them.<br>
• Since you do not have to formulate the loss function and the optimization algorithm, do experiment
with the architecture.<br>
• Save the predictions predictions on test set to file “ans2-uni.npy” similar to fully connected neural
network method.<br>
• Describe how the hyperparameter tuning was done, briefly mentioning the experimentation with the
activation functions, optimizers, number of layers,kernel sizes etc. Also state and describe the best
performance network. (This should be included in the notebook itself at the end in a markdown cell.)
This would return the images as tensors. Please note that for the pytorch implementation the tensors
could be directly used however for the vanilla network in Python, the tensors would have to be converted
into numpy ndarrays.<br>

 [[Read_me for CNN](https://github.com/ksw25/Deep-Learning/blob/master/CNN%20and%20Vanilla%20Network/HW1-ksw352/HW1-CNN-ksw352.pdf)]

 [[Read_me for Fullyconnected](https://github.com/ksw25/Deep-Learning/blob/master/CNN%20and%20Vanilla%20Network/HW1-ksw352/HW1-fullyConnected-ksw352.pdf)]
