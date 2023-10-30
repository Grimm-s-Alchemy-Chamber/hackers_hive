## Building Your First Neural Network with TensorFlow

![alt text](https://miro.medium.com/max/4556/1*L049OsPATvKKUA1yq95Jsg.png)
1. `Installation` : First install tensorflow using the command in command prompt:
   
   ```
   pip install tensorflow
   ```
2. `Import tensorflow in your file or Notebook` : Import tensorflow in your python file or Notebook by writing this command:
   
   ```
   import tensorflow as tf
   ```
3. 'Prepare the data` : You will need a data to train and test your neural network model.Tensorflow has various functions and tools for data manipulation and processing.You can start by using datasets like MNIST for digit recognition.
4. `Building the model` : After the data preparation and processing is done,we go ahead to building the model using the `tf.model.Sequential`.A basic neural netwoek will look like as given below :
   
   ```
   model = tf.keras.Sequential([
    tf.keras.layers.Flatten(input_shape=(28, 28)),  # Input layer (flatten 28x28 images)
    tf.keras.layers.Dense(128, activation='relu'),  # Hidden layer with 128 neurons and ReLU activation
    tf.keras.layers.Dense(10, activation='softmax') # Output layer with 10 neurons (for classification) and softmax activation
   ])
   ```
   #### Explanation:
      1. `tf.keras.Sequential` is a class in TensorFlow's high-level neural networks API, Keras, which is commonly used to build and train deep learning models. It provides a straightforward way to create a linear stack of layers in a neural network.
      2. `tf.keras.layers.Flatten` is a layer in TensorFlow's Keras API that is used to flatten the input data. It is often employed as the first layer in a neural network model, especially when working with structured or image data that needs to be transformed from a multi-dimensional shape into a one-dimensional vector.
      3. `tf.keras.layers.Dense` is a fundamental layer in TensorFlow's Keras API that implements a fully connected or densely connected neural network layer. It's commonly used for building feedforward neural networks, including multi-layer perceptrons (MLPs). This layer connects every neuron in the current layer to every neuron in the subsequent layer.
      4. `activation=` An activation function introduces non-linearity to a neural network, allowing it to model complex relationships in data. Without activation functions, a neural network, no matter how many layers it has, would be reduced to a linear regression model because it would be a linear combination of its input data.
      5. `ReLU` is one of the most widely used activation functions. It's defined as f(x)=max(0,x), which means that if the input is greater than zero, it remains unchanged, but if it's less than zero, it becomes zero.
      6. The `softmax` activation function is often used in the output layer of multi-class classification models. It transforms a vector of real numbers into a probability distribution, where each value represents the probability of belonging to a specific class.
  
  
6. `Compile the Model` : Compile the model by specifying the optimizer, loss function, and evaluation metrics:
   ```
    model.compile(optimizer='adam',
                  loss='sparse_categorical_crossentropy',
                  metrics=['accuracy'])
    ```
   #### Explanation:
      1. An `optimizer` is a crucial component in training machine learning and deep learning models. Its primary function is to minimize a loss function by adjusting the model's parameters (weights and biases) during the training process. Optimizers use various techniques to update these parameters iteratively, and the choice of optimizer can significantly affect the training speed and the final model's performance.
      2. `adam` is a popular and effective optimization algorithm used for training neural networks. It combines ideas from two other optimizers, RMSprop and Momentum, to achieve efficient convergence during training
      3. `loss` refers to a measure of how well a model's predictions match the actual target values in the training data. It quantifies the error or the difference between what the model predicts and what it should predict. The goal during the training process is to minimize this loss because a lower loss indicates better alignment between the model's predictions and the actual data.
      4. `sparse_categorical_crossentropy` is a loss function used for classification tasks when the target labels are represented as integers (sparse labels) and is often used in neural network models with softmax activation in the output layer.
      5. The function `metrics` is used to specify which evaluation metrics should be computed and displayed during the training process.
      6. `accuracy` is a common evaluation metric for classification tasks. It measures the proportion of correctly classified examples (both true positives and true negatives) out of the total number of examples. In other words, accuracy tells you how often the model's predictions match the actual labels.
   
  6.` Train the Model` : Train your model by using the `fit()` function also with specifying the epochs,The term `epochs` refer to the number of times the entire training dataset is passed forward and backward through a neural network.

    ```
    model.fit(x_train, y_train, epochs=5) 
    ```
    
7. `Evaluate the Model peroformance ` : Evaluate the model performance and accuracy with `evaluate` funtcion:
    ```
    test_loss, test_accuracy = model.evaluate(x_test, y_test)
    print(f"Test accuracy: {test_accuracy}")
    ```
    
8.  `Make predictions` : Make predictions in unknown dataa using the `predict` function :
    ```
    predictions = model.predict(x_new_data)
    ```
    
9. `Fine-Tuning and Experimentation` : As you become more comfortable with TensorFlow, you can experiment with different neural network architectures, activation functions, optimizers, and hyperparameters to improve your model's performance.
