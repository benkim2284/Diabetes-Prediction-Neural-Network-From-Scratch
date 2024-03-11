# Diabetes Prediction Neural Network From Scratch
I developed a two-layer neural network from scratch to predict diabetes onset. Leveraging the Leaky ReLU and sigmoid activation functions enabled effective binary classification. Utilizing the binary cross-entropy loss function, I was able to facilitate accurate gradient calculations and enable successful implementation of backpropagation. After iteratively updated the weights and biases, I was able to achieve an `80% training accuracy rate` and `78% testing accuracy rate`. 

## Overall Structure
I decided to create a two layer neural network, with the middle layer having 25 nodes, and the output having one node. For the middle layer's activation function, I decided to use the leaky reLU (leaky rectified linear unit) activation function rather than just the standard reLU in order to prevent any vanishing gradient issues during the training process. The outer layer's activation function is the sigmoid function, which is effective for binary classification.  


## Building the Neural Network
<img src="https://github.com/benkim2284/Diabetes-Prediction-Neural-Network-From-Scratch/assets/114448555/06f6fa23-1527-4f7d-812b-6fc389d32031" width="400"/>
<img src="https://github.com/benkim2284/Diabetes-Prediction-Neural-Network-From-Scratch/assets/114448555/2c65a347-1a08-4124-ad70-82a8dd4d5f6c" width="384"/>
<br />
<br />


In order to simplify the math process later on and to save myself a headache, I decided to outline the math for the forward and backward propagation cycles. For the forward propogation cycle, I mainly labeled my matrices: 
* `x` is the input matrix
* `w` is the weight matrix
* `b` is the bias matrix
* `z` is the dot product of the input and weight plus the bias
* `a` is the result of applying the activation function to `z`
* `y_hat` is the predicted output
<br />

For the loss function, I decided to use the binary cross-entropy loss function to essentially fuel my backpropagation cycle. I calculated each gradient that I would need by utilizing the chain rule (everyone's favorite), and by doing this, I was able to simplify some of the equations which was pretty satisfying. Also, I was able to analyze each matrix dimension for the various equations and determine which matrices to transpose in order to get consistent dimenions for the gradient and its corresponding variable. For example, dw2 and w2 would have to have the same dimensions, as well as db2 and b2. 







