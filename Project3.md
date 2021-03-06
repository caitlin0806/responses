For this project, we were given 10,000 images that were 480x480 pixels of Korle Gonno, Accra. The images were of population counts in the town. We were also given a csv file that contained an array of labels that corresponded to each image and the second column provided counts of the people that resided in each particular image. The data is from September 2005. 

The first thing I did was unzip the 4 accra folders and put the first 3 folders all in one folder that was labeled my training. I kept the 4th folder the same and called it my testing. So, my training was 90%. I then made code to import my data that allowed a pathway for my training folder, testing folder, and labels csv file. Now I have my training data, training labels, testing data, and testing labels. I originally tried to divide my training images and testing images by 255.0 but my computer wouldn’t allow me because it said that I did not have enough storage. So, I just skipped trying to standardize it unfortunately. Next, I started to build a DNN model. I used a Sequential keras model that included a flatten layer, a dense layer with 128 neurons and a relu activation, another dense layer with 64 neurons and relu activation, and then one last dense layer with 1 neuron. I used relu for my activation because relu allows for faster and more effective training of deep neural networks on larger datasets and our dataset is pretty large. I then compiled the model by using an RMSprop optimizer. I chose RMSprop as the optimizer because Rprop doesn’t work well with large datasets and RMSprop is similar to Adagrad as it still keeps the same estimate of squared gradients, but instead of letting that estimate continually accumulate over training, it keeps a moving average of it. I chose mse as my loss function because it ensures the training model has no outlier predictions with huge errors. For the metric I chose mae and mse instead of accuracy because accuracy wouldn’t be a good measure for this kind of data. Instead, the goal was to decrease mae and mse as much as possible. Next, I fit the model using the training images and training labels with 100 epochs, 90 steps per epoch, and 100 batch size. This combination gave me the best output where the mse and mae was at its lowest. My mae ended up being 35.5113 and my mse ended up being 1591.2771. Next, I evaluated my model using the testing images and testing labels that consisted of 1000 pictures and it gave me mae of 47.1175 and mse of 2493.1792. Watching the epochs run, my loss accuracy would drop tremendously from the start and then start to fluctuate as it went on. The loss increasing after decreasing was a strong indicator that the model is over fit. My mae would also increase after decrease and continue to fluctuate, so that was also an indicator of overfitting. After being happy with my results for my DNN model, I decided to make a CNN model. 

For the CNN model I used a Sequential model, I had 3 Conv2D layers that used the relu activation, 3 MaxPooling2D layers, 1 flatten layer, and 3 dense layers. When I went to compile it, I kept my arguments the same as the DNN model. Then, I fit the model to the training images and training labels using 5 epochs, 90 steps per epoch, and 100 batch size. When I first ran this code my computer CRASHED. It restarted and I lost everything. Luckily, I was writing this markup on a pdf file at first and it recovered everything I wrote above. Once I finally managed to get everything back, I reran the code and got 48.6224 mae and 7591.9077 mse. Then I evaluated the model and got 36.1886 for mae and 1764.5979 mse for the testing images and testing labels. It is clear that the CNN model worked better than the DNN model as the mae and mse were lower for the testing scores, which is the ultimate goal. It is obvious the model is still overfit as the loss and mae would fluctuate by increasing after decreasing and is not very good and with trial and error I'm sure I can get the mae and mse lower but I dont think it can't get that much lower due to limitations. I feel like this project has allowed me to explore the different variables and what they all mean in order for me to choose the appropriate things like the optimizer and activation variables. It also helped me with my debugging skills and to understand different errors that I got along the way. This project was definitely rewarding despite the hardships that were faced.

Next, I randomly picked 3 images to predict the population and used a CNN model where I used the same layers but used a subset of 3000 images for training and the same 1000 images for testing. When i fit the model I used 5 epochs, 30 steps per epoch, and 100 for batch size. It gave me 24.3942 mae and 2076.6416 for mse for the training set. When I evaluated the model it gave me 69.5349 mae and 6292.8740 for mse for the testing set. I tested the 228th image, 179th image, and 114th image. Below are my results, respectively. The model performed a lot better than I thought it would. I still believe with a lot of trial and error I can get a better mae/mse and get a better prediction. Some limitations that I found with this project was the fact that I was not able to standardize the data becuase my computer simply could not handle it. So, I am working with raw data. If I was able to standardize the data it would be able to give me better results though. 


228: ![228](https://user-images.githubusercontent.com/67920437/88588059-ee156100-d024-11ea-8b1d-e923e3fc7b15.jpeg)

![predict228](https://user-images.githubusercontent.com/67920437/88587996-d50cb000-d024-11ea-8615-c385a2e68e28.png)


predicted output: 13.79285
actual: 10.6513538360596
This was really good at predicting. 


179: ![179](https://user-images.githubusercontent.com/67920437/88588074-f5d50580-d024-11ea-87c4-4eb6046f05ed.jpeg)

![predict179](https://user-images.githubusercontent.com/67920437/88588505-ad6a1780-d025-11ea-98ea-49261955fa98.png)


predicted: 9.1854515
actual: 37.6723289489746
This was more what was expected with the error. 


114: ![114](https://user-images.githubusercontent.com/67920437/88588100-01c0c780-d025-11ea-8177-4fa4bebae89b.jpeg)

![predict114](https://user-images.githubusercontent.com/67920437/88588767-1782bc80-d026-11ea-8d57-c1083f8839ee.png)


predicted: 14.124335
actual: 8.98873329162598
I thought this did pretty well given the circumstances. 


