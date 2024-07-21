# MNIST Neural Network

The Mnist dataset is a collection of 60 thousand 28x28 handwritten digits which is commonly used to train basic neural networks in image classification. 

In this project I coded from scratch a neural network to classify the handwritten digits. 
Key elements in the neural network include:
* Backpropagation
* Momentum
* Batch Training
* decreasing learning rate
* Flexibility to easily change the number of layers as well as the activation function (ReLU or softmax) and the size of each layer
* Cross-entropy (for this reason the last layer should be a softmax activation function)
* Data saver for the weights and biases
* Data loaded to load in previous weights and biases

# Problems Encountered

Although the neural network was classifying the MNIST handwritten digits well, it was overfitting the data and unable to classify my handwritten digits. To fix this I added a randomize function to the mnist dataset which rotates, translates, and adds noise to each number so that the network learns more general patterns. While the model is training a screen is displayed where you can press 'c' to see what the numbers in the mnist dataset look like before and after randomization.

# User Interface

There is also an option to draw numbers where you can draw your own number (setting drawing = true) and have the program classify it for you, the output is a probability distribution of what number it thinks it most likely is. To clear the screen you can press 'c'.

When the neural network is training you a window opens which displayes a MNIST number and the corresponding number when put through the ranodmized function. To get a new number you can press 'c'.

# Results 

The classification after training is far from perfect, where training on mnist data gets around 95% but randomized mnist data gets up to 60-70%, further improvements can be added by extending it to a convolutional neural network.

# Variables you can change

In ReadingNumbersTesting (the main class) there is a list of global variables which can be altered to change the model, these include:

* batchAmount - the sample size it takes from the dataset before applying backpropagation
* learningRate - can be thought of how big a step is being took in the direction of the gradient, note that in the code the learning Rate decreases once a plateau is reached
* hiddenLayerNodes - the size of each vector throughout the neural network. It should start with 784 (since its a 28x28 image) and end with 10 (since there are 10 possible outputs). Ex: {784, 400, 200, 10}
* layerType - possible to choose between a softmax activation function (0) or ReLU activation function (1), as noted above softmax activation function must be on the output layer. Ex: if the layer nodes are as above, a possible layerType array could be {1,1,0}
* files - list of files for where the data of each layer will be saved
* loadData - if you already have a list of files you want to load, then this should be true, else false
* drawing - if you want to test the neural network by drawing your own image, then both loadData and drawing should be true
