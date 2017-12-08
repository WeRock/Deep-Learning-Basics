# Deep Learning with Tensorflow
### Neurons
### Hidden Layers
These are generally Dense / Fully Connected Layers

#### Activation functions: 
These determine when the neuron will fire
  * Perceptron (Binary or Bipolar activation i.e. (0,1) or (-1,1))
  * Sigmoid (gradual transition between 0 to 1) 1/(1+e**-x)
  * tanh (hyperbolic tangent)
  * ReLu (Relative linear unit)
#### Cost Functions
These determine how well the neuron is performing
* Quadratic (Mean squared error)

	C = Σ (y - y<sup>'</sup>)<sup>2</sup> / n
* Cross Entropy

	C = - 1 / n Σ (y * ln(y<sup>'</sup>) + (1 - y<sup>'</sup>) * ln(1 - a))
#### Learning functions
These determine how the model will learn. In case of neural networks it determines the weights and biases so that the **cost** is minimum.

**Gradient Descent** is one approach for minimizing cost. It takes small steps towards the direction where the value decreses (global minima). This is done by taking slope (derivative) of cost function and then move towards the direction where slope decreases. Ideal scenario would be the global minima where the slope/tangent is **ZERO** (or the tangent at that point is parallel to horizontal axis). 

![alt text](https://mandrostorage.blob.core.windows.net/blogfiles/Stratosphere.MachineLearning.Studio_2016-03-17_20-28-45.png "Gradient descent")

#### Back Propagation
Determine the results using Gradient Descent and Cost Functions and propagate back the error to adjust the weights and biases and try with new batch of features. This is repeated multiple times to obtain closer to actual values.

### Output Layer
Collects the output from previous layer and presents as a probability vector with each item stating the probability for the classified class. Also known as softmax layer.
* Softmax Regression
	
    p<sub>i</sub> = e<sup>u<sub>i</sub></sup> / Σ<sub>j</sub> (e<sup>u<sub>i</sub></sup>)
	
### Max Pooling Layer
Converts a large feature set into a smaller one using some approximations
### Flattening Layer
Converts a higher dimension feature set into a lower dimension featureset (2D to 1D array)
### Convolutional Layer
