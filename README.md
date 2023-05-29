### Convolutional Neural Network (CNN) Operations

This repository provides Python implementations of key operations for Convolutional Neural Networks (CNNs). It includes implementations for both the forward and backward passes of the following operations:

#### Convolution Layer

The `convolution_layer` class implements the forward and backward passes for a convolution layer in a CNN. It supports convolution between a single-channel input and multiple-channel output. The layer takes in the height and width of the input image, the number of output channels, the number of input channels, and the dimensions of the kernel. The forward pass performs the convolution operation, while the backward pass computes the gradients and updates the weights and biases.

#### Flatten Operation

The `flatten` class implements the flatten operation in a CNN. It converts the multi-dimensional output from the convolution layer into a flattened vector while preserving the order of elements.

#### Training on MNIST Dataset

This repository also includes an example of training a CNN on the MNIST dataset. The CNN architecture consists of two layers:

1. Convolution Layer:
   - Utilizes 16 output channels.
   - Applies the Tanh activation function to the output.
   - Uses the implemented forward and backward passes for efficient computation.
   
2. Fully Connected Layer:
   - Consists of 10 output neurons with a linear activation function.
   - Transforms the input from the previous layer into a probability distribution over classes.
   
The CNN is trained using the softmax cross-entropy loss function, which optimizes the network's parameters to minimize the classification error. The implemented stochastic gradient descent (SGD) algorithm is used for training.

To train the CNN on the MNIST dataset, the `sgd_q6` function is provided. It performs the forward and backward passes for each training sample, updates the weights and biases, and calculates the loss values. After training, the overall loss is calculated to evaluate the model's performance.

Please refer to the code in this repository for detailed implementations and usage examples. Feel free to explore and modify the code to suit your specific needs.
