A1) The ImageDataGenerator() command is a class that let's you instantiate generators of augmented image batches via .flow(data, labels) or .flow_from_directory(directory). The argument used the rescale parameter so that the data can be normalized and range from 0 to 1. It takes data generators as inputs. Target_size is important because you could be using different sized images and inputing a target_size allows all the images to be of the same size when running code. For this example, the class mode should be binary since when are dealing with 2 classes then we can end the network with a sigmoid activation so that the output will be a single scalar between 0 and 1. You would want to reference the validation directory. The ImageDataGenerator() and .flow_from_directory() will differ depending on if you are referenicng the training or testing batch since they are in two different places. the arguments are different as well. The ImageDataGenerator() takes the rescale argument and .flow_from_directory() takes a directory argument as others mentioned above like target_size and class_mode. 

A2) The horses and humans CNN has 3 Conv2D layers, 3 MaxPooling2D layers, 1 Flatten layer, and 2 Dense layers. The model lets you input any image and the model changes the size of the image so that everything is the same size. It then uses the training and testing set and based off of that data it calculates whether or not the image is a horse or not. The filters double every layer in the output and the image's pixels decrease by half after the MaxPooling2D. I used the sigmoid activation since it is a binary classifaction and the output will be a single scalar between 0 and 1 (ie horse or not). In the model comiler I used binaray_crossentropy for the loss, accuracy for metrics, and RMSprop(lr=0.001) for the optimizer. 


B1)
![pairplot](https://user-images.githubusercontent.com/67920437/87739195-43dc4480-c7ad-11ea-84a6-d4240eee62f8.png)
This pairplot can be used to see which variables are correlated more than other variables with each other. Displacement vs weight has strong positive correlation. Displacement vs MPG and weight vs MPG has a strong negative correlation. The diagonal access represents the distributuion of the variables to itself. It describes the relationship between the variables. 

B2)
![plot](https://user-images.githubusercontent.com/67920437/87740160-8141d180-c7af-11ea-8990-71bfa4a7412c.png)

Based off of the tail of the dataframe, the model is overfit. This is because as the epochs increase, the val_loss decreases and then increases on the loss epoch which is a common consequence of overfitting. The model looks like is improving but around the 997th epoch it seems to be too accurate so the callback is happening so that the accuracy can lower. So, the model would work better if we decreased the epochs. 


C1) 
The significance of comparing the 4 different sized models is to show the effects of overfitting and underfitting by using different parameters. Since there is no magic formula to determine the parameters to use for a model so that it is perfect and not overfit/underfit you need to experiment with different variables to see what will give the best results. It was revealed that the tiny model avoids being overfit and the larger models are indeed overfit. 
![graph 1](https://user-images.githubusercontent.com/67920437/87740739-f19d2280-c7b0-11ea-83b1-a72efb5b9680.png)

