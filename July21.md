A1) We used the pop function to split the labels from the training set. Species is the name of the labels dataset.

A2) 5 different estimators: 
1) tf.estimator.DNNClassifier is for deep models that perform multi-class classification.
2) tf.estimator.DNNLinearCombinedClassifier is for wide & deep models.
3) tf.estimator.LinearClassifier is for classifiers based on linear models
4) tf.estimator.WarmStartSettings warm-starts all weights in the model (input layer and hidden weights). The directory or a specific checkpoint can be provided.
5) tf.estimator.RunConfig specifies the configurations for an Estimator run

A3) The purpose of input functions is to supply data for training, evaluating, and prediction. A feature column is an object that describes how the model should use raw input data. The purpose of defining feature columns is that when you build an estimator model, you pass it a list of feature columns that describes each of the features you want the model to use. The tf.feature_column module provides many options for representing data to the model.

A4) The input_fn call is wrapped up in a lambda to capture the arguments while providing an input function that takes no arguments. The steps argument tells the method to stop training after a number of training steps. The nested function is lamba and we are applying it to the training set. 

A5) When the classifier = tf.estimator.DNNClassifier, the set accuracy is 0.933 and Prediction is "Setosa" (81.5%), expected "Setosa"
Prediction is "Versicolor" (54.5%), expected "Versicolor"
Prediction is "Virginica" (61.5%), expected "Virginica"

when the classifier = tf.estimator.DNNLinearCombinedClassifier 
when the classifier = tf.estimator.LinearClassifier

B1)
![agehist](https://user-images.githubusercontent.com/67920437/88186090-c0827f00-cc02-11ea-982d-b4493b769a4b.png)
![pairplot](https://user-images.githubusercontent.com/67920437/88187074-1146a780-cc04-11ea-80be-73a2a28dd52a.png)

Above, the 1st picture is a histogram of the age of the passengers on the titanic and the 2nd picture is a pairplot of all the variables. The distribution of age in the pairplot closely resembles the histogram. The majority of people were in their 20-30's and they paid around $50-150 for fare. These people tend to have 0-2 siblings and 0-2 kids. Most of the survivors probably are made up of this age group, especially the women and their kids. 

B2) Dense features can also inspect the result of a specific feature column using the tf.keras.layers.DenseFeatures layer. They only accept dense tensors. To inspect a categorical column you need to transform it to a indicator column first. Categorical columns are just the feature types of the variable (a category). It is used to represent discrete input data with a numerical value. 
What they represent can be exactly the same. Dense features are not stored by defining only the non-zero entries. The 0s are also being stored. However, how they are stored and the efficiency of the implementations differ.

B3) The feature columns are ['sex', 'age', 'n_siblings_spouses' (number of siblings/spouses aboard), 'parch' (number of parents/children aboard), 'fare', 'class', 'deck', 'embark_town' (Port of Embarkation), 'alone']. 
Dense features include [‘age’, ‘n_siblings_spouses’, ‘parch’, ‘fare’].
Categorical features include [‘sex’, ‘class’, ‘deck’, ‘embark_town’, ‘alone’]
The purpose of adding a cross featured column to the model is to learn the differences between different feature combinations.

The original accuracy was 0.7537879 and the loss was 0.46544266 which is not good at all. 


{'accuracy': 0.7765151', 'accuracy_baseline': 0.625, 'auc': 0.83474135, 'auc_precision_recall': 0.79513633, 'average_loss': 0.47293583, 'label/mean': 0.375, 'loss': 0.46544266, 'precision': 0.67346936, 'prediction/mean': 0.38475904, 'recall': 0.6666667, 'global_step': 200}


Now the accuracy is 0.7765151 and the loss is 0.46027577. So, the accuracy did increase and loss d ecreased, suggesting that the model is getting better but it still has a long way to go. 


{'accuracy': 0.7765151, 'accuracy_baseline': 0.625, 'auc': 0.8518519, 'auc_precision_recall': 0.79191834, 'average_loss': 0.46924594, 'label/mean': 0.375, 'loss': 0.46027577, 'precision': 0.73255813, 'prediction/mean': 0.33667478, 'recall': 0.6363636, 'global_step': 200}

![Unknown](https://user-images.githubusercontent.com/67920437/88190847-c5e2c800-cc08-11ea-93e1-dafa03387dad.png)
![Roc](https://user-images.githubusercontent.com/67920437/88188853-61bf0480-cc06-11ea-8243-96e463684a63.png)
