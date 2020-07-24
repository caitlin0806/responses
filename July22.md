A1) One-hot-coded columns is a feature provided by feature columns that let's categorical variables be converted into a form that could be provided (numerical date) to machine learning algorithms to do a better job at predicting. It puts the values into binary form where 0 relates to false and 1 relates to true. The source values are discrete. 

A2) A dense feature inspects the result of a feature column and inspects categorical columns by transforming it to an indicator column first. This can be useful because it is another way to understand the data and give new meaning since certain values can't be interpreted correctly without it. 

A3) The boosted tree model seems to have performed better since the mortality rate is higher. The probability distributuions for the linear and boosted seems quite similarly located. The ROC curve does show that the model is becoming overfit. It starts to level off at a point which means the true positive rate stays the same as false still continues to rise. The area under the curve seems to be a lot but it could be greater. The greater the area under the curve, the better the model is. 


This is for the logistic: ![Unknown-2](https://user-images.githubusercontent.com/67920437/88429737-26b6ff80-cdc5-11ea-8f29-fbe28ac589b1.png)

This is for the boosted: ![Unknown-3](https://user-images.githubusercontent.com/67920437/88429740-27e82c80-cdc5-11ea-824f-478058e7937f.png)

This is the graphs on top of eachother: ![Unknown](https://user-images.githubusercontent.com/67920437/88429735-24ed3c00-cdc5-11ea-9365-37409e99c105.png)

This is the ROC curve: ![Unknown copy](https://user-images.githubusercontent.com/67920437/88333145-b5f8e000-ccfd-11ea-972d-a5be4a80ed12.png)

B1)

![Unknown copy 2](https://user-images.githubusercontent.com/67920437/88352271-3b44ba80-cd27-11ea-82d7-e8f8f05509c5.png)
![Unknown-2](https://user-images.githubusercontent.com/67920437/88352273-3bdd5100-cd27-11ea-8458-2641ed7cb2b0.png)

The features that contributed the most to the predicted probability are sex, age, and class. The graphs are showing that being a 31 year old male in 2nd class meant your chance of survival wasn't the best. The graphs also show that fare and parch made chances of survival better.  

B2)

![Unknown-3](https://user-images.githubusercontent.com/67920437/88352274-3bdd5100-cd27-11ea-8fd6-99e6bcd95cd9.png)
![Unknown-4](https://user-images.githubusercontent.com/67920437/88352275-3bdd5100-cd27-11ea-86ee-24e2657750e0.png)

The features that are the most important are sex, class, and age which makes sense. It was shown that women were favorable for survival and the more you paid for fare the higher of chance you had for survival, which basically means if you are 1st class that increased your chance. In the 2nd graph the red corresponds to larger function values (positive) and blue was smaller (negative). So the blue would mean the survival rate was low.  
