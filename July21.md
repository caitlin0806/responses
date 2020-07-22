A1) We used the pop function to split the labels from the training set. Species is the name of the labels dataset. 
A2) 5 different estimators: 
1: tf.estimator.DNNClassifier is for deep models that perform multi-class classification.
2: tf.estimator.DNNLinearCombinedClassifier is for wide & deep models.
3: tf.estimator.LinearClassifier is for classifiers based on linear models
4: tf.estimator.WarmStartSettings warm-starts all weights in the model (input layer and hidden weights). The directory or a specific checkpoint can be provided.
5: tf.estimator.RunConfig specifies the configurations for an Estimator run
A3) The purpose of input functions is to supply data for training, evaluating, and prediction. A feature column is an object that describes how the model should use raw input data. The purpose of defining feature columns is that when you build an estimator model, you pass it a list of feature columns that describes each of the features you want the model to use. The tf.feature_column module provides many options for representing data to the model.
A4) The input_fn call is wrapped up in a lambda to capture the arguments while providing an input function that takes no arguments. The steps argument tells the method to stop training after a number of training steps. The nested function is lamba and we are applying it to the training set. 
A5) When the classifier = tf.estimator.DNNClassifier, the set accuracy is 0.933
