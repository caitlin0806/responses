I.A. The data is split into testing and training because test data is supposed to be data that is given and the training data is supposed to be data that the model hasn’t seen yet so that you can see how good the model is at classifying the values. 

I.B. Relu only passes values of 0 or greater to the next layer in the network. Softmax takes the biggest value from a set (output of layer). Then it transforms the set into all zeros except the biggest which is transformed into 1. There are 10 neurons in the final layer because there 10 digits and the number of neurons in the final layer should be the number of classes you are classifying for. 

I.C. The loss function measures accuracy of the model during training. So, minimizing the loss function makes the model better. The optimizer is how the model is updated based on the data and loss function.

I.D. 
1) 60000 images 28 by 28 pixels
2) 60000
3) 10000 images 28 by 28 pixels
4) array output:  [[9.6861429e-11 4.3787887e-07 9.9999952e-01 1.0604523e-09 1.2526731e-16
  3.6759984e-10 2.3595672e-11 1.7706627e-14 8.6952684e-10 1.8218145e-17]]

