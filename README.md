# fBm-FLNN
fBm FLNN

The code defines a class FluidLatticeNeuralNetwork, which represents a neural network with fluid lattice architecture.

The constructor of the FluidLatticeNeuralNetwork class takes three parameters: layerSizes, learningRate, and fBmScale. layerSizes is a vector that specifies the number of neurons in each layer of the network. learningRate determines how quickly the network learns during training. fBmScale is a parameter that controls the magnitude of the fractional Brownian motion (fBm) values generated during training.

The predict function takes an input vector and returns the output vector generated by the neural network. It iterates through the layers of the network, computing the activations of each neuron based on the weighted sum of the previous layer's activations. The activation function used is the Rectified Linear Unit (ReLU), which returns the maximum of 0 and the input value.

The train function trains the neural network using the provided inputs and targets. It performs forward propagation to calculate the predicted outputs and then backpropagation to update the weights based on the prediction errors. The training is performed for the specified number of epochs. The error is calculated as the mean squared difference between the predicted outputs and the target outputs.

The initializeWeights function initializes the weights of the neural network. It sets up the weight matrices with random values drawn from a normal distribution with mean 0 and standard deviation 1. The scale of the weights is determined using the Xavier initialization method, which helps with the convergence of the network.

The calculateError function calculates the error between the predicted outputs and the target outputs. It uses the mean squared error as the error metric.

The saveWeightsToFile function saves the trained weights to a file. It writes the weight values of each layer to the file.

The loadWeightsFromFile function loads the weights from a file. It reads the weight values from the file and assigns them to the weight matrices of the neural network.

The generatefBm function generates a fractional Brownian motion (fBm) value using a multi-layered fBm process. It iteratively adds fBm values with decreasing amplitude and increasing frequency. The persistence parameter controls the decay of amplitude, and the fBm scale parameter determines the overall magnitude of the fBm values.

The generateNoise function generates random noise values using a uniform distribution between -1 and 1, which are used in the fBm generation process.

In the main function, an instance of the FluidLatticeNeuralNetwork class is created. The network is trained on a set of inputs and target outputs for a specified number of epochs.

After training, an example usage is shown where an input vector is passed to the network's predict function, and the predicted output is printed.

Overall, this code implements a fluid lattice neural network and trains it using the specified inputs and targets. The weights are updated using backpropagation, and the training progress is displayed. The fBm generation is integrated into the weight update step, allowing the network to learn with the addition of fBm values.
