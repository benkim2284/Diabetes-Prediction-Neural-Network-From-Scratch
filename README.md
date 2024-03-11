# Diabetes Prediction Neural Network From Scratch
I developed a two-layer neural network from scratch to predict diabetes onset. Leveraging the Leaky ReLU and sigmoid activation functions enabled effective binary classification. Utilizing the binary cross-entropy loss function, I was able to facilitate accurate gradient calculations and enable successful implementation of backpropagation. After iteratively updated the weights and biases, I was able to achieve an `80%` training accuracy and `78%` testing accuracy. 

## Overall Structure
I decided to create a two layer neural network, with the middle layer having 25 nodes, and the output having one node. For the middle layer's activation function, I decided to use the `leaky reLU` (leaky rectified linear unit) activation function rather than just the standard reLU in order to prevent any vanishing gradient issues during the training process. The outer layer's activation function is the `sigmoid` function, which is effective for binary classification.  

## Data Preprocessing
Before using the dataset to train the model, I first confirmed that there were no NaN values. However, the dataset did contain 0 values in certain columns where such values are physiologically improbable. For example, it would be highly unusual to observe a blood pressure or BMI of 0. To combat this, I used a KNN Imputer to impute these "missing values". 

## Building the Neural Network
### Neural Network Math
In order to simplify the math process later on and to save myself a headache, I decided to outline the math for the forward and backward propagation cycles.
<br />
<br />
<img src="https://github.com/benkim2284/Diabetes-Prediction-Neural-Network-From-Scratch/assets/114448555/06f6fa23-1527-4f7d-812b-6fc389d32031" width="400"/>
<img src="https://github.com/benkim2284/Diabetes-Prediction-Neural-Network-From-Scratch/assets/114448555/2c65a347-1a08-4124-ad70-82a8dd4d5f6c" width="384"/>

### Forward Propagation
For the forward propogation cycle, I mainly labeled my matrices: 
* `x` is the input matrix
* `w` is the weight matrix
* `b` is the bias matrix
* `z` is the dot product of the input and weight plus the bias
* `a` is the result of applying the activation function to `z`
* `y_hat` is the predicted output

### Backward Propagation
For the loss function, I decided to use the binary `cross-entropy loss function` to essentially fuel my backpropagation cycle. I calculated each gradient that I would need by utilizing the chain rule (everyone's favorite), and by doing this, I was able to simplify some of the equations which was pretty satisfying. Also, I was able to analyze each matrix dimension for the various equations and determine which matrices to transpose in order to get consistent dimenions for the gradient and its corresponding variable. For example, dw2 and w2 would have to have the same dimensions, as well as db2 and b2.

## Results
<img src="https://github.com/benkim2284/Diabetes-Prediction-Neural-Network-From-Scratch/assets/114448555/0e3879be-966e-4e27-bf0d-3552ad5bbf48" width="600">
<br />
<br />

After experimentation with:
* various imputation methods
* the number of nodes in the hidden layer
* the learning rate
* the number of epochs
* and much more...

I was able to achieve a training accuracy of `80%` and a testing accuracy of `78%`. Overall, the model had good statistical generalization, as it was able to generalize well to the testing data. 
<br />
<br />
`I give this a 10/10 learning experience, would recommend 👍!`




