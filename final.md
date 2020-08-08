**Problem Statement**
The topic I chose to do was image classification on weather using convolutional neural networks. My objective is to use CNNs to correctly classify the type of weather an image belongs to. Depending on the complexity of this idea, image classification on weather is important because improving computer vision on things such as bad weather and limited visibility caused by weather like heavy rain, snow, or fog is crucial for things such as driving assistance. To improve machine vision in bad weather situations, a reliable detection system is necessary as a ground base. I want to see how well of a CNN model I can build and how accurately can I correctly classify images. 

**Data**
I used data from a multi-class weather dataset for image classification of still images. The dataset provides a platform for outdoor weather analysis by extracting various features for recognizing diferent weather conditons. It includes 1122 google stock images of different types of weather that falls into 4 categories: cloud (300), rain (212), sunrise (357), and shine (253). 

**Method**
When I downloaded the dataset, I split the dataset folder into 4 different subfolders within it that each corresponded to the type of class. After that, I made all the images the same size at 300x168 pixels. Then, I made code to import my data into pycharm. Next, I split my data into 80% training and 20% testing. I plotted the first 9 images of my training set to see the different classifications coresspond to an image seen here: ![first9trainingset](https://user-images.githubusercontent.com/67920437/89699404-b051eb80-d8f4-11ea-8a3c-8f7201384a5e.png). Now I configure the dataset for performace and standardize my images. I start building my first CNN model seen here: 
<img width="742" alt="Screen Shot 2020-08-08 at 1 24 44 PM" src="https://user-images.githubusercontent.com/67920437/89716414-bab6c880-d97a-11ea-9429-58fd1ecf8981.png">.
I used 3 Conv2D layers, 3 MaxPooloing layers, 1 Flatten , and 2 Dense layers. I selected relu for my activation since it allows for faster and more effective training of deep neural networks. I compiled the model using adam as the optimizersince Adam combines the best properties of the AdaGrad and RMSProp algorithms to provide an optimization algorithm that can handle sparse gradients on noisy problems. I used SparseCategoricalCrossentropy for the loss function to compute the crossentropy loss between the labels and predictions and this one is used for when there or 2 or more label classes. For the metrics, I used accuracy as my goal is to produce the highest accuracy. Finally, I fitted the model with a batch size of 32 and 10 epochs. My results included:![trainvalaccloss](https://user-images.githubusercontent.com/67920437/89699406-b0ea8200-d8f4-11ea-92ad-fa48dfda8c40.png).
My training accuracy was 94% and my testing accuarcy was 80%. In the graph you can see the training accuracy being a lot higher than the validation accuracy, the training loss is lower than the testing loss, and the fluctuation of the accuracies. These are all strong indicators that the model is well overfit. To combat the overfitting, I took my CNN model and added data augmentating and a Dropout layer since these are common ays to decrease the overfitting as seen here: <img width="742" alt="Screen Shot 2020-08-08 at 1 25 30 PM" src="https://user-images.githubusercontent.com/67920437/89716411-b9859b80-d97a-11ea-898f-c52ce61cea46.png">.
Then i compiled and fitted the model with the same arguments and got a little bit of better results as seen here: ![trainvalaccloss1](https://user-images.githubusercontent.com/67920437/89699407-b0ea8200-d8f4-11ea-8b62-83040bb6ff50.png).
My training accurcy became 87% and my testing accuracy became 83%. So, the model is still overfit but not as much as before. These were the best results I could get at this time. Moving on, I decided to look up a few images on google that fall into the 4 different categories and decided to test my model on it to see how well it would do. my results included:

![cloud1](https://user-images.githubusercontent.com/67920437/89699066-9ca58580-d8f2-11ea-87cb-d6b181eb86c4.jpg)
Cloud1: This image most likely belongs to shine with a 34.94 percent confidence.

![cloud2](https://user-images.githubusercontent.com/67920437/89716757-bf30b080-d97d-11ea-8277-12c387405d75.jpg)
Cloud2: This image most likely belongs to shine with a 70.09 percent confidence.

![rain1](https://user-images.githubusercontent.com/67920437/89699068-9d3e1c00-d8f2-11ea-831f-7e074c327a4b.jpg)
Rain1: This image most likely belongs to rain with a 100.00 percent confidence.

![rain2](https://user-images.githubusercontent.com/67920437/89699069-9dd6b280-d8f2-11ea-95b8-29bde557b967.jpg)
Rain2: This image most likely belongs to rain with a 100.00 percent confidence.

![shine1](https://user-images.githubusercontent.com/67920437/89699070-9e6f4900-d8f2-11ea-87c9-976648f28576.jpg)
Shine1: This image most likely belongs to sunrise with a 96.31 percent confidence.

![shine2](https://user-images.githubusercontent.com/67920437/89699071-9f07df80-d8f2-11ea-8b75-df9ee7d2725e.jpg)
Shine2: This image most likely belongs to sunrise with a 85.76 percent confidence.

![sunrise1](https://user-images.githubusercontent.com/67920437/89699073-9f07df80-d8f2-11ea-9b89-613d0c547432.jpg)
Sunrise1: This image most likely belongs to sunrise with a 99.83 percent confidence.

![sunrise2](https://user-images.githubusercontent.com/67920437/89699074-9fa07600-d8f2-11ea-9305-ce65578ab6f5.jpg)
Sunrise2: This image most likely belongs to sunrise with a 100.00 percent confidence.


As you can see, my model correctly identified the 2 rain images, and sunrise images. The model incorrectly identified both cloud images to be in the shine category and it incorrectly indentified the 2 shine images to be in the sunrise category.

**Conclusion**
If I had more time and did more trial and error, I am sure I could get better accuracies and less overfitting so that my model can run more efficiently. I do think my model did pretty well, however. I think I would also try different weather categories like snow. I would also like to increase the number of photos for each category so that it can have a wide variety of range of the different categories. Based of my results, it seems my model was getting the cloud images wrong probably due to the fact that it is a beautiful day and there's light outside, making it think that it shine. And it was probably getting my shine pictures wrong because it saw the sun and classified it as sunrise. So picking categories that are more different would be another thing I would like to do. 


**References**
Ajayi, Gbeminiyi. “Multi-Class Weather Dataset for Image Classification.” Mendeley Data, Mendeley Data, 13 Sept. 2018, data.mendeley.com/datasets/4drtyfjtfy/1.
Ajayi, Gbeminiyi. “Multi-Class Weather Dataset for Image Classification.” Mendeley Data, Mendeley Data, 13 Sept. 2018, dx.doi.org/10.17632/4drtyfjtfy.1.
“Image Classification  :   TensorFlow Core.” TensorFlow, www.tensorflow.org/tutorials/images/classification.

**Related Works**
https://www.mrt.kit.edu/z/publ/download/Roser_al2008iv.pdf
https://www.researchgate.net/publication/331353178_Weather_Classification_using_Convolutional_Neural_Networks



