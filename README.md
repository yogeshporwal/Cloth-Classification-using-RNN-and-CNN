# Cloth-Classification-using-RNN-and-CNN
Cloth Classification on Fashion MNIST Dataset using RNN and CNN with Tensorflow v1

## Project Description

### Dataset: 
Fashion MNIST Dataset. You can load the dataset from tf.keras directly as shown in the following tutorial: https://www.tensorflow.org/tutorials/keras/classification with the following lines of code:

```python 
fashion_mnist = tf.keras.datasets.fashion_mnist
(train_data, train_labels), (test_data, test_labels) =fashion_mnist.load_data()
```

The images are 28x28 NumPy arrays, with pixel values ranging from 0 to 255.

**Class Labels:** Each training and test example is assigned to one of the following labels:

- 0 T-shirt/top
- 1 Trouser
- 2 Pullover
- 3 Dress
- 4 Coat
- 5 Sandal
- 6 Shirt
- 7 Sneaker
- 8 Bag
- 9 Ankle boot

### **Task 1 :**
Create a recurrent neural network with a tensorflow.compat.v1.nn.rnn_cell.RNNCell as a basic component. Use tensorflow.compat.v1.nn.static_rnn to create the RNN. Train it end to end.

### **Task 2 :**
Create a 2D convolutional neural network using tensorflow.compat.v1.layers.conv2d as a basic component. Train it end to end.

## Results 

### RNN:

**Model Specifications:**

| Property                                      | Description |
| ------------------------------------------- | ----------- |
| Hidden state size                                      | 100      |
| Timesteps for unfolding the RNN                                | 28        |
| Loss function | categorical softmax cross entropy with logits |
| Optimizer | Adam |

**Model Hyperparameters:**

| Name                                     | Value |
| ------------------------------------------- | ----------- |
| Learning Rate                                     | 0.001      |
| BasicRNNCell Layers                                | 3        |
| Dropout with Retention Probability | 0.8
| Number of Epochs | 150 |
| Batch Size for Training | 50 |
| Patience for Early Stopping | 10 |
