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

The custom ReLU activation function is defined in `custom_relu.py`. The ReLU function is defined as:

```python
def custom_relu(x):
    return tf.maximum(0., x)
```
## Usage in Sequential Model
The custom ReLU activation function can be used in a Sequential model in TensorFlow and Keras. 
