# Custom Gradient for Rectified Linear Unit (ReLU) Activation Function in TensorFlow

This repository provides an example of implementing a custom gradient for the Rectified Linear Unit (ReLU) activation function in TensorFlow. 
Although TensorFlow supports ReLU out of the box, this example demonstrates how to create a simplified custom version of ReLU using TensorFlow's custom gradient feature.

## Requirements

- TensorFlow 2.x
- Keras

## Files

- `custom.ipynb`: Jupyter notebook demonstrating the usage of the custom ReLU activation function in a Sequential model.

## Implementation

### Custom ReLU Activation Function

The custom ReLU activation function is defined in `custom.ipynb`. The ReLU function is defined as:

```python
def custom_relu(x):
  return tf.maximum(0., x)

def custom_relu(x):
  return tf.maximum(x, 0.0)

def custom_relu_grad(x):
  return tf.where(x > 0, tf.ones_like(x), tf.zeros_like(x))

@tf.custom_gradient
def custom_relu_op(x):
 y = custom_relu(x)
 def grad(dy):
   return custom_relu_grad(x) * dy
 return y, grad

```
## Usage in Sequential Model
The custom ReLU activation function can be used in a Sequential model in TensorFlow and Keras. 

## Read My Article
For a deeper understanding of custom gradients in TensorFlow, please read my article available at : https://www.geeksforgeeks.org/custom-gradients-in-tensorflow/

## Model A (Default ReLU):
`Test Accuracy:` 0.9751999974250793
## Model B (Custom ReLU): 
`Test Accuracy:` 0.9776999950408936
