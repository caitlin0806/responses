A)

This is the original image.

original image: ![original image](https://user-images.githubusercontent.com/67920437/87498901-f33adf00-c626-11ea-9b8c-cedbac31fdce.png)

I tried different filters and used the vertical line enhance, sharpens image, and the blur filters. 

vertical line enhance: ![vertical line enhance](https://user-images.githubusercontent.com/67920437/87498905-f635cf80-c626-11ea-9478-1c3aff4b16e6.png)
sharpens image: ![sharpens image](https://user-images.githubusercontent.com/67920437/87693254-bff96c80-c75a-11ea-9df5-f7a870c0de2a.png)
blur: ![blur](https://user-images.githubusercontent.com/67920437/87498910-f930c000-c626-11ea-8367-824d40c3d4c7.png)

The vertical line enhance picture made the vertical lines of the original picture stand out, resulting in the picture coming out darker. The stairs itself came out brighter and easier to see and then the background/the sky was blacked out. The sharpens image filter made the picture quality so much better and came out clearer. The blur filter wasn't as obvious. It did in fact blur it and I can tell by looking very closely. I thought this one was the most fascinating since thinking about what is going on the background is that the pixels are being manipulated in a way that it uses nearby pixels to guess and change so that the result comes out different. Funtionally, the filter has weights and it is being applied to the pixels which is how they are manipulated. The application of a convolving filter to an image is useful for comptuer vision because the process itself is actually quite complex and this way it makes the process so much easier, allowing people to do it without exactly understanding what is happening in the background. Also, the process of applying filters is necessary because pictures are used for different reasons and certain filters either show/hide what is necessary for that moment. 

B)

Below I used the edge filter on the original image and then pooled it. 

edge: ![edge](https://user-images.githubusercontent.com/67920437/87501835-15842b00-c62e-11ea-9201-fca3d6000b97.png)
pooling edge: ![pooling edge](https://user-images.githubusercontent.com/67920437/87501837-161cc180-c62e-11ea-93f3-d9f9832a83bb.png)

The x-axis and y-axis of the pooled image goes up to 250, while the edge image goes to 500 on both images. So, the pooled image is a quarter as big, but the features of the image itself is still clear and remains intact. The pooling that was used was max pooling. It looked at a pixel and its neighbors that are to the right, below, and right-below. It took the largest of them by index 0 since the values are from largest to smallest and loaded it to the new image that we now see. This method is useful because it is smaller, so it takes up less space and the image itself is maintainend so you don't lose any important features. 

C)

32: ![32](https://user-images.githubusercontent.com/67920437/87723958-9820fd80-c788-11ea-9fc4-f2f015a33fad.png)
Adding the Conv2D and Maxpooling2D layers to the neural network did in fact improve the model. The accuracy was 0.9860. The first picture has a straight line that looks like a seven. As it goes on you can see a loop which could possibly by a nine. Then, there is a straight line and finally goes to a few colored boxes.

Below are the images when I changed the 32s to 16 or 64. The accuracy improved when I increased the filter of the layer and the time also increased. The accuracy decreased when I decreased the filter of the layer and so did the time. If more convolution layers are added the accuracy would increase and takes less epochs.  
32to16: ![32to16](https://user-images.githubusercontent.com/67920437/87722004-5e9ac300-c785-11ea-9eea-3546d696d069.png)
32to64: ![32to64](https://user-images.githubusercontent.com/67920437/87722014-60fd1d00-c785-11ea-85f1-0e3d84bf2e90.png)
16: loss: 0.0559 - accuracy: 0.9854
32:loss: 0.0626 - accuracy: 0.9860
64: loss: 0.0539 - accuracy: 0.9870
 
 
