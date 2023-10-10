## Building Your First Neural Network with TensorFlow

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
5. `Compile the Model` : Compile the model by specifying the optimizer, loss function, and evaluation metrics:
   ```
    model.compile(optimizer='adam',
                  loss='sparse_categorical_crossentropy',
                  metrics=['accuracy'])
    ```
  6.` Train the Model` : Train your model by usinf the `fit()` function also with speciyinh the epochs:

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
