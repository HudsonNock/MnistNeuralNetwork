# MnistNeuralNetwork

What is the Mnist Dataset?

The Mnist dataset is a collection of 60 thousand 28x28 handwritten digits which is commenly used to train basic neural networks in image classification. 

In this project I coded from scratch in java a neural network which uses back propagation to update the weights and baises. It is flexable enough that you can easily
enter in the number of layers wanted as well as the activation function (ReLU vs softmax) for each layer and the size of each layer, although since the score is based
on cross-entropy, the last layer should be a softmax activation function. It also allows data to be loaded into each layer where the weights of the layer are stored 
in a file row-based (thinking of the weights as a matrix) and the baises are stored in the same file after the weights.

I noticed that the network overfits data from the mnist dataset and so added a randomize function to the mnist dataset which rotates, translates, and adds noise to
each number so that the network learns more general patterns. While the model is training a screen is displayed where you can press 'c' to see what the numbers
in the mnist dataset look like before and after randomization.

There is also an option to draw numbers where you can draw your own number and have the program classify it for you, the output is a probability distribuation 
of what number it thinks it most likely is.

The classification after training is far from perfect, where training on mnist data gets around 95% but randomized mnist data gets up to 60-70%, further improvments can
be added by extening it to a convalutional neural network, however, for now I am satisfied with the progress I made and don't have time to continue adding to the project.
