2. Compile and train the model from the tensorflow exercise. Plot the training and validation loss as well as accuracy. Post your plots and describe them.
D. Text Classification with an RNN
1. Again compile and train the model from the tensorflow exercise. Plot the training
and validation loss as well as accuracy. Stack two or more LSTM layers in your
model. Post your plots and describe them.


C1) One-hot encoding is inefficient towards vectorizing a corpus of words because a one-hot encoded vector is sparse so most of the indices are zero, which isn't helpful if we had a lot of words in the vocabulary. 

C2)

![loss](https://user-images.githubusercontent.com/67920437/88739563-d44d4a00-d108-11ea-9233-083ed59b373c.png)
![accuracy](https://user-images.githubusercontent.com/67920437/88739564-d44d4a00-d108-11ea-879e-a9caf044a5df.png)

The graph that plots the training loss vs validation loss shows that the validation loss fluctuates up and down but is significantly higher than the training loss that is decliniing the whole time as the epochs increase. The training loss decreases, but the validation loss increases is a strong indicator of overfitting. 

The graph that plots the training accuracy vs validation accuracy shows that the training accuracy is continuously higher and continuously increases than the validation accuracy that flutates as the epochs increase. The training accuracy being a lot higher is a strong indicator that the model is overfit. The validation accuracy fluctuating by increasing, decreasing, and then increasing again is also another indicator of overfitting. 

D1)

![loss](https://user-images.githubusercontent.com/67920437/88741363-75d69a80-d10d-11ea-8ab2-0dbade3f2ee6.png)
![accuracy](https://user-images.githubusercontent.com/67920437/88741365-766f3100-d10d-11ea-9a90-d78249ad7d20.png)

The training loss starts off higher than the validation loss then rapidly declines as the epochs increases. The validation loss is more stable and increases as epochs increase. From middle to end the validation loss is a lot higher. The validation loss increasing and training loss decreasing is a strong indicator of overfitting. 

The training accuracy starts off a lot lower than the validation accuracy. The validation accuracy stays steady and the training accuracy has a sharp increases and then slowly increases towrds the end. In the end, the training accuracy is alot higher than the validation accuracy. The training accuracy being a lot higher than the validation accuracy is a strong indicstor that the model is overfit. 


![loss1](https://user-images.githubusercontent.com/67920437/88741370-78d18b00-d10d-11ea-8e54-2d6f10ffa3ed.png)
![accuracy1](https://user-images.githubusercontent.com/67920437/88741368-78d18b00-d10d-11ea-8240-43d40626662f.png)

Stacking two or more LSTM layers to the model didn't really make that much of a difference. As you can see, the graphs are very similar and don't hold a significant difference. 
