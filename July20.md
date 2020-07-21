Responses
A. Write a Problem Statement. Introduce your topic, quantify its significance, and describe the problem as a process. 
Identify and quantify significant obstacles to solving your problem. 
Demonstrate why your topic is important, and why the obstacles associated with your topic are significant both globally as well as within the context of your selected application.
Describe and analyze the complex nature of the process you are investigating, including the system, the environment, agents and networks. 
Describe and analyze scope, scale and hierarchy of processes and sub-processes. 
Describe and analyze factors that contribute to quantified obstacles.
Describe and analyze process oriented causes-effect relationships.

A. I plan on creating a neural network to make prediction on criminal behavior based on the history of the arrest bookings. I want to use machine learning to help classify criminal behavior. 


1. The optimizer selected was the RMSprop. Rprop and Adagrad are other optimizers. RMSprop is the adaptation of rprop algorithm for mini-batch learning. RMSprop also has similarities with Adagrad. It is viewed as a way to deal with its radically diminshing learning rates. Rprop doesnt really work with large datasets. RMSprop is similar to Adagrad as it still keep the same estimate of squared gradients, but instead of letting that estimate continually accumulate over training, we keep a moving average of it.  

2. The loss function chosen was the binary_crossentropy. We used this loss function because we are training a binary classifier (cat or dog). If the probability associated with the true class is 1.0, we need its loss to be zero. Conversely, if that probability is low, we need its loss to be huge. Taking the negative log of the probability will help penalize bad predictions.  

3. the metric=argument sets up parameters to judge how well the model is working. It is similar to loss functions, but the results from evaluating a metric aren't used when training the model.  

4. 

![figure 1](https://user-images.githubusercontent.com/67920437/88005422-633ddf00-cad7-11ea-8abe-f119d9a10925.png)

![figure 2](https://user-images.githubusercontent.com/67920437/88005424-646f0c00-cad7-11ea-97a9-c113a7d2f95f.png)

The model is definitely overfit. The val_loss was decreasing from the 12th-14th epoch and then on the last epoch it increased. This is a clear indication that the model is overfit. The accuaracy of the training set was .97 so it learned the training set too well. 

![chow chow](https://user-images.githubusercontent.com/67920437/88006327-5cb06700-cad9-11ea-8361-1b51cc8a447e.jpeg)
predicted correct

![husky](https://user-images.githubusercontent.com/67920437/88006332-62a64800-cad9-11ea-97ae-a35eeed0a0eb.jpeg)
predicted correct

![pitbull](https://user-images.githubusercontent.com/67920437/88006395-88335180-cad9-11ea-8e0c-530c3599e77a.jpeg)
predicted correct

![tabby](https://user-images.githubusercontent.com/67920437/88006400-89fd1500-cad9-11ea-8623-f5df8754587f.jpeg)
predicted correct

![siamese](https://user-images.githubusercontent.com/67920437/88006404-8b2e4200-cad9-11ea-8924-9a17fcba13a8.jpeg)
predicted correct

![persian](https://user-images.githubusercontent.com/67920437/88006406-8c5f6f00-cad9-11ea-94c8-5f6683f0f417.jpeg)
predicted correct

The model did accurately classify all my pictures. Since the model is overfit, I suggest that we reduce the network's capacity by removing layers, apply regularization by adding a cost to the loss function for large weights, and use dropout layers. 

