# Diabetes Prediction Neural Network From Scratch
I developed a two-layer neural network from scratch to predict diabetes onset. Leveraging the Leaky ReLU and sigmoid activation functions enabled effective binary classification. Utilizing the binary cross-entropy loss function, I was able to facilitate accurate gradient calculations and enable successful implementation of backpropagation. After iteratively updated the weights and biases, I was able to achieve an 80% training accuracy rate and 78% testing accuracy rate. 

<br />

# Building the Neural Network
In order to simplify the math process later on and to save myself a headache, I decided to outline the math for the forward and backward propagation cycles. For the forward propogation cycle, I mainly labeled my matrices: `x` is the input, `b`'s are the biases, `z`'s are the dot product of the input and weight plus the bias, `a`'s are the result of applying the activation function to the z's, and `y_hat` is the predicted output.

<br />

<img src="https://github.com/benkim2284/Diabetes-Prediction-Neural-Network-From-Scratch/assets/114448555/06f6fa23-1527-4f7d-812b-6fc389d32031" width="500"/>
<img src="https://github.com/benkim2284/Diabetes-Prediction-Neural-Network-From-Scratch/assets/114448555/2c65a347-1a08-4124-ad70-82a8dd4d5f6c" width="500"/>




